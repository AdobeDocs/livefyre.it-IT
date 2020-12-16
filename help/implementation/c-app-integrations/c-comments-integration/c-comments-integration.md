---
description: Abilitare i commenti in diretta sulla pagina.
seo-description: Abilitare i commenti in diretta sulla pagina.
seo-title: Commenti
solution: Experience Manager
title: Commenti
uuid: decad9b0-2074-4748-bd77-914008817bfa
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '1475'
ht-degree: 2%

---


# Commenti{#comments}

Abilitare i commenti in diretta sulla pagina. I commenti consentono di sostituire il sistema di commenti predefinito con conversazioni in tempo reale sulla pagina.

## Integrazione {#concept_4093E8BAA96A464BA74D263DA031C0B0}

L&#39;incorporazione dell&#39;app dei commenti segue il processo di incorporazione di un&#39;app di base descritto in Guida introduttiva > Incorporazione di un&#39;app.

### Esempio 

```
<html> 
  <head> 
    <script src="//cdn.livefyre.com/Livefyre.js"> 
    </script> 
  </head> 
<body> 
    <script type="text/javascript"> 
    var networkConfig = { 
      network: 'domainName' 
    }; 
    var convConfig = { 
      siteId: 'siteId', 
      articleId: 'articleId', 
      el: 'livefyre', 
      collectionMeta: 'collectionMeta', 
      checksum: 'checksum' 
    }; 
    
    Livefyre.require(['fyre.conv#3', 'auth'], function(Conv, auth) { 
        new Conv(networkConfig, [convConfig], function(commentsWidget) {}); 
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

Come indicato nella sezione Building CollectionMeta, CollectionMeta è un oggetto JSON codificato. Nell&#39;esempio precedente, l&#39;oggetto JSON ha il formato seguente prima che sia codificato JWT:

```
{ 
"url": "articleUrl",  
"articleId": "articleId",  
"type": "livecomments",  
"title": "articleTitle" 
}
```

## Oggetto NetworkConfig {#c-networkconfig-object}

L&#39;oggetto `NetworkConfig` è un oggetto JSON che personalizza il sistema di autenticazione per gli utenti di rete.
L&#39;oggetto `NetworkConfig` è un oggetto JSON contenente i seguenti parametri:

| Parametro | Tipo | Descrizione |
|---|---|---|
| **authDelegate** | **  requiredobject | Utilizzato per personalizzare il sistema di autenticazione per gli utenti di rete personalizzati. |
| **network** | Stringa *obbligatoria* | Un nome di rete Livefyre. Ad esempio: *nomeutente.fyre.co.* |
| **attachmentDelegate** | *optionalobject*  | Utilizzato per specificare i tipi di allegati multimediali visibili nel flusso App. Per ulteriori informazioni, vedere [Limitazione dei supporti](/help/implementation/c-app-customizations/c-restrict-media.md#c_restrict_media). |
| **strings** | *optionalobject*  | Utilizzato per personalizzare le stringhe di testo degli elementi HTML in una qualsiasi delle app core Livefyre. Per ulteriori informazioni, vedere [Personalizzazioni stringa](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md). |

## Oggetto ConvConfig {#c-convconfig-object}

L&#39;oggetto `convConfig` è un oggetto JSON utilizzato per specificare il contenuto di cui l&#39;app Livefyre esegue il rendering sulla pagina.

>[!NOTE]
>
>I parametri dell&#39;oggetto `convConfig` elencati qui non si applicano all&#39;app Reviews. Per informazioni sull&#39;integrazione dell&#39;app Reviews tramite l&#39;oggetto `convConfig`, consultate Integrazione delle recensioni.

L&#39;oggetto `ConvConfig` contiene i seguenti parametri obbligatori:

| Parametro | Tipo | Descrizione |
|--- |--- |--- |
| **articleId** | ** requiredstring | Identifica in modo univoco una raccolta all&#39;interno del sito. In genere corrisponde a una chiave primaria del database o a un ID Post all’interno del CMS. Ad esempio: &quot;post-42&quot;. Limite di 255 caratteri.  Nota:  Se utilizzate l&#39;URL dell&#39;articolo come articleId, accertatevi che la stringa sia codificata MD5 o SHA-1. |
| **authPageReload** | **  optionalboolean | Si applica all&#39;app Commenti: Consente di controllare se il commento di un utente viene memorizzato localmente durante il processo di autenticazione. Se è true, se un utente immette un commento e quindi accede all&#39;app, il commento viene memorizzato localmente e viene reinserito nel campo del contenuto dopo l&#39;accesso e l&#39;aggiornamento della pagina. Se false, il contenuto immesso verrà cancellato durante il processo di accesso e dovrà essere ridigitato. |
| **collectionMeta** | ** requiredstring | Metadati codificati JWT per la raccolta. Per ulteriori informazioni, vedere [CollectionMeta](#c_collectionmeta_object) Oggetto. |
| **el** | ** requiredstring | L&#39;ID di un elemento DOM a cui verrà eseguito il rendering del flusso di contenuto. |
| **siteId** | ** requiredstring | L&#39;ID Livefyre fornito per il sito Web o l&#39;applicazione a cui appartiene la raccolta. Ad esempio: &quot;303617&quot;. |

>[!NOTE]
>
>Il parametro `app` non è richiesto per l&#39;implementazione di un&#39;app di commenti.

L&#39;oggetto `ConvConfig` può contenere anche i seguenti parametri facoltativi:

| Parametro | Tipo | Descrizione |
|--- |--- |--- |
| **actionButtons** | ** optionalarray | Un array di pulsanti di azione personalizzati da aggiungere a un contenuto accanto ai pulsanti Condividi e Contrassegna. Per ulteriori informazioni, consultate Aggiunta di pulsanti personalizzati. |
| **animazioni** | ** optionalboolean | Definisce se le animazioni verranno eseguite nell&#39;app Livefyre. Impostate su false per disabilitare le animazioni. Il valore predefinito è true. |
| **anonimoFlaggingEnabled** | ** optionalboolean | Definisce se gli utenti ospiti dispongono dell’opzione per contrassegnare il contenuto. Il valore predefinito è true. |
| **browserType** | ** optionalstring | Definisce il dispositivo per il quale deve essere generato il contenuto di visualizzazione. Ciò causerà la modifica del CSS e di alcune funzionalità per adattarlo al tipo di dispositivo di input. Le opzioni sono desktop, mobile o tablet. Se lasciato vuoto, per impostazione predefinita verrà utilizzata la determinazione di Google Agent per il formato di visualizzazione. |
| **checksum** | ** consigliendedstring | Identifica lo stato corrente di CollectionMeta. Modificando questo valore, Livefyre aggiornerà i dati sul server con i nuovi valori in CollectionMeta. |
| **datetimeFormat** | *funzione oggetto*  optionalstring | Specifica il formato data/ora del contenuto in streaming. Per ulteriori informazioni, vedere Personalizzazione dei timbri data e ora. |
| **disableAvatars** | ** optionalboolean | Impedisce il rendering degli avatar nel flusso App e riduce quindi il numero di elementi caricati nel browser. Il valore predefinito è false. |
| **disableIE8Shim** | ** optionalboolean | Disattiva lo shiv predefinito utilizzato da Livefyre per polilizzare Internet Explorer 8 in modo che gli elementi HTML5 siano supportati. Livefyre utilizza il seguente progetto:  [https://github.com/aFarkas/html5shiv](https://github.com/aFarkas/html5shiv) . Il valore predefinito è false.  Nota:  Se questo valore è false, è necessario utilizzare il polifugo di un certo tipo prima che Livefyre Chat venga richiamato per il supporto di Internet Explorer 8. |
| **disableThirdPartyAnalytics** | ** optionalboolean | Disattiva i sistemi di analisi di terze parti (Quantserve e Google Analytics) che Livefyre può utilizzare per le misurazioni interne. Il valore predefinito è false. |
| **editorCss** | *optionalobject*  | Utilizzato per personalizzare lo stile dell’editor dei commenti. È possibile formattare il colore di sfondo del campo dell’editor, nonché il colore del font, le dimensioni e la famiglia del testo che appare all’interno dell’editor.  Ad esempio: `{background: ‘#ccc’, color: ‘red’, font: ’30px “Helvetica Neue”, Helvetica, Arial, Geneva, sans-serif’}` |
| **initialNumVisible** | ** optionalinteger | Consente di impostare il numero predefinito di commenti visibili nell&#39;app al momento del caricamento. Può essere un numero intero compreso tra 1 e 50. |
| **initialNumVisibleLegacy** | ** optionalinteger | Consente di impostare il numero predefinito di elementi di contenuto legacy visibili nell&#39;app al momento del caricamento. Può essere un numero intero compreso tra 1 e 50. Se questo parametro non viene specificato, per impostazione predefinita viene utilizzato initialNumVisible.  Ad esempio: Se la raccolta include 100 commenti attivi e 100 legacy, impostare i commenti inizialiNumVisible:10 e initialNumVisibleLegacy:5 per visualizzare 10 commenti attivi (con un pulsante Mostra più) + 5 commenti dell&#39;archivio (con un pulsante Mostra più). |
| **maxVisible** | ** optionalinteger | Imposta il numero massimo di parti visibili del contenuto di livello principale nell&#39;app Chat. Se vengono inserite nuove parti di contenuto, il contenuto nella parte inferiore del flusso verrà rimosso dalla pagina. Se si fa clic sul pulsante Show more (Mostra altro), il parametro viene ignorato e l&#39;utente può visualizzare tutto il contenuto desiderato. (Usate questo parametro per controllare il numero di elementi che appaiono sulla pagina in flussi ad alta velocità.) |
| **postToButtons** | ** optionalarray | Utilizzato per configurare quali fornitori vengono visualizzati quando si incorpora l&#39;app Live Blog. Le opzioni disponibili sono due (Twitter), fb (Facebook) e li (LinkedIn). Il valore predefinito è [ tw, fb ]. |
| **readOnly** | ** optionalboolean | Disattiva tutte le interattività per la raccolta. Se true, gli utenti non potranno accedere al flusso e non potranno pubblicare contenuti Post, Edit, Reply to o Come. Se true, gli utenti potranno contrassegnare e condividere il contenuto. Il valore predefinito è false. |
| **stream** | *optionalobject*  | Contiene opzioni per configurare lo streaming dell&#39;app. |
| **stream.catchup** | ** optionalinteger | Specifica il numero di secondi precedenti al momento in cui il flusso deve essere caricato. Per impostazione predefinita, Livefyre carica 50 parti di contenuto, quindi carica tutto il contenuto inviato tra quelle e l&#39;ora attuale. In casi di utilizzo molto rapidi, il contenuto potrebbe essere pubblicato troppo rapidamente per consentire all&#39;app di &quot;raggiungere&quot; il presente. Utilizzate questa impostazione per definire il numero di secondi precedenti al momento per il quale verrà pubblicato il contenuto (dopo il caricamento iniziale del contenuto). |
| **stream.delay** | ** optionalinteger | Specifica il numero di secondi tra le richieste di streaming. Utilizzate questo parametro per controllare il flusso di contenuto e ritardare la frequenza con cui il DOM viene aggiornato.  Nota:  Se impostato su un valore troppo elevato, il flusso potrebbe rimanere indietro. |


>[!NOTE]
>
>Durante l&#39;inizializzazione dell&#39;app è possibile passare uno o più oggetti `convConfig` per visualizzare più app sulla stessa pagina. Tenete presente che ulteriori app utilizzano risorse del browser e che le prestazioni potrebbero peggiorare con l&#39;aumento del numero.

## CollectionMeta Object {#c-collectionmeta-object}

L&#39;oggetto `CollectionMeta` è un oggetto JSON che specifica i metadati da memorizzare all&#39;interno della raccolta.

`CollectionMeta` viene sempre codificato prima di essere passato a Livefyre per motivi di sicurezza. Il valore codificato viene passato all&#39;oggetto `ConvConfig` indicato sopra.

>[!NOTE]
>
>È necessario aggiungere codice lato server per codificare l&#39;oggetto JSON `CollectionMeta`. Per ulteriori informazioni, consulta Creazione di token sul lato server.

| Parametro | Tipo | Descrizione |
|--- |--- |--- |
| **articleId** | ** requiredstring | Un ID univoco per la raccolta. |
| **title** | ** requiredstring | Titolo da applicare alla raccolta. Questo spesso corrisponde al titolo della pagina che visualizza l&#39;app.  Ad esempio: &quot;L&#39;integrazione è così divertente!&quot; <br>**Nota:**  la lunghezza massima dei caratteri per il titolo è di 255 caratteri. Il campo title non supporta le entità HTML. Codificare caratteri speciali utilizzando UTF-8. |
| **url** | ** requiredstring | L&#39;URL assoluto canonico che si desidera allegare a questa raccolta. Questo URL verrà utilizzato per generare i collegamenti all&#39;app dal contenuto condiviso su Facebook e Twitter, dalle notifiche e-mail e da Livefyre Studio.  <br>**** NoteLivefyre richiede l’uso di un nome di dominio completo; il numero di porta o un callback per risolvere la configurazione locale non è richiesto. Se il test avviene localmente, accertatevi di utilizzare un dominio URL di base valido. <br>Ad esempio:  `https://customer.com` è valido, mentre non  `https://localhost:5995` lo è. Una volta configurato il server Web locale per accettare un nome di dominio completo, non sono necessari callback o risoluzioni e lo sviluppo locale può procedere come previsto. |
| **type** | ** requiredstring | Il tipo Collection. Deve essere `livechat`. |

L&#39;oggetto `CollectionMeta` può contenere anche il seguente parametro opzionale:

| Parametro | Tipo | Descrizione |
|---|---|---|
| **tags** | ** optionalstring | Elenco separato da virgole di parole chiave singole o di frasi. Consente di eseguire ricerche nelle raccolte in base ai tag in Studio o con l&#39;API di ricerca. <br> **Nota:** Anche se i tag aggiunti tramite Studio possono contenere spazi, i tag immessi tramite l&#39;API non possono. Utilizzate i caratteri di sottolineatura per definire i tag che visualizzeranno gli spazi nell&#39;interfaccia utente. Ad esempio: utilizzare `Monday_Quarterback` per visualizzare il Quarterback del lunedì in Studio. |

## Aggiunta di un gestore eventi {#concept_06D8B811C98B4CC6B38C6340EBA176E5}

Per registrare i gestori di eventi, utilizza la chiamata widget.on all&#39;interno della funzione di callback dell&#39;app.

### Ad esempio

```
Livefyre.require(['fyre.conv#3'], function(Conv) { 
   new Conv(networkConfig, [convConfig], function(widget) { 
      widget.on('<strong><eventName></strong>', function (data) { 
         // Do something, perhaps using data 
      }); 
   }); 
});
```
