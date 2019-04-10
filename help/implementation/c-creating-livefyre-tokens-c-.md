---
description: Scoprite come generare token Livefyre utilizzando la lingua "C
seo-description: Scoprite come generare token Livefyre utilizzando la lingua "C
seo-title: Creazione di Livefyre Tokens'C
solution: Experience Manager
title: Creazione di Livefyre Tokens'C
uuid: c 5 e 05625-8550-4 b 51-9211-134600 e 20 ec 7
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Creazione di token Livefyre C\ # {#creating-livefyre-tokens-c}

Scopri come generare token Livefyre utilizzando il linguaggio ``C#``.

Puoi sfruttare la documentazione precedente e il codice di esempio da utilizzare `C#.NET` per scrivere metodi per la creazione di token.

Per fare riferimento alle librerie ufficiali di Livefyre, utilizzate la [Libreria Java](https://github.com/Livefyre/livefyre-java-utils) come punto di partenza per `C#` gli sviluppatori.

Potete anche utilizzare la libreria [Node. js](https://github.com/Livefyre/livefyre-nodejs-utils) dalla riga di comando per generare token di riferimento personali e acquisire familiarità con la struttura del metodo.

* [Passare al token meta della raccolta](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-collectionMeta-token)
* [Passa al token di autenticazione](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-auth-token)

## Dipendenze {#section_c15_fnh_xz}

* Per generare i token, sarà necessario il pacchetto [JWT cloud](https://www.nuget.org/packages/JWT) nel progetto.
* Gli esempi di codice in questa pagina utilizzano il pacchetto [Newtonsoft JSON](https://www.nuget.org/packages/newtonsoft.json/) .

## Token collectionmeta {#section_dzt_4mh_xz}

Il Token collectionmeta viene passato a Livefyre quando incorporate Commenti su una pagina e fornisce il nostro sistema ai metadati necessari per la nuova raccolta. Inoltre, dovrete creare un MD 5 `checksum` di questi dati, che Livefyre verifica per verificare se i metadati sono cambiati. (ad es. se il titolo o l'URL dell'articolo è stato modificato).

Questo token è firmato con voi `Site Key`, fornito dal vostro Account Manager tecnico in Livefyre.

Vedi anche:

* Documenti token collectionmeta ufficiali
* [Esempio gist](https://gist.github.com/pcolombo/dbbea020618c521a2bd5)

1. Create un dictonario contenente i metadati per la raccolta. In questo passaggio verranno aggiunti solo alcuni dei campi necessari, richiamati da prima di aggiungere l'articleid.

   ```
       // Site Key provided by Livefyre 
       string siteSecret = "ABCDE1234"; 
   
       var meta = new Dictionary<string, object>() { 
           {"title", "Kings win the Stanley Cup"}, 
           {"url", "https://www.website.com/kings-win-stanley-cup"}, 
           {"tags", "sports, hockey, stanley_cup"}, 
           {"type", "livecomments"} 
       };
   ```

   * **titolo** *richiesto*: Titolo della raccolta, in genere il titolo dell'articolo. La lunghezza massima è di 255 caratteri. Non supporta le entità HTML. Codificate caratteri speciali utilizzando UTF -8.
   * **url** *richiesto*: L'URL canonico dell'articolo. Questa funzione viene utilizzata dalle funzioni di condivisione dei commenti e di sincronizzazione social network e collegamenti all'articolo dal dashboard Amministratore. Se si verifica localmente, tenete presente che Livefyre non accetta «localhost» come dominio.
   * **tag** *facoltativi*: Elenco di tag separati da virgole da aggiungere alla raccolta nel dashboard di Livefyre. I tag non possono contenere spazi. Utilizza i caratteri di sottolineatura se vuoi che uno spazio venga visualizzato nell'Admin Dashboard.
   * **type** *facoltativo*: Stringa che indica il tipo di raccolta da creare. I valori validi sono:

      * `reviews`
      * `sidenotes`
      * `ratings`
      * `counting`
      * `livecomments`
      * `liveblog`
      * `livechat`
      Se non viene specificata, per impostazione predefinita viene creata una raccolta livecomments.


1. JSON codifica questo dizionario e genera un checksum md 5.

   ```
          var metaStr = JsonConvert.SerializeObject(meta); 
       byte[] hash; 
   
       using (var md5 = MD5.Create()) 
       { 
           hash = md5.ComputeHash(Encoding.UTF8.GetBytes(metaStr)); 
       } 
   
       StringBuilder sBuilder = new StringBuilder(); 
   
       // Loop through each byte of the hashed data  
       // and format each one as a hexadecimal string  
       for (int i = 0; i < hash.Length; i++) 
       { 
           sBuilder.Append(hash[i].ToString("x2")); 
       } 
   ```

1. Aggiungere l' **articleid** al Dizionario. Il **checksum** non entra nel token collectionmeta, ma deve essere inviato come parametro seaprate nell'oggetto js convconfig.

   ```
       meta.Add("articleId", "article-abcde00001"); 
   ```

   * **Articleid** *richiesto*: Un identificatore univoco per la raccolta nel sito Livefyre. In genere, l'elemento articleid univoco utilizzato nel CMS. (ad es. l'ID post wordpress) Questo valore non deve mai cambiare. Livefyre identifica raccolte univoche in base alla combinazione di siteid e articleid.

1. Generare un Token JWT firmato del Dizionario, utilizzando la chiave del sito fornita da Livefyre. È necessario specificare l'algoritmo hash corretto, in quanto il pacchetto JWT non utilizza HS 256 per impostazione predefinita.

   ```
       string token = JWT.JsonWebToken.Encode(meta, siteSecret, JWT.JwtHashAlgorithm.HS256);
   ```

## Token autenticazione utente {#section_g1d_43h_xz}

Il token di autenticazione utente viene usato per firmare un utente in Livefyre. Quando un utente accede al sito, il sito genera un token di autenticazione utente passato al widget Livefyre sulla pagina. (Per ulteriori informazioni sul processo di autenticazione, consulta Profili remoti.)

Questo token richiede il nome rete (network. fyre. co) ed è firmato con la vostra chiave di rete, fornito dall'Account Manager tecnico in Livefyre.

Vedi anche:

* Docs token di autenticazione ufficiali
* [Esempio gist](https://gist.github.com/pcolombo/7d7403172c28734c87e2)

1. Create un dictonario contenente le informazioni necessarie.

   ```
       string networkKey = "ABCDEF1234"; 
   
       var payload = new Dictionary<string, object>() {  
               { "domain", "mynetwork.fyre.co" }, 
               { "user_id", "user-00001" }, 
               { "expires", DateTime.Now.AddDays(7).Ticks }, 
               { "display_name", "johndoe" } 
           }; 
   ```

   * **domain:** Il nome della rete (fornito da Livefyre). ad esempio mynetwork. fyre. co
   * **user_ id:** L'ID utente univoco per l'utente nel sistema di profilo del sito. Devono essere solo caratteri alfanumerici (A-Z, a-z, 0-9). Se l'ID utente di sistema contiene grafici non validi, prendete in considerazione l'invio di Livefyre un hash md 5 dell'ID utente oppure una versione di esso basata su 64. (Lasciate che sia il manager dell'account a sapere se farlo.)
   * **scade:** Data (in tempo epoch) della scadenza del token. Questo deve corrispondere al tempo di sessione degli accessi sul sito, in modo che lo stato Accesso di Livefyre rimanga sincronizzato con lo stato di accesso del sito.
   * **display_ name:** Nome visualizzato dell'utente nel sistema di profilo, in quanto dovrebbe essere visualizzato nel flusso di commento.

1. Generare un Token JWT firmato del Dizionario, utilizzando la chiave di rete fornita da Livefyre. È necessario specificare l'algoritmo hash corretto, in quanto il pacchetto JWT non utilizza HS 256 per impostazione predefinita.

   ```
          string token = JWT.JsonWebToken.Encode(payload, networkKey, JWT.JwtHashAlgorithm.HS256);
   ```
