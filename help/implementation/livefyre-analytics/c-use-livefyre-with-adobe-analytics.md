---
description: nulle
seo-description: nulle
seo-title: Utilizza Livefyre con Adobe Analytics e Dynamic Tag Manager (DTM) lk xavvn
  vefyre con Adobe Analytics e Dynamic Tag Manager (DTM)
uuid: 9 a 1 c 25 c 0-c 474-46 ff -82 ac-e 89357007 c 7 f
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Utilizzo di Livefyre con Adobe Analytics e Dynamic Tag Manager (DTM){#use-livefyre-with-adobe-analytics-and-dynamic-tag-manager-dtm}

Configurate Adobe Analytics e Dynamic Tag Manager (DTM) per raccogliere i dati per Livefyre Apps.

## Passaggio 1: Configurare gli eventi in Adobe Analytics {#section_iks_kgd_4cb}

Mappatura degli eventi di Livefyre su uno o più eventi di successo personalizzati in Adobe Analytics Report Suite Manager.

Per ulteriori informazioni su Gestore suite di rapporti, vedi [Report Suite Manager](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html).

1. Accedete ad Adobe Analytics come utente amministratore.
1. Apri Adobe Analytics Admin Report Suite Manager.
1. Create una nuova suite di rapporti o sceglietene una esistente.
1. Modifica la suite di rapporti facendo clic sulla suite di rapporti per modificarla, quindi passa **[!UICONTROL Edit Settings > Conversion > Success Events]**a.
1. Mappate gli eventi Livefyre su uno o più eventi di successo personalizzati.

## Passaggio 2: Configurare le variabili di conversione

Mappatura delle variabili di conversione di Livefyre (evars) sulle variabili di conversione in Adobe Analytics Admin Report Suite Manager. Le variabili di conversione si comportano come una funzione di ordinamento per determinare la modalità di identificazione dei dati raccolti dagli eventi Livefyre.

1. Nel clic Suite di rapporti **[!UICONTROL Edit Settings > Conversion > Conversion Variables]**.
1. Scegli le variabili di conversione personalizzate (evars) da usare e mapparle sulle variabili di conversione di Livefyre. Per mappare una variabile di conversione Livefyre in una variabile di conversione personalizzata:
* Attivare la variabile di conversione
* Assegnare un nome alla variabile di conversione
* Assegna alla variabile di conversione un tipo
1. Salva le variabili di conversione personalizzate.

## Passaggio 3: Utilizza Gestione dinamica dei tag per aggiungere la tua suite di rapporti con eventi Livefyre {#section_t15_2hd_4cb}

Aggiungi Adobe Analytics a DTM per far funzionare Analytics. A tal fine, crea una nuova proprietà e uno strumento e aggiungi alla proprietà la nuova suite di rapporti con eventi Livefyre. Per ulteriori informazioni su Gestione dinamica dei tag, consulta [Gestione dinamica dei tag](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html).

Non è necessario eseguire questo passaggio se disponete già di una proprietà o di uno strumento configurato per la suite di rapporti impostata con eventi Livefyre.

1. In Gestione dinamica dei tag, crea o modifica una proprietà esistente.
1. Create o modificate uno strumento Adobe Analytics esistente.
1. Se uno strumento Adobe Analytics esistente non esiste, fate clic sul **[!UICONTROL Add a Tool]** pulsante.
Impostate i seguenti parametri per lo strumento:
* Impostato **[!UICONTROL Tool Type]** su **[!UICONTROL Adobe Analytics]**.
* Abilita **[!UICONTROL Automatic Configuration]**.
* Abilita **[!UICONTROL Authenticate via Marketing Cloud]**.
1. Aggiungi o conferma il nome della suite di rapporti con gli eventi Livefyre al **[!UICONTROL Report Suites]** campo.

## Passaggio 4: Impostare una regola di caricamento pagina per impostare la gestione di Analytics {#section_jfj_j3d_4cb}

Configurate una regola di caricamento pagina per inserire tutti i dati. La regola di caricamento pagina consente di inserire javascript personalizzati nella regola che registra l'evento quando la pagina viene caricata.

>[!NOTE]
>
>Non utilizzate regole basate su eventi o regole di chiamata diretta.

1. In Gestione dinamica dei tag, seleziona **[!UICONTROL Rules]** scheda.
1. Fate clic **[!UICONTROL Page Load Rules]**su.
1. Fate clic **[!UICONTROL Create New Rule]** sul pulsante.
1. Aprite la **[!UICONTROL Conditions]** sezione facendo clic sul **[!UICONTROL Plus]** pulsante.
1. Attivate la regola. Scegliete **[!UICONTROL DOM Ready]** o **[!UICONTROL Onload]** attivate i tipi se desiderate ritardare o implementare la regola in modo asincrono.
1. (Facoltativo) Aggiungete parametri aggiuntivi per limitare le pagine che mostrano Livefyre Apps. Per ulteriori informazioni sulle opzioni di configurazione aggiuntive, consulta [Gestione dinamica dei tag](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html).
1. Sotto **[!UICONTROL Javascript/ Third Party Tags]**, fate clic sulla **[!UICONTROL Non-sequential]** scheda, quindi fate clic **[!UICONTROL Add New Script]**su.
1. Selezionare **[!UICONTROL Sequential HTML]** il tipo di script.
1. Aggiungete lo script seguente nell'editor di codice e fate clic **[!UICONTROL Save Code]**su.
Lo script seguente chiama la `livefyre_analytics` regola di chiamata diretta dopo il caricamento di Livefyre javascript. Il seguente esempio di script controlla ogni 400 ms per vedere se `livefyre.analytics` si trova sulla pagina. Una volta caricata la pagina, livefyre. analytics invia informazioni di tracciamento.

```
/** 
* Poll for Livefyre.analytics object to exist since it gets loaded via the 
* Livefyre.js JavaScript file. Depending on the timing, this could already 
* exist or need a little time. 
*/ 
function pollForAnalytics() {  
 if (Livefyre.analytics) { 
   _satellite.track('livefyre_analytics'); 
     return true; 
   } 
   setTimeout(pollForAnalytics, 400); 
} 
  
setTimeout(pollForAnalytics, 400);
```

1. Fate clic **[!UICONTROL Save Code]**su.
1. Fate clic **[!UICONTROL Save Rule]**su.

## Passaggio 5: Creare una regola di chiamata diretta per creare la configurazione mappatura di Adobe Analytics per Livefyre {#section_gvp_b1g_pdb}

Esistono altri modi per implementare Livefyre con Gestione dinamica dei tag utilizzando gli eventi personalizzati, i campi dell'interfaccia utente Adobe Analytics all'interno di DTM e gli elementi di dati. Questo documento utilizza Javascript personalizzato per eseguire lo stesso effetto.

1. In Gestione dinamica dei tag seleziona la **scheda Regole** , quindi fai clic su **Regole chiamate dirette**.
1. Fate clic sul pulsante **Crea nuova regola** .
1. Denominate la nuova regola **Livefyre Analytics**.
1. Espande l' **area** di configurazione delle condizioni.
1. Nel campo **Stringa** , immettete `livefyre_analytics`.
1. Espandere la sezione Tag Javascript/3 rd Party e fare clic sul pulsante **Aggiungi nuovo script** .
1. Immettete **la configurazione di Livefyre Analytics** nella **casella** di testo Nome tag.
1. Selezionare **Javascript non sequenziale**.
1. Inserite il seguente codice di configurazione Livefyre nell'editor di codice e fate clic sul pulsante **Salva codice** .

   ```
   var s = _satellite.getToolsByType('sc')[0].getS(); 
   
   var evarMap = {  
     appId: 'eVar81',  
     appType: 'eVar82' 
   }; 
   
   var eventMap = { 
     FlagCancel: 'event82',  
     FlagClick: 'event82',  
     FlagDisagree: 'event82',  
     FlagOffensive: 'event82',  
     FlagOffTopic: 'event82',  
     FlagSpam: 'event82',  
     Like: 'event82', 
     Load: 'event81',  
     RequestMore: 'event82',  
     ShareButtonClick: 'event82',  
     ShareFacebook: 'event82',  
     ShareOnPostClick: 'event82',  
     ShareTwitter: 'event82',  
     ShareURL: 'event82',  
     SortStream: 'event82',  
     TwitterLikeClick: 'event82', 
     TwitterReplyClick: 'event82',  
     TwitterRetweetClick: 'event82',  
     TwitterUserFollow: 'event82' 
   }; 
   
    function trackLivefyreEvent(data) {  
     var event = eventMap[data.type]; 
     console.log('Track:', data.type, event); 
   
     if (!event) { 
       console.warn(data.type, 'is not mapped   to an event in AA');  
       return; 
     } 
     var vars = ['events'];  
     switch (event) { 
       case 'event82': s.eVar83 = data.type;  
         vars.push('eVar83');  
         break; 
       default: 
     } 
       ['generator', 'evars'].forEach(function (type) {  
       var obj = data[type]; 
       for (var d in obj) { 
         if (obj.hasOwnProperty(d) && evarMap[d]) {  
           s[evarMap[d]] = obj[d];  
           vars.push(evarMap[d]); 
         } 
       } 
     }); 
     s.linkTrackVars = vars.join(',');  
     s.linkTrackEvents = event;  
     s.events = event; 
   
     console.log('linkTrackVars:',  s.linkTrackVars);  
     console.log('linkTrackEvents:',  s.linkTrackEvents);  
     console.log('events:', s.events); 
     s.tl(); 
    } 
   ]
   
   /** 
   ```

* Aggiunge un gestore di analisi per tutti gli eventi di analisi di Livefyre. Per ogni evento, imposta i dati su un oggetto globale e quindi invia l'evento.

   ```
   */ 
    function addAnalyticsHandler() {  
      Livefyre.analytics.addHandler(function (events) { 
        (events || []).forEach(function (data) {  
          console.log('Event handled:', data.type);  
          trackLivefyreEvent(data); 
        }); 
      }); 
    } 
    addAnalyticsHandler(); 
   
```
1. Click on **Save Rule**.

## Step 6: Approve changes for Page Load Rule {#section_pxc_11t_ycb}

1. Go to **[!UICONTROL Approvals]** tab.
1. Click **[!UICONTROL Approve]**.
1. Click **[!UICONTROL Yes, approve]** to confirm your approval.
1. Go to **[!UICONTROL Overview > Publish Queue]**.
1. Select the Rule to publish.
1. Click **[!UICONTROL Publish Selected]**.
1. Click **[!UICONTROL Publish]** to confirm that you want to publish.

## Script {#section_xkb_vft_mcb}

The following sample code maps the specific eVars to available Livefyre eVars. The Livefyre conversion variable ( `eVar`) name (for example, `appId`) maps to the name you set up in the Report Suite Manager (for example, `eVar81`). Change the `eVar` names in this script to the custom conversion variables.
```

var s =_ satellite. gettoolsbytype`('sc')[0]`. GET ();
var evarmap = {appid: ' Evar 81 ',
apptype: ' Evar 82 '};

```
The following sample code maps the specific events you set up in the Report Suite Manager with available Livefyre events. In this example, `event82` is set up as any user interaction event without differentiating which kind of user interaction event (for example, liking or sharing content). This is an efficient way to record all user interaction information in a block. You can also map the events in the DTM Analytics UI with Data Element referencing.
```

var eventmap = {flagcancel: ' event 82 ',\
Flagclick: ' event 82 ',\
Flagd: ' event 82 ',\
Flagoffensive: ' event 82 ',\
Flagofftopic: ' event 82 ',\
Flagspam: ' event 82 ',\
Come: ' event 82 ',
Load: ' event 81 ',\
Requestmore: ' event 82 ',\
Sharebuttonclick: ' event 82 ',\
Sharefacebook: ' event 82 ',\
Shareonpostclick: ' event 82 ',\
Sharetwitter: ' event 82 ',\
Shareurl: ' event 82 ',\
Sortstream: ' event 82 ',\
Twitterlikeclick: ' event 82 ',
twitterreplyclick: ' event 82 ',\
Twitterretweetclick: ' event 82 ',\
Twitteruserfollow: ' event 82 '};

```
The following sample states that if there isn't an event in this list, don't do anything. You do not need to modify this section of code.
```

function tracklivefyreevent (data) {\
var event = eventmapdata[. type];
console. log ('Track: ', data. type, event);

if (! event) {console.
alert (data. type,'non è mappato a un evento in AA ');\
return;}

```
The following code differentiates the event types that `event82` records. The conversion variable, `eVar83` records the type of user interaction, and the script sets up `eVar83` to separate the user interaction data by type. So `eVar83` allows you to break out the recorded data into specific types of user interactions.
```

var vars = ['events '];\
switch (event) {case'event
82 ': s. evar 83 = data. type;\
vars. push ('evar 83 ');\
break;
default:}

[' generator ','evars ']. foreach (function (type) {\
var obj = datatype[];
for (var d in obj) {if
(obj. hasownproperty (d) & & evarmapd[]) {\
s [evarmapd[]] = objd[];\
vars. push (evarmapd[]);}}});

s. linktrackvars = vars. join (',');\
s. linktrackevents = event;\
s. events = event;

console. log ('linktrackvars: ', s. linktrackvars);\
console. log ('linktrackevents: ', s. linktrackevents);\
console. log (', eventi: ', s. events);

s. tl ();}

```
The following code sample adds a handler to listen to all the events that happen. It uses the page load rule on load, waits for events to exist, then sets up handler for all events from the App and tracks them. You do not need to modify this code.
```

/**
* Aggiunge un gestore di analisi per tutti gli eventi di analisi di Livefyre. Per ogni evento, imposta i dati su un oggetto globale e quindi invia l'evento.

*/function
addanalyticshandler () {Livefyre.
analytics. addhandler (function (events) {(events) || []). Foreach (funzione (data) {console.
log ('Evento gestito: ', data. type);
Tracklivefyreevent (data);});});}

```
## More Info

For more information on the topics discussed on this page, see:

* [Report Suite Manager](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)
* [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html)
* [Rules](https://marketing.adobe.com/resources/help/en_US/dtm/rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)

