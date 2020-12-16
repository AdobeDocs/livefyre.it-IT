---
description: Scoprite come generare token Livefyre utilizzando il linguaggio "C#".
seo-description: Scoprite come generare token Livefyre utilizzando il linguaggio "C#".
seo-title: Creazione di token Livefyre `C#`
solution: Experience Manager
title: Creazione di token Livefyre `C#`
uuid: c5e05625-8550-4b51-9211-134600e20ec7
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 1%

---


# Creazione di token Livefyre C\# {#creating-livefyre-tokens-c}

Scopri come generare token Livefyre utilizzando il linguaggio ``C#``.

È possibile utilizzare la documentazione e il codice di esempio legacy per utilizzare `C#.NET` per creare token con metodi di scrittura.

Per fare riferimento alle librerie ufficiali di Livefyre, utilizzate la [libreria Java](https://github.com/Livefyre/livefyre-java-utils) come punto di partenza per gli sviluppatori `C#`.

È inoltre possibile utilizzare la libreria [Node.js](https://github.com/Livefyre/livefyre-nodejs-utils) dalla riga di comando per generare token di riferimento personalizzati e per acquisire familiarità con la struttura del metodo.

* [Passare al token di metadati della raccolta](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-collectionMeta-token)
* [Passare al token di autenticazione](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-auth-token)

## Dipendenze {#section_c15_fnh_xz}

* Per generare i token è necessario il [pacchetto di destinazione JWT](https://www.nuget.org/packages/JWT) nel progetto.
* Gli esempi di codice presenti in questa pagina utilizzano il pacchetto [Newtonsoft JSON](https://www.nuget.org/packages/newtonsoft.json/).

## CollectionMeta Token {#section_dzt_4mh_xz}

CollectionMeta Token viene passato a Livefyre quando si incorpora Commenti in una pagina e fornisce al nostro sistema i metadati necessari per la nuova raccolta. Inoltre, verrà creato un MD5 `checksum` di questi dati, che Livefyre verifica per verificare se i metadati sono cambiati. (ad esempio se il titolo o l’URL dell’articolo è stato modificato).

Questo token viene firmato con il `Site Key`, fornito dall&#39;Account Manager tecnico di Livefyre.

Vedi anche:

* Raccolta ufficialeMetadati Docs
* [Esempio Gist](https://gist.github.com/pcolombo/dbbea020618c521a2bd5)

1. Create un dizionario contenente i metadati per la raccolta. In questo passaggio verranno aggiunti solo alcuni dei campi necessari, perché si desidera creare un checksum di questo oggetto prima di aggiungere articleId.

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

   * **** *titolarità richiesta*: Il titolo della raccolta, in genere il titolo dell&#39;articolo. La lunghezza massima è di 255 caratteri. Non supporta le entità HTML. Codificare caratteri speciali utilizzando UTF-8.
   * **** *non richiesto*: URL canonico dell&#39;articolo. Questo viene utilizzato dalle funzioni di condivisione dei commenti e sincronizzazione social network, e dai collegamenti all&#39;articolo dal dashboard di amministrazione. Se eseguite il test localmente, tenete presente che Livefyre non accetterà ‘localhost’ come dominio.
   * **** *tagsico*: Un elenco separato da virgole di tag da aggiungere alla raccolta nel dashboard Livefyre. I tag non possono contenere spazi. Utilizzate i caratteri di sottolineatura se desiderate che uno spazio venga visualizzato nel dashboard di amministrazione.
   * **** *typeoptional*: Una stringa che indica il tipo di raccolta da creare. I valori validi sono:

      * `reviews`
      * `sidenotes`
      * `ratings`
      * `counting`
      * `livecomments`
      * `liveblog`
      * `livechat`

      Se non viene specificato, per impostazione predefinita viene creata una raccolta LiveComments.


1. JSON codifica questo dizionario e ne genera un checksum md5.

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

1. Aggiungete il **articleId** al dizionario. Il **checksum** non va nel token collectionMeta, ma deve essere inviato come parametro separato nell&#39;oggetto convConfig js.

   ```
       meta.Add("articleId", "article-abcde00001"); 
   ```

   * **** *articleId*: Un identificatore univoco per la raccolta all&#39;interno del sito Livefyre. In genere, l’ID articolo univoco utilizzato nel CMS. (ad esempio, l&#39;ID del post di WordPress) Questo valore non deve mai essere modificato. Livefyre identifica raccolte univoche dalla combinazione di siteId e articleId.

1. Generate un token JWT firmato del dizionario, utilizzando la chiave del sito fornita da Livefyre. Tenete presente che dovete specificare l&#39;algoritmo hash corretto, in quanto il pacchetto JWT non utilizza HS256 per impostazione predefinita.

   ```
       string token = JWT.JsonWebToken.Encode(meta, siteSecret, JWT.JwtHashAlgorithm.HS256);
   ```

## Token autenticazione utente {#section_g1d_43h_xz}

Il token di autenticazione utente viene utilizzato per firmare un utente in Livefyre. Quando un utente accede al sito, il sito genera un token di autenticazione utente che viene passato al widget Livefyre sulla pagina. Per ulteriori informazioni sul processo di autenticazione, vedere Profili remoti.

Questo token richiede il nome della rete (network.fyre.co) e viene firmato con la chiave di rete fornita dall&#39;Account Manager tecnico di Livefyre.

Vedi anche:

* Documenti token di autenticazione ufficiale
* [Esempio Gist](https://gist.github.com/pcolombo/7d7403172c28734c87e2)

1. Create un dizionario contenente le informazioni necessarie.

   ```
       string networkKey = "ABCDEF1234"; 
   
       var payload = new Dictionary<string, object>() {  
               { "domain", "mynetwork.fyre.co" }, 
               { "user_id", "user-00001" }, 
               { "expires", DateTime.Now.AddDays(7).Ticks }, 
               { "display_name", "johndoe" } 
           }; 
   ```

   * **dominio:** il nome della rete (fornito da Livefyre). ad esempio mynetwork.fyre.com
   * **user_id:** ID utente univoco per l’utente nel sistema del profilo del sito. Deve essere composto solo da caratteri alfanumerici (A-Z, a-z, 0-9). Se l&#39;ID utente del sistema contiene caratteri non validi, provate a inviare un hash di Livefyre 5 dell&#39;ID utente o una versione codificata di base64. Informate il vostro account manager.
   * **scade:** la data (in Epoch Time) in cui il token scade. Questo deve corrispondere all’ora di sessione degli accessi sul sito, in modo che lo stato di accesso di Livefyre rimanga sincronizzato con lo stato di accesso del sito.
   * **display_name:** il nome visualizzato dall&#39;utente nel sistema del profilo, così come dovrebbe essere visualizzato nel flusso dei commenti.

1. Generate un token JWT firmato del dizionario, utilizzando la chiave di rete fornita da Livefyre. Tenete presente che dovete specificare l&#39;algoritmo hash corretto, in quanto il pacchetto JWT non utilizza HS256 per impostazione predefinita.

   ```
          string token = JWT.JsonWebToken.Encode(payload, networkKey, JWT.JwtHashAlgorithm.HS256);
   ```
