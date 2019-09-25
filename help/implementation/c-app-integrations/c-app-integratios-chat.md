---
description: Aggiunta di chat live alla pagina.
seo-description: Aggiunta di chat live alla pagina.
seo-title: Chat
solution: Experience Manager
title: Chat
uuid: d6761a69-efa5-4ad3-abaf-1ba8e6c17f94
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Chat{#chat}

Aggiunta di chat live alla pagina.

La chat consente al pubblico di avviare una conversazione in tempo reale intorno agli eventi in diretta. Il contenuto viene visualizzato come un flusso continuo che incoraggia una rapida partecipazione al dialogo in corso.

Versione corrente: Utilizzo della chat `fyre.conv v3.0.0.`

## Integrazione {#concept_0A99792A7E89403F95D082D52D600F17}

L'incorporazione dell'app chat segue il processo di incorporazione di un'app di base descritto in Guida introduttiva &gt; [Incorporazione di un'app](../c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md#using-livefyre-js-create-customize-apps).

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

Come indicato nella sezione [CollectionMeta Token](../c-getting-started/c-implementation-process/c-collectionmeta-tokent.md#collectionmeta-tokent) , CollectionMeta è un oggetto JSON codificato. Nell'esempio precedente, l'oggetto JSON ha il formato seguente prima della codifica JWT corrispondente:

```
{ 
"url": "https://dev.livefyre.com/articles/test.html",  
"articleId": "1",  
"type": "livechat",  
"title": "Title 1" 
}
```

## Oggetto NetworkConfig {#c-networkconfig-object}

L' `NetworkConfig` oggetto è un oggetto JSON che personalizza il sistema di autenticazione per gli utenti della rete.

L' `NetworkConfig` oggetto è un oggetto JSON contenente i seguenti parametri:

| Parametro | Tipo | Descrizione |
|---|---|---|
| authDelegate | *oggetto obbligatorio* | Utilizzato per personalizzare il sistema di autenticazione per gli utenti di rete personalizzati. |
| network | *stringa obbligatoria* | Un nome di rete Livefyre. Ad esempio: *nomeutente.fyre.co.* |
| attachmentDelegate | Oggetto | Utilizzato per specificare i tipi di allegati multimediali visibili nel flusso App. Per ulteriori informazioni, consultate [Limitazione dei file multimediali](../c-app-customizations/c-restrict-media.md#c_restrict_media). |
| strings | *oggetto facoltativo* | Utilizzato per personalizzare le stringhe di testo degli elementi HTML in una qualsiasi delle app core Livefyre. Per ulteriori informazioni, vedere Personalizzazioni di [stringhe](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md). |

## Oggetto ConvConfig {#c-convconfig-object}

L' `convConfig` oggetto è un oggetto JSON utilizzato per specificare il contenuto di cui viene eseguito il rendering nell'app Livefyre sulla pagina.

>[!NOTE]
>
>I parametri `convConfig` oggetto elencati qui non si applicano all'app Reviews. Per informazioni sull'integrazione dell'app Reviews tramite l' `convConfig` oggetto, vedere Integrazione delle recensioni.

L' `ConvConfig` oggetto contiene i seguenti parametri obbligatori:

| Parametro | Tipo | Descrizione |
|--- |--- |--- |
| articleId | *stringa obbligatoria* | Identifica in modo univoco una raccolta all'interno del sito. In genere corrisponde a una chiave primaria del database o a un ID Post all’interno del CMS. Ad esempio: "post-42". Limite di 255 caratteri.  Nota:  Se utilizzate l'URL dell'articolo come articleId, accertatevi che la stringa sia codificata MD5 o SHA-1. |
| collectionMeta | *stringa obbligatoria* | Metadati codificati JWT per la raccolta. Per ulteriori informazioni, consulta [CollectionMeta Object](../c-getting-started/c-implementation-process/c-collectionmeta-tokent.md#collectionmeta-tokent) . |
| el | *stringa obbligatoria* | L'ID di un elemento DOM a cui verrà eseguito il rendering del flusso di contenuto. |
| siteId | *stringa obbligatoria* | L'ID Livefyre fornito per il sito Web o l'applicazione a cui appartiene la raccolta. Ad esempio: "303617". |

>[!NOTE]
>
>Il `app` parametro non è richiesto per l'implementazione di un'app di commenti.

L' `ConvConfig` oggetto può anche contenere i seguenti parametri facoltativi:

| Parametro | Tipo | Descrizione |
|--- |--- |--- |
| actionButtons | *array facoltativo* | Un array di pulsanti di azione personalizzati da aggiungere a un contenuto accanto ai pulsanti Condividi e Contrassegna. Per ulteriori informazioni, consultate Aggiunta di pulsanti personalizzati. |
| animazioni | *facoltativo* boolean | Definisce se le animazioni verranno eseguite nell'app Livefyre. Impostate su false per disabilitare le animazioni. Il valore predefinito è true. |
| anonimoFlaggingEnabled | *facoltativo* boolean | Definisce se gli utenti ospiti dispongono dell’opzione per contrassegnare il contenuto. Il valore predefinito è true. |
| browserType | *stringa facoltativa* | Definisce il dispositivo per il quale generare il contenuto di visualizzazione. Ciò causerà la modifica del CSS e di alcune funzionalità per adattarlo al tipo di dispositivo di input. Le opzioni sono desktop, mobile o tablet. Se lasciato vuoto, per impostazione predefinita verrà utilizzata la determinazione di Google Agent per il formato di visualizzazione. |
| checksum | *stringa consigliata* (consigliato) | Identifica lo stato corrente di CollectionMeta. Modificando questo valore, Livefyre aggiornerà i dati sul server con i nuovi valori in CollectionMeta. |
| datetimeFormat | *funzione oggetto stringa opzionale* | Specifica il formato datetime del contenuto in streaming. Per ulteriori informazioni, vedere Personalizzazione dei timbri data e ora. |
| disableAvatars | *facoltativo* boolean | Impedisce il rendering degli avatar nel flusso App e riduce quindi il numero di elementi caricati nel browser. Il valore predefinito è false. |
| disableIE8Shim | *facoltativo* boolean | Disattiva lo shiv predefinito utilizzato da Livefyre per polilizzare Internet Explorer 8 in modo che gli elementi HTML5 siano supportati. Livefyre utilizza il seguente progetto:  [https://github.com/aFarkas/html5shiv](https://github.com/aFarkas/html5shiv). Il valore predefinito è false.  Nota:  Se questo valore è false, è necessario utilizzare il polifugo di un certo tipo prima che Livefyre Chat venga richiamato per il supporto di Internet Explorer 8. |
| disableThirdPartyAnalytics | *bBoolean facoltativo* | Disattiva i sistemi di analisi di terze parti (Quantserve e Google Analytics) che Livefyre può utilizzare per le misurazioni interne. Il valore predefinito è false. |
| editorCss | *oggetto facoltativo* | Utilizzato per personalizzare lo stile dell’editor dei commenti. È possibile formattare il colore di sfondo del campo dell’editor, nonché il colore del font, le dimensioni e la famiglia del testo che appare all’interno dell’editor.  Ad esempio: `{background: ‘#ccc’, color: ‘red’, font: ’30px “Helvetica Neue”, Helvetica, Arial, Geneva, sans-serif’}` |
| initialNumVisible | *numero intero facoltativo* | Consente di impostare il numero predefinito di commenti visibili nell'app al momento del caricamento. Può essere un numero intero compreso tra 1 e 50. |
| initialNumVisibleLegacy | *numero intero facoltativo* | Consente di impostare il numero predefinito di elementi di contenuto legacy visibili nell'app al momento del caricamento. Può essere un numero intero compreso tra 1 e 50. Se questo parametro non viene specificato, per impostazione predefinita viene utilizzato initialNumVisible.  Ad esempio: Se la raccolta include 100 commenti attivi e 100 legacy, impostare i commenti inizialiNumVisible:10 e initialNumVisibleLegacy:5 per visualizzare 10 commenti attivi (con un pulsante Mostra più) + 5 commenti dell'archivio (con un pulsante Mostra più). |
| maxVisible | *numero intero facoltativo* | Imposta il numero massimo di parti visibili del contenuto di livello principale nell'app chat. Se vengono inserite nuove parti di contenuto, il contenuto nella parte inferiore del flusso verrà rimosso dalla pagina. Se si fa clic sul pulsante Show more (Mostra altro), il parametro viene ignorato e l'utente può visualizzare tutto il contenuto desiderato. (Usate questo parametro per controllare il numero di elementi visualizzati sulla pagina in flussi ad alta velocità.) |
| postToButtons | *array facoltativo* | Utilizzato per configurare quali fornitori vengono visualizzati quando si incorpora l'app Live Blog. Le opzioni disponibili sono due (Twitter), fb (Facebook) e li (LinkedIn). Il valore predefinito è [ due, fb ]. |
| readOnly | *facoltativo* boolean | Disattiva tutte le interattività per la raccolta. Se true, gli utenti non potranno accedere al flusso e non potranno pubblicare contenuti Post, Edit, Reply to o Come. Se true, gli utenti potranno contrassegnare e condividere il contenuto. Il valore predefinito è false. |
| stream | *oggetto facoltativo* | Contiene opzioni per configurare lo streaming dell'app. |
| stream.catchup | *numero intero facoltativo* | Specifica il numero di secondi precedenti al momento in cui il flusso deve essere caricato. Per impostazione predefinita, Livefyre carica 50 parti di contenuto, quindi carica tutto il contenuto inviato tra quelle e l'ora attuale. In casi di utilizzo molto rapidi, il contenuto potrebbe essere pubblicato troppo rapidamente per consentire all'app di "raggiungere" il presente. Utilizzate questa impostazione per definire il numero di secondi precedenti al momento per il quale verrà pubblicato il contenuto (dopo il caricamento iniziale del contenuto). |
| stream.delay | *numero intero facoltativo* | Specifica il numero di secondi tra le richieste di streaming. Utilizzate questo parametro per controllare il flusso di contenuto e ritardare la frequenza con cui il DOM viene aggiornato.  Nota:  Se impostato su un valore troppo elevato, il flusso potrebbe rimanere indietro. |


>[!NOTE]
>
>Durante l'inizializzazione dell'app è possibile passare uno o più `convConfig` oggetti per visualizzare più app sulla stessa pagina. Tenete presente che ulteriori app utilizzano risorse del browser e che le prestazioni potrebbero peggiorare con l'aumento del numero.

## CollectionMetaObject {#c-collectionmeta-object}

L' `CollectionMeta` oggetto è un oggetto JSON che specifica i metadati da memorizzare all'interno della raccolta.

`CollectionMeta` viene sempre codificato prima di essere passato a Livefyre per motivi di sicurezza. Il valore codificato viene passato all' `ConvConfig` oggetto indicato sopra.

>[!NOTE]
>
>È necessario aggiungere codice lato server per codificare l'oggetto `CollectionMeta` JSON. Per ulteriori informazioni, consulta Creazione di token sul lato server.

| Parametro | Tipo | Descrizione |
|--- |--- |--- |
| articleId | *stringa obbligatoria* | Un ID univoco per la raccolta. |
| title | *stringa obbligatoria* | Titolo da applicare alla raccolta. Questo spesso corrisponde al titolo della pagina che visualizza l'app.  Ad esempio: "L'integrazione è così divertente!"  Nota:  La lunghezza massima dei caratteri per il titolo è di 255 caratteri. Il campo title non supporta le entità HTML. Codificare caratteri speciali utilizzando UTF-8. |
| url | *stringa obbligatoria* | L'URL assoluto canonico che si desidera allegare a questa raccolta. Questo URL verrà utilizzato per generare i collegamenti all'app dal contenuto condiviso su Facebook e Twitter, dalle notifiche e-mail e da Livefyre Studio.  Nota:  Livefyre richiede l’uso di un nome di dominio completo; il numero di porta o un callback per risolvere la configurazione locale non è richiesto. Se il test avviene localmente, accertatevi di utilizzare un dominio URL di base valido. Ad esempio: `https://customer.com` è valido, ma non `https://localhost:5995` lo è.) Una volta configurato il server Web locale per accettare un nome di dominio completo, non sono necessari callback o risoluzioni e lo sviluppo locale può procedere come previsto. |
| type | *stringa obbligatoria* | Il tipo Collection. Deve essere livechat. |

L' `CollectionMeta` oggetto può anche contenere il seguente parametro opzionale:

| Parametro | Tipo | Descrizione |
|--- |--- |--- |
| tags | *stringa facoltativa* | Elenco separato da virgole di parole chiave singole o di frasi. Consente di eseguire ricerche nelle raccolte in base ai tag in Studio o con l'API di ricerca.  Nota: Anche se i tag aggiunti tramite Studio possono contenere spazi, i tag immessi tramite l'API non possono. Utilizzate i caratteri di sottolineatura per definire i tag che visualizzeranno gli spazi nell'interfaccia utente. Ad esempio: utilizzate Monday_Quarterback per visualizzare il Quarterback del lunedì in Studio.) |

## Aggiunta di un gestore eventi {#concept_E7C17EFB43F24F1A8572E60C69176C6D}

Per registrare i gestori di eventi, utilizza la chiamata widget.on all'interno della funzione di callback dell'app.

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

Per ulteriori informazioni e per un elenco degli eventi disponibili, consultate Eventi [](../c-app-customizations/c-javascript-events.md#c_javascript_events)JavaScript.
