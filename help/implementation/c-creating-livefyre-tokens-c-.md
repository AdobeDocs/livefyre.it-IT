---
description: Scopri come generare token Livefyre utilizzando il linguaggio C#.
title: Creazione di token Livefyre `C#`
exl-id: 6360c325-0c3f-4ecb-90f7-951ef4e6f410
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '784'
ht-degree: 1%

---

# Creazione di token Livefyre C\# {#creating-livefyre-tokens-c}

Scopri come generare token Livefyre utilizzando il linguaggio ``C#``.

Puoi sfruttare la documentazione legacy e il codice di esempio per utilizzare `C#.NET` per scrivere i metodi per creare i token.

Per fare riferimento alle librerie ufficiali di Livefyre, utilizza la [Libreria Java](https://github.com/Livefyre/livefyre-java-utils) come punto di partenza per gli sviluppatori `C#`.

È inoltre possibile utilizzare la [Libreria Node.js](https://github.com/Livefyre/livefyre-nodejs-utils) dalla riga di comando per generare token di riferimento autonomamente e per acquisire familiarità con la struttura del metodo.

* [Passa alla raccolta del token metadati](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-collectionMeta-token)
* [Passa al token di autenticazione](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-auth-token)

## Dipendenze {#section_c15_fnh_xz}

* Per generare i token è necessario il [pacchetto di nuget JWT](https://www.nuget.org/packages/JWT) nel progetto.
* Gli esempi di codice su questa pagina utilizzano il pacchetto [Newtonsoft JSON](https://www.nuget.org/packages/newtonsoft.json/) .

## Token CollectionMeta {#section_dzt_4mh_xz}

Il Token CollectionMeta viene passato a Livefyre quando incorpori commenti su una pagina e fornisce al nostro sistema i metadati necessari per la tua nuova raccolta. Inoltre, creerai un MD5 `checksum` di questi dati, che Livefyre controlla per vedere se i metadati sono cambiati. (ad esempio, se il titolo o l’url dell’articolo è stato modificato).

Questo token è firmato con il tuo `Site Key`, che ti è stato fornito dal tuo Technical Account Manager di Livefyre.

Vedi anche:

* Documentazione ufficiale del token CollectionMeta
* [Esempio Gist](https://gist.github.com/pcolombo/dbbea020618c521a2bd5)

1. Crea un dizionario contenente i metadati della raccolta. In questo passaggio aggiungeremo solo alcuni dei campi necessari, perché vogliamo creare un checksum di questo oggetto PRIMA di aggiungere l’articleId.

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

   * **** *titolarità richiesta*: Il titolo della raccolta, in genere il titolo dell’articolo. La lunghezza massima è di 255 caratteri. Non supporta le entità html. Codifica caratteri speciali utilizzando UTF-8.
   * **** *Valore obbligatorio*: URL canonico dell’articolo. Viene utilizzato dalle funzioni di condivisione dei commenti e sincronizzazione social e dai collegamenti all’articolo dal dashboard di amministrazione. Se esegui un test localmente, tieni presente che Livefyre non accetterà &quot;localhost&quot; come dominio.
   * **** *tagsopzionale*: Un elenco di tag separati da virgole da aggiungere alla raccolta nel dashboard Livefyre. I tag non possono contenere spazi. Utilizza i caratteri di sottolineatura se desideri che uno spazio venga visualizzato nel dashboard di amministrazione.
   * **** *typeoptional*: Una stringa che indica il tipo di raccolta da creare. I valori validi sono:

      * `reviews`
      * `sidenotes`
      * `ratings`
      * `counting`
      * `livecomments`
      * `liveblog`
      * `livechat`

      Se non viene specificato, per impostazione predefinita viene creata una raccolta LiveComments.


1. JSON codifica questo dizionario e genera un checksum md5 di esso.

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

1. Aggiungi il **articleId** al dizionario . Il **checksum** non va nel token collectionMeta, ma deve essere inviato come parametro separato nell&#39;oggetto convConfig js .

   ```
       meta.Add("articleId", "article-abcde00001"); 
   ```

   * **** *articleId*: Un identificatore univoco per la tua raccolta all&#39;interno del tuo sito Livefyre. In genere, l&#39;id articolo univoco utilizzato nel CMS. (ad esempio, l&#39;ID del post di WordPress) Questo valore non deve mai cambiare. Livefyre identifica raccolte univoche dalla combinazione di siteId e articleId.

1. Genera un token JWT firmato del dizionario, utilizzando la chiave del sito fornita da Livefyre. Tieni presente che devi specificare l’algoritmo hash corretto, in quanto il pacchetto JWT non utilizza HS256 per impostazione predefinita.

   ```
       string token = JWT.JsonWebToken.Encode(meta, siteSecret, JWT.JwtHashAlgorithm.HS256);
   ```

## Token di autenticazione utente {#section_g1d_43h_xz}

Il Token di autenticazione dell’utente viene utilizzato per firmare un utente in Livefyre. Quando un utente accede al tuo sito, il sito genera un token di autenticazione utente che viene passato al widget Livefyre sulla pagina. (Per ulteriori informazioni sul processo di autenticazione, vedere Profili remoti.)

Questo token richiede il tuo nome di rete (network.fyre.co) e viene firmato con la tua chiave di rete che ti viene fornita dal tuo Account Manager tecnico su Livefyre.

Vedi anche:

* Documenti ufficiali del token di autenticazione
* [Esempio Gist](https://gist.github.com/pcolombo/7d7403172c28734c87e2)

1. Crea un dizionario contenente le informazioni necessarie.

   ```
       string networkKey = "ABCDEF1234"; 
   
       var payload = new Dictionary<string, object>() {  
               { "domain", "mynetwork.fyre.co" }, 
               { "user_id", "user-00001" }, 
               { "expires", DateTime.Now.AddDays(7).Ticks }, 
               { "display_name", "johndoe" } 
           }; 
   ```

   * **dominio:** il nome della tua rete (fornito da Livefyre). ad esempio mynetwork.fyre.co
   * **user_id:** l’ID utente univoco per l’utente nel sistema di profilo del tuo sito. Deve essere composto solo da caratteri alfanumerici (A-Z, a-z, 0-9). Se gli ID utente del sistema contengono caratteri non validi, considera l’invio di un hash md5 dell’ID utente o di una versione codificata base64. (Informare il tuo account manager se lo fai).
   * **Scadenza:** la data (in Epoch time) in cui scade il token. Questo dovrebbe corrispondere al tempo di sessione degli accessi sul sito, in modo che lo stato di accesso di Livefyre rimanga sincronizzato con lo stato di accesso del sito.
   * **display_name:** il nome visualizzato dell’utente nel sistema del profilo, come dovrebbe essere visualizzato nel flusso di commenti.

1. Genera un token JWT firmato del dizionario, utilizzando la chiave di rete fornita da Livefyre. Tieni presente che devi specificare l’algoritmo hash corretto, in quanto il pacchetto JWT non utilizza HS256 per impostazione predefinita.

   ```
          string token = JWT.JsonWebToken.Encode(payload, networkKey, JWT.JwtHashAlgorithm.HS256);
   ```
