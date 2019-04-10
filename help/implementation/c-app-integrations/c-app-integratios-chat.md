---
description: Aggiunta di chat live alla pagina.
seo-description: Aggiunta di chat live alla pagina.
seo-title: Chat
solution: Experience Manager
title: Chat
uuid: d 6761 a 69-efa 5-4 ad 3-abaf -1 ba 8 e 6 c 17 f 94
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Chat{#chat}

Aggiunta di chat live alla pagina.

Chat consente al pubblico di partecipare in tempo reale agli eventi in diretta. Il contenuto viene visualizzato come flusso continuo, stimolando la partecipazione rapida nella finestra di dialogo di annullamento della folio.

Versione corrente: La chat utilizza `fyre.conv v3.0.0.`

## Integrazione {#concept_0A99792A7E89403F95D082D52D600F17}

L'incorporazione dell'app chat segue il processo per incorporare un'app di base descritta in Guida introduttiva > [Incorporazione di un'app](../c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md#using-livefyre-js-create-customize-apps).

Esempio:

```
<html> 
  <head> 
    <script src="//cdn.livefyre.com/Livefyre.js"> 
    </script> 
  </head> 
<body> 
    <script type="text/javascript"> 
    var networkConfig = { 
      network: "client-solutions.fyre.co" 
    }; 
    var convConfig = { 
      siteId: '347674', 
      articleId: '1', 
      el: 'livefyre', 
      collectionMeta: 'eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6IlRpdGxlIDEiLCJ1cmwiOiJodHRwOlwvXC9kZXYubGl2ZWZ5cmUuY29tIiwidGFncyI6InRhZzEsdGFnMiIsImNoZWNrc3VtIjoiY2Q0YTJjYWJkMTIxOTkyM2FjZGJhMjExOWY2NmYwNTUiLCJhcnRpY2xlSWQiOiIxIn0.Dq-ghi9KYmEPmagvCS1NPyYDRMGBujm735QaTRb7E7k', 
      checksum: '6e2e4faf7b95f896260fe695eafb34ba' 
    }; 
    
    Livefyre.require(['fyre.conv#3'], function(Conv) { 
        new Conv(networkConfig, [convConfig], function(chatWidget) {}); 
        auth.delegate({ 
          login: function (callback) { 
            callback(null,{livefyre:'<userauthtoken>'}); 
          }, 
        }); 
    }); 
  
    </script> 
    <div id="livefyre"> 
    </div> 
   </body> 
</html>
```

Come indicato nella [sezione Token](../c-getting-started/c-implementation-process/c-collectionmeta-tokent.md#collectionmeta-tokent) collectionmeta, collectionmeta è un oggetto JSON codificato. Nell'esempio precedente, l'oggetto JSON prende il seguente formato prima della codifica JWT:

```
{ 
"url": "https://dev.livefyre.com/articles/test.html",  
"articleId": "1",  
"type": "livechat",  
"title": "Title 1" 
}
```

## Oggetto networkconfig {#c-networkconfig-object}

`NetworkConfig` L'oggetto è un oggetto JSON che personalizza il sistema di autenticazione per gli utenti di rete.

`NetworkConfig` L'oggetto è un oggetto JSON contenente i seguenti parametri:

| Parametro | Tipo | Descrizione |
|---|---|---|
| Authdelegate | *required* object | Utilizzato per personalizzare il sistema di autenticazione per gli utenti di rete personalizzati. |
| network | *required* string | Un nome di rete di Livefyre. Ad esempio: *nomeserver. fyre. co.* |
| Attachmentdelegate | Oggetto | Utilizzato per specificare i tipi di allegati multimediali visibili nel flusso app. Per ulteriori informazioni, consultate [Limitazione dei file multimediali](../c-app-customizations/c-restrict-media.md#c_restrict_media). |
| stringhe | *optional* object | Utilizzato per personalizzare le stringhe di testo degli elementi HTML in una qualsiasi delle app core Livefyre. Per ulteriori informazioni, consultate [Personalizzazione delle stringhe](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md). |

## Oggetto convconfig {#c-convconfig-object}

`convConfig` L'oggetto è un oggetto JSON utilizzato per specificare il contenuto renderizzato nell'app Livefyre.

>[!NOTE]
>
>I `convConfig` parametri oggetto elencati qui non sono validi per l'app Reviews. Per informazioni sull'integrazione sull'app Recensioni con l' `convConfig` oggetto, consultate Integrazione revisioni.

`ConvConfig` L'oggetto contiene i seguenti parametri richiesti:

| Parametro | Tipo | Descrizione |
|--- |--- |--- |
| Articleid | *required* string | Identifica in modo univoco una raccolta all'interno del sito. Generalmente corrisponde a una chiave primaria del database o all'ID post all'interno del CMS. Ad esempio: «post -42». Limite di 255 caratteri. Nota: Se utilizzate l'URL articolo come articleid, accertatevi che la stringa sia MD 5 o SHA -1. |
| Collectionmeta | *required* string | Metadati codificati in JWT sulla raccolta. Per [ulteriori informazioni, vedere](../c-getting-started/c-implementation-process/c-collectionmeta-tokent.md#collectionmeta-tokent) Oggetto collectionmeta. |
| el | *required* string | L'ID di un elemento DOM a cui verrà eseguito il rendering del flusso di contenuto. |
| Siteid | *required* string | L'ID di Livefyre per il sito Web o l'applicazione a cui appartiene la raccolta. Ad esempio: «303617». |

>[!NOTE]
>
>Il `app` parametro non è richiesto per l'implementazione di un'app commenti.

L `ConvConfig` 'oggetto può contenere anche i seguenti parametri facoltativi:

| Parametro | Tipo | Descrizione |
|--- |--- |--- |
| Actionbuttons | *optional* array | Un array di pulsanti di azione personalizzati da aggiungere a una parte di contenuto accanto ai pulsanti Condividi e Flag. Per ulteriori informazioni, consultate Aggiunta di pulsanti personalizzati. |
| animazioni | *optional* boolean | Definisce se le animazioni verranno eseguite nell'app Livefyre. Impostate su false per disabilitare le animazioni. Impostazione predefinita: true. |
| Anonousflaggingenabled | *optional* boolean | Definisce se gli utenti ospiti hanno la possibilità di segnalare il contenuto. Il valore predefinito è true. |
| Browsertype | *optional* string | Definisce il dispositivo per il quale deve essere generato il contenuto di visualizzazione. In questo modo, i CSS e alcune funzionalità saranno modificati in base al tipo di dispositivo di input. Le opzioni sono desktop, dispositivi mobili o tablet. (Se lasciato vuoto, predefinito la determinazione Agente Google per il formato di visualizzazione.) |
| checksum | *stringa consigliata* (consigliato) | Identifica lo stato corrente della raccolta collectionmeta. Modificando questo valore, Livefyre può aggiornare i dati sul server con i nuovi valori in collectionmeta. |
| Datetimeformat | *funzione oggetto* stringa opzionale | Specifica il formato datetime del contenuto in streaming. Per ulteriori informazioni, consultate Timbri data e ora. |
| Disableavatars | *optional* boolean | Impedisce il rendering di avatar nel flusso app e riduce quindi il numero di elementi caricati nel browser. Il valore predefinito è false. |
| disableIE8Shim | *optional* boolean | Disattiva l'ombreggiatura predefinita utilizzata da Livefyre per il polifill Internet Explorer 8, in modo che gli elementi HTML 5 siano supportati. Livefyre usa il seguente progetto: [https://github.com/aFarkas/html5shiv](https://github.com/aFarkas/html5shiv). Il valore predefinito è false. Nota: Se questo valore è false, è necessario utilizzare il polifill di some sort prima che sia richiamato Livefyre Chat per il supporto di Internet Explorer 8. |
| Disablethirdpartyanalytics | *optional* bboolean | Disabilita i sistemi di analisi di terze parti (Quantserve e Google Analytics) che Livefyre può utilizzare per le misure interne. Il valore predefinito è false. |
| Editorcss | *optional* object | Utilizzato per personalizzare lo stile dell'editor commento. Potete definire lo stile del colore dello sfondo del campo dell'editor, nonché il colore, le dimensioni e la famiglia del testo che vengono visualizzati all'interno dell'editor. Ad esempio: `{background: ‘#ccc’, color: ‘red’, font: ’30px “Helvetica Neue”, Helvetica, Arial, Geneva, sans-serif’}` |
| Initialnumvisible | *numero* intero opzionale | Consente di impostare il numero predefinito di commenti visibili nell'app al momento del caricamento. Può essere un numero intero compreso tra 1 e 50. |
| Initialnumvisiblelegacy | *numero* intero opzionale | Consente di impostare il numero predefinito di elementi di contenuto precedenti visibili nell'app al momento del caricamento. Può essere un numero intero compreso tra 1 e 50. Se questo parametro non è specificato, predefinito initialnumvisible. Ad esempio: Se la raccolta include 100 commenti attivi e 100 precedenti, impostare initalnumvisible: 10 e initialnumvisiblelegacy: 5, per visualizzare 10 commenti attivi (con un pulsante Mostra più) + 5 archivio (con un pulsante Mostra più). |
| Maxvisible | *numero* intero opzionale | Imposta il numero massimo di parti visibili del contenuto di livello principale nell'app chat. Se sono presenti nuove parti di flusso contenuto in, il contenuto nella parte inferiore del flusso verrà rimosso dalla pagina. Se viene fatto clic sul pulsante Mostra più…, il parametro viene ignorato e l'utente è gratuito per mostrare il contenuto desiderato. (Utilizzate questo parametro per controllare il numero di elementi visualizzati sulla pagina in flussi ad alta velocità). |
| Posttobuttons | *optional* array | Utilizzato per configurare i fornitori visualizzati durante l'incorporazione dell'app blog live. Le opzioni disponibili sono tw (Twitter), fb (Facebook) e li (linkedin). Impostazione predefinita [ : tb ]. |
| Readonly | *optional* boolean | Disattiva tutte le interattività per la raccolta. Se è true, gli utenti non potranno effettuare l'accesso al flusso e non possono pubblicare, modificare, rispondere o come il contenuto. Se è true, gli utenti potranno segnalare e condividere il contenuto. Il valore predefinito è false. |
| stream | *optional* object | Contiene opzioni per configurare lo streaming dell'app. |
| stream. catchup | *numero* intero opzionale | Specifica il numero di secondi precedente al momento corrente in cui il flusso deve essere caricato. Per impostazione predefinita, Livefyre carica 50 pezzi di contenuto, quindi carica tutto il contenuto inviato tra questi e il tempo corrente. Nei casi d'uso molto veloci, il contenuto potrebbe venire postato troppo rapidamente per consentire all'app di eseguire il'accessò al presente. Utilizzate questa impostazione per definire il numero di secondi precedente per il quale verrà pubblicato il contenuto (dopo il caricamento iniziale del contenuto). |
| stream. delay | *numero* intero opzionale | Specifica il numero di secondi tra richieste di streaming. Utilizzate questo parametro per controllare il flusso dei contenuti e ritardare la frequenza con cui il DOM viene aggiornato. Nota: Se il valore è troppo elevato, il flusso potrebbe cadere dietro. |


>[!NOTE]
>
>È possibile trasmettere uno o più `convConfig` oggetti durante l'inizializzazione dell'app per visualizzare più app sulla stessa pagina. Tenete presente che altre app utilizzano risorse browser e le prestazioni possono degradarsi a mano a mano che il numero aumenta.

## Oggetto collectionmeta {#c-collectionmeta-object}

`CollectionMeta` L'oggetto è un oggetto JSON che specifica i metadati da memorizzare all'interno della raccolta.

`CollectionMeta` è sempre codificata prima di essere passata a Livefyre per la sicurezza. Il valore codificato viene passato nell' `ConvConfig` oggetto indicato sopra.

>[!NOTE]
>
>È necessario aggiungere un codice lato server per codificare l'oggetto `CollectionMeta` JSON. Per ulteriori informazioni, consultate Creazione di token lato server.

| Parametro | Tipo | Descrizione |
|--- |--- |--- |
| Articleid | *required* string | ID univoco per la raccolta. |
| title | *required* string | Titolo da applicare alla raccolta. Spesso corrisponde al titolo della pagina che visualizza l'app. Ad esempio: «Integrazione è molto divertente! »» Nota: La lunghezza massima del carattere per il titolo è 255 caratteri. Il campo Titolo non supporta le entità HTML. Codificate caratteri speciali utilizzando UTF -8. |
| url | *required* string | L'URL assoluto canonico che desiderate allegare a questa raccolta. Questo URL verrà utilizzato per generare collegamenti all'app dal contenuto condiviso su Facebook e Twitter, notifiche e-mail e Livefyre Studio. Nota: Livefyre richiede l'utilizzo di un nome di dominio qualificato, il numero di porta o un callback per risolvere la configurazione locale non è richiesto. In caso di test localmente, assicuratevi che sia utilizzato un dominio URL di base valido. (Ad esempio: `https://customer.com` is valid, while `https://localhost:5995` not.) Una volta configurato il server Web locale per accettare un nome di dominio qualificato, non sono necessari callback o risoluzioni e lo sviluppo locale può procedere come previsto. |
| type | *required* string | Il tipo di raccolta. Deve essere live. |

L `CollectionMeta` 'oggetto può contenere anche il seguente parametro opzionale:

| Parametro | Tipo | Descrizione |
|--- |--- |--- |
| tag | *optional* string | Un elenco separato da virgole di parole chiave o frasi. Cerca raccolte in base ai tag in Studio o nell'API di ricerca. Nota: I tag aggiunti tramite Studio possono contenere spazi, i tag inseriti tramite l'API non possono. Utilizzate i caratteri di sottolineatura per definire i tag che visualizzeranno gli spazi nell'interfaccia utente. (Ad esempio: use Monday_ Quarterback per visualizzare Lunedì Quarterback in Studio.) |

## Aggiunta di un gestore di eventi {#concept_E7C17EFB43F24F1A8572E60C69176C6D}

Per registrare i gestori di eventi, utilizzate la chiamata al widget. on all'interno della funzione di callback dell'app.

Ad esempio:

```
Livefyre.require(['fyre.conv#3'], function(Conv) { 
   new Conv(networkConfig, [convConfig], function(widget) { 
      widget.on('<strong><eventName></strong>', function (data) { 
         // Do something, perhaps using data 
      }); 
   }); 
});
```

Per ulteriori informazioni, e per un elenco degli eventi disponibili, vedere [Eventi Javascript](../c-app-customizations/c-javascript-events.md#c_javascript_events).