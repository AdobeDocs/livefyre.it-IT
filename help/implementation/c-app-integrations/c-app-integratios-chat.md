---
description: Aggiunta di una live chat alla pagina.
title: Chat
exl-id: f383bf19-0ff1-42ca-9b32-209a22679ad2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '1429'
ht-degree: 2%

---

# Chat{#chat}

Aggiunta di una live chat alla pagina.

La chat consente al tuo pubblico di partecipare a conversazioni in tempo reale che circondano gli eventi live. Il contenuto viene visualizzato come un flusso continuo, incoraggiando una rapida partecipazione al dialogo in corso.

Versione corrente: La chat utilizza `fyre.conv v3.0.0.`

## Integrazione {#concept_0A99792A7E89403F95D082D52D600F17}

L&#39;incorporazione dell&#39;app Chat segue il processo di incorporazione di un&#39;app core descritto in Guida introduttiva > [Incorporazione di un&#39;app](../c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md#using-livefyre-js-create-customize-apps).

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

Come indicato nella sezione [CollectionMeta Token](../c-getting-started/c-implementation-process/c-collectionmeta-tokent.md#collectionmeta-tokent), CollectionMeta è un oggetto JSON codificato. Nell&#39;esempio precedente, l&#39;oggetto JSON assume il formato seguente prima della codifica JWT:

```
{ 
"url": "https://dev.livefyre.com/articles/test.html",  
"articleId": "1",  
"type": "livechat",  
"title": "Title 1" 
}
```

## Oggetto NetworkConfig {#c-networkconfig-object}

L&#39;oggetto `NetworkConfig` è un oggetto JSON che personalizza il sistema di autenticazione per gli utenti di rete.

L&#39;oggetto `NetworkConfig` è un oggetto JSON contenente i seguenti parametri:

| Parametro | Tipo | Descrizione |
|---|---|---|
| authDelegate | ** requiredobject | Utilizzato per personalizzare il sistema di autenticazione per gli utenti di rete personalizzati. |
| rete | ** requiredstring | Nome di rete fornito da Livefyre. Ad esempio: *nome.file.co.* |
| attachmentDelegate | Oggetto | Utilizzato per specificare i tipi di allegati multimediali visibili nel flusso di app. Per ulteriori informazioni, consulta [Limitazione di Media](../c-app-customizations/c-restrict-media.md#c_restrict_media). |
| stringhe | ** optionalobject | Utilizzato per personalizzare le stringhe di testo degli elementi HTML in una qualsiasi delle app core Livefyre. Per ulteriori informazioni, consulta [Personalizzazioni di stringhe](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md). |

## Oggetto ConvConfig {#c-convconfig-object}

L’oggetto `convConfig` è un oggetto JSON utilizzato per specificare il contenuto di cui l’app Livefyre esegue il rendering sulla pagina.

>[!NOTE]
>
>I parametri dell&#39;oggetto `convConfig` elencati qui non si applicano all&#39;app Reviews. Per informazioni sull&#39;integrazione dell&#39;app Reviews tramite l&#39;oggetto `convConfig`, consulta Integrazione delle revisioni.

L&#39;oggetto `ConvConfig` contiene i seguenti parametri obbligatori:

| Parametro | Tipo | Descrizione |
|--- |--- |--- |
| articleId | ** requiredstring | Identifica in modo univoco una raccolta all&#39;interno del sito. Di solito corrisponde a una chiave primaria del database o a un ID post all&#39;interno del CMS. Ad esempio: &quot;post-42&quot;. Limite di 255 caratteri.  Nota:  Se utilizzi l’URL dell’articolo come articleId, assicurati che la stringa sia codificata in MD5 o SHA-1. |
| collectionMeta | ** requiredstring | Metadati codificati JWT sulla raccolta. Per ulteriori informazioni, consulta [CollectionMeta Object](../c-getting-started/c-implementation-process/c-collectionmeta-tokent.md#collectionmeta-tokent) . |
| el | ** requiredstring | ID di un elemento DOM a cui verrà eseguito il rendering del flusso di contenuto. |
| siteId | ** requiredstring | ID Livefyre fornito per il sito web o l&#39;applicazione a cui appartiene la raccolta. Ad esempio: &quot;303617&quot;. |

>[!NOTE]
>
>Il parametro `app` non è necessario per l’implementazione di un’app Commenti .

L&#39;oggetto `ConvConfig` può contenere anche i seguenti parametri facoltativi:

| Parametro | Tipo | Descrizione |
|--- |--- |--- |
| actionButtons | *array facoltativo*  | Matrice di pulsanti di azione personalizzati da aggiungere a un contenuto accanto ai pulsanti Condividi e Contrassegna . Per ulteriori informazioni, vedere Aggiunta di pulsanti personalizzati. |
| animazioni | ** optionalboolean | Definisce se le animazioni verranno eseguite nell’app Livefyre. Imposta su false per disabilitare le animazioni. Predefinito su true. |
| anonymousFlaggingEnabled | ** optionalboolean | Definisce se gli utenti ospiti possono contrassegnare il contenuto. Il valore predefinito è true. |
| browserType | ** optionalstring | Definisce il dispositivo per il quale deve essere generato il contenuto visualizzato. Questo comporterà la modifica del CSS e di alcune funzionalità per adattarlo al tipo di dispositivo di input. Le opzioni sono desktop, dispositivi mobili o tablet. Se lasciato vuoto, verrà impostato automaticamente sulla determinazione di Google Agent per il formato di visualizzazione. |
| checksum | ** recommendationsstring (consigliato) | Identifica lo stato corrente di CollectionMeta. La modifica di questo valore comporterà l’aggiornamento dei dati sul server da parte di Livefyre con i nuovi valori in CollectionMeta. |
| datetimeFormat | *Funzione oggetto* optionalstring | Specifica il formato datetime del contenuto in streaming. Per ulteriori informazioni, vedere Personalizzazione di timestamp e timestamp. |
| disableAvatars | ** optionalboolean | Impedisce il rendering degli avatar nel flusso di app e quindi riduce il numero di elementi caricati nel browser. Il valore predefinito è false. |
| disableIE8Shim | ** optionalboolean | Disattiva lo shiv predefinito utilizzato da Livefyre per il polyfill di Internet Explorer 8 in modo che gli elementi HTML5 siano supportati. Livefyre utilizza il seguente progetto:  [https://github.com/aFarkas/html5shiv](https://github.com/aFarkas/html5shiv). Il valore predefinito è false.  Nota:  Se questo valore è false, è necessario utilizzare un tipo di polyfill prima che Livefyre Chat venga richiamato per il supporto di Internet Explorer 8. |
| disableThirdPartyAnalytics | ** optionalbBoolean | Disattiva i sistemi di analisi di terze parti (Quantserve e Google Analytics) che Livefyre può utilizzare per le misurazioni interne. Il valore predefinito è false. |
| editorCss | ** optionalobject | Utilizzato per personalizzare lo stile dell’editor dei commenti. È possibile formattare il colore di sfondo del campo dell’editor, nonché il colore del font, le dimensioni e la famiglia del testo visualizzato all’interno dell’editor.  Ad esempio: `{background: ‘#ccc’, color: ‘red’, font: ’30px “Helvetica Neue”, Helvetica, Arial, Geneva, sans-serif’}` |
| initialNumVisible | ** numero intero facoltativo | Consente di impostare il numero predefinito di commenti visibili nell’app al momento del caricamento. Può essere un numero intero compreso tra 1 e 50. |
| initialNumVisibleLegacy | ** numero intero facoltativo | Consente di impostare il numero predefinito di elementi di contenuto legacy visibili nell’app al momento del caricamento. Può essere un numero intero compreso tra 1 e 50. Se questo parametro non viene specificato, viene impostato il valore predefinito initialNumVisible.  Ad esempio: Se la raccolta include 100 commenti attivi e 100 legacy, impostare initalNumVisible:10 e initialNumVisibleLegacy:5 per visualizzare 10 commenti attivi (con un pulsante Mostra altro) + 5 commenti di archivio (con un pulsante Mostra altro). |
| maxVisible | ** numero intero facoltativo | Imposta il numero massimo di parti visibili del contenuto di primo livello nell&#39;app Chat. Se vengono inserite nuove parti di contenuto, il contenuto nella parte inferiore del flusso verrà rimosso dalla pagina. Se si fa clic sul pulsante Show more (Mostra altro), il parametro viene ignorato e l’utente può mostrare il contenuto desiderato. (Usa questo parametro per controllare il numero di elementi visualizzati sulla pagina in flussi ad alta velocità.) |
| postToButtons | *array facoltativo*  | Utilizzato per configurare quali provider vengono visualizzati quando si incorpora l&#39;app Live Blog. Le opzioni disponibili sono due (Twitter), fb (Facebook) e li (LinkedIn). Il valore predefinito è [ tw , fb ]. |
| readOnly | ** optionalboolean | Disattiva tutte le interattività per la raccolta. Se true, gli utenti non saranno in grado di accedere al flusso e non potranno pubblicare, modificare, rispondere o mettere ’Mi piace’ al contenuto. Se true, gli utenti potranno contrassegnare e condividere il contenuto. Il valore predefinito è false. |
| flusso | ** optionalobject | Contiene le opzioni per configurare lo streaming dell’app. |
| stream.catchup | ** numero intero facoltativo | Specifica il numero di secondi precedenti al momento in cui il flusso deve essere caricato. Per impostazione predefinita, Livefyre carica 50 parti di contenuto, quindi carica tutti i contenuti inviati tra quelle e l’ora attuale. In casi d’uso molto rapidi, il contenuto può essere pubblicato troppo rapidamente per consentire all’app di &quot;raggiungere&quot; il presente. Utilizza questa impostazione per definire il numero di secondi precedenti al momento per i quali verrà pubblicato il contenuto (dopo il caricamento iniziale del contenuto). |
| stream.delay | ** numero intero facoltativo | Specifica il numero di secondi tra le richieste di streaming. Usa questo parametro per controllare il flusso di contenuto e ritardare la frequenza con cui viene aggiornato il DOM.  Nota:  Se impostato troppo grande, il flusso potrebbe cadere indietro. |


>[!NOTE]
>
>Puoi passare uno o più oggetti `convConfig` durante l&#39;inizializzazione dell&#39;app per visualizzare più app sulla stessa pagina. Tieni presente che le app aggiuntive utilizzano risorse del browser e le prestazioni possono degradarsi man mano che il numero aumenta.

## Oggetto CollectionMeta {#c-collectionmeta-object}

L&#39;oggetto `CollectionMeta` è un oggetto JSON che specifica i metadati da memorizzare all&#39;interno della raccolta.

`CollectionMeta` viene sempre codificato prima di essere passato a Livefyre per motivi di sicurezza. Il valore codificato viene passato nell&#39;oggetto `ConvConfig` mostrato sopra.

>[!NOTE]
>
>Devi aggiungere codice lato server per codificare l’oggetto JSON `CollectionMeta` . Per ulteriori informazioni, consulta Generazione di token lato server .

| Parametro | Tipo | Descrizione |
|--- |--- |--- |
| articleId | ** requiredstring | Un ID univoco per la raccolta. |
| title | ** requiredstring | Titolo da applicare alla Raccolta. Questo corrisponde spesso al titolo della pagina che visualizza l’app.  Ad esempio: &quot;L&#39;integrazione è così divertente!&quot;  Nota:  La lunghezza massima dei caratteri per il titolo è di 255 caratteri. Il campo titolo non supporta le entità HTML. Codifica caratteri speciali utilizzando UTF-8. |
| url | ** requiredstring | URL assoluto canonico da allegare a questa raccolta. Questo URL verrà utilizzato per generare collegamenti all’app dal contenuto condiviso su Facebook e Twitter, dalle notifiche e-mail e da Livefyre Studio.  Nota:  Livefyre richiede l’uso di un nome di dominio completo; il numero di porta o un callback per risolvere la configurazione locale non è necessario. Se esegui il test localmente, assicurati di utilizzare un dominio URL di base valido. (Ad esempio: `https://customer.com` è valido, mentre `https://localhost:5995` non lo è.) Una volta configurato il server Web locale per accettare un nome di dominio completo, non sono necessari callback o risoluzioni e lo sviluppo locale può procedere come previsto. |
| type | ** requiredstring | Tipo di raccolta. Deve essere in livechat . |

L&#39;oggetto `CollectionMeta` può anche contenere il seguente parametro opzionale:

| Parametro | Tipo | Descrizione |
|--- |--- |--- |
| tag | ** optionalstring | Elenco separato da virgole di singole parole chiave o frasi. Cerca raccolte per tag in Studio o con l’API di ricerca.  Nota: Anche se i tag aggiunti tramite Studio possono contenere spazi, i tag immessi tramite l’API non possono. Utilizza i caratteri di sottolineatura per definire i tag che visualizzano gli spazi nell’interfaccia utente. (Ad esempio: utilizzare il parametro Monday_Quarterback per visualizzare il valore del trimestre del lunedì in Studio.) |

## Aggiunta di un gestore eventi {#concept_E7C17EFB43F24F1A8572E60C69176C6D}

Per registrare i gestori di eventi, utilizza la chiamata widget.on all&#39;interno della funzione di callback dell&#39;app.

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

Per ulteriori informazioni e per un elenco degli eventi disponibili, consulta [Eventi JavaScript](../c-app-customizations/c-javascript-events.md#c_javascript_events).
