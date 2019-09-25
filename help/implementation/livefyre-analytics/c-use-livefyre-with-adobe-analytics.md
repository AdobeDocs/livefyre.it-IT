---
description: nulle
seo-description: nulle
seo-title: Utilizzo di Livefyre con Adobe Analytics e Dynamic Tag Manager (DTM) lk xavvn vefyre con Adobe Analytics e Dynamic Tag Manager (DTM)
uuid: 9a1c25c0-c474-46ff-82ac-e89357007c7f
translation-type: tm+mt
source-git-commit: 55bfc0a545bb4a1093c29bd11e764c9799135324

---


# Utilizzo di Livefyre con Adobe Analytics e Dynamic Tag Manager (DTM){#use-livefyre-with-adobe-analytics-and-dynamic-tag-manager-dtm}

Configurate Adobe Analytics e Dynamic Tag Manager (DTM) per raccogliere i dati per le app Livefyre.

## Passaggio 1: Impostazione di eventi in Adobe Analytics {#section_iks_kgd_4cb}

Mappatura degli eventi Livefyre su uno o più eventi di successo personalizzati in Adobe Analytics Report Suite Manager.

Per ulteriori informazioni su Report Suite Manager, consulta [Report Suite Manager](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html).

1. Accedete ad Adobe Analytics come utente amministratore.
1. Apri Adobe Analytics Admin Report Suite Manager.
1. Create una nuova suite di rapporti o sceglietene una esistente.
1. Modifica la suite di rapporti facendo clic sulla suite di rapporti da modificare, quindi passa a **[!UICONTROL Edit Settings > Conversion > Success Events]**.
1. Mappare gli eventi Livefyre su uno o più eventi di successo personalizzati.

## Passaggio 2: Imposta variabili di conversione

Mappa le variabili di conversione Livefyre (eVar) su variabili di conversione in Adobe Analytics Admin Report Suite Manager. Le variabili di conversione si comportano come una funzione di ordinamento per determinare in che modo intendete identificare i dati raccolti dagli eventi Livefyre.

1. In Report Suite Manager fate clic su **[!UICONTROL Edit Settings > Conversion > Conversion Variables]**.
1. Scegliete le variabili di conversione personalizzate (eVar) da usare e mappatele sulle variabili di conversione Livefyre. Per mappare una variabile di conversione Livefyre su una variabile di conversione personalizzata:
* Abilita la variabile di conversione
* Denominate la variabile di conversione
* Attribuire un tipo alla variabile di conversione
1. Salvare le variabili di conversione personalizzate.

## Passaggio 3: Utilizzo di Gestione dinamica dei tag per aggiungere la suite di rapporti con gli eventi Livefyre {#section_t15_2hd_4cb}

Aggiungi Adobe Analytics a DTM per far funzionare Analytics. A tal fine, create una nuova proprietà e un nuovo strumento e aggiungete alla proprietà la nuova suite di rapporti con gli eventi Livefyre. Per ulteriori informazioni su Gestione dinamica dei tag, vedi [Gestione dinamica dei tag](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html).

Non è necessario eseguire questo passaggio se si dispone già di una proprietà o di uno strumento impostato per la suite di rapporti impostata con gli eventi Livefyre.

1. In Gestione dinamica dei tag, crea o modifica una proprietà esistente.
1. Creare o modificare uno strumento Adobe Analytics esistente.
1. Se uno strumento Adobe Analytics esistente non esiste, fate clic sul **[!UICONTROL Add a Tool]** pulsante.
Impostate i seguenti parametri per lo strumento:
* Impostate **[!UICONTROL Tool Type]** su **[!UICONTROL Adobe Analytics]**.
* Enable **[!UICONTROL Automatic Configuration]**.
* Enable **[!UICONTROL Authenticate via Marketing Cloud]**.
1. Aggiungete o confermate il nome della suite di rapporti con gli eventi Livefyre al **[!UICONTROL Report Suites]** campo.

## Passaggio 4: Imposta una regola di caricamento pagina per impostare la gestione di Analytics {#section_jfj_j3d_4cb}

Imposta una regola di caricamento pagina per inserire tutti i dati. La regola di caricamento delle pagine consente di inserire JavaScript personalizzato nella regola che registra l’evento al caricamento della pagina.

>[!NOTE]
>
>Non utilizzate le regole basate su eventi o le regole di chiamata diretta.

1. In Gestione dinamica dei tag, seleziona **[!UICONTROL Rules]** scheda.
1. Fai clic su **[!UICONTROL Page Load Rules]**.
1. Fate clic sul **[!UICONTROL Create New Rule]** pulsante.
1. Aprite la **[!UICONTROL Conditions]** sezione facendo clic sul **[!UICONTROL Plus]** pulsante.
1. Attiva la regola. Scegliete **[!UICONTROL DOM Ready]** o **[!UICONTROL Onload]** tipi di trigger se desiderate ritardare o implementare la regola in modo asincrono.
1. (Facoltativo) Aggiungete ulteriori parametri per limitare le pagine in cui sono visualizzate le app Livefyre. Per ulteriori informazioni sulle opzioni di configurazione aggiuntive, vedi [Gestione dinamica dei tag](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html).
1. In **[!UICONTROL Javascript/ Third Party Tags]**, fare clic sulla **[!UICONTROL Non-sequential]** scheda e quindi su **[!UICONTROL Add New Script]**.
1. Selezionare **[!UICONTROL Sequential HTML]** come tipo di script.
1. Aggiungere lo script seguente nell'editor di codice e fare clic su **[!UICONTROL Save Code]**.
Lo script seguente richiama la regola di chiamata `livefyre_analytics` diretta dopo il caricamento di Livefyre JavaScript. L'esempio di script seguente verifica ogni 400 ms per verificare se `livefyre.analytics` si trova sulla pagina. Dopo il caricamento della pagina, livefyre.analytics invia le informazioni di tracciamento.

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

1. Fai clic su **[!UICONTROL Save Code]**.
1. Fai clic su **[!UICONTROL Save Rule]**.

## Passaggio 5: Crea una regola di chiamata diretta per costruire la configurazione di mappatura Adobe Analytics per Livefyre {#section_gvp_b1g_pdb}

Esistono altri modi per implementare Livefyre con DTM utilizzando eventi personalizzati, campi dell'interfaccia utente di Adobe Analytics in DTM ed elementi di dati. Questo documento utilizza JavaScript personalizzato per ottenere lo stesso effetto.

1. In Gestione dinamica dei tag, seleziona la scheda **Regole** e fai clic su Regole **chiamate** dirette.
1. Click on the **Create New Rule** button.
1. Denominate la nuova regola **Livefyre Analytics**.
1. Espandere l'area di configurazione **delle condizioni** .
1. Nel campo **Stringa** , immettere `livefyre_analytics`.
1. Espandete la sezione Tag Javascript/3rd party e fate clic sul pulsante **Aggiungi nuovo script** .
1. Immettete **Livefyre Analytics Config** nella casella di input Nome **** tag.
1. Selezionate Javascript **non sequenziale**.
1. Immettete il seguente codice di configurazione Livefyre nell’editor del codice e fate clic sul pulsante **Salva codice** .

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

* Aggiunge un gestore di analisi per tutti gli eventi di analisi da Livefyre. Per ogni evento, imposta i dati su un oggetto globale e quindi invia l'evento.

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

var s = _satellite.getToolsByType`('sc')[0]`.getS();
var evarMap = {appId: 'eVar81',appType: 'eVar82'};

```
The following sample code maps the specific events you set up in the Report Suite Manager with available Livefyre events. In this example, `event82` is set up as any user interaction event without differentiating which kind of user interaction event (for example, liking or sharing content). This is an efficient way to record all user interaction information in a block. You can also map the events in the DTM Analytics UI with Data Element referencing.
```

var eventMap = {FlagCancel: 'event82',\
FlagClick: 'event82',\
ContrassegnoNon d'accordo: 'event82',\
FlagOffensive: 'event82',\
FlagOffTopic: 'event82',\
FlagSpam: 'event82',\
Ad esempio: 'event82',Load: 'event81',\
RequestMore: 'event82',\
ShareButtonClick: 'event82',\
Condividi su Facebook: 'event82',\
ShareOnPostClick: 'event82',\
ShareTwitter: 'event82',\
ShareURL: 'event82',\
SortStream: 'event82',\
TwitterLikeClick: 'event82',TwitterReplyClick: 'event82',\
TwitterRetweetClick: 'event82',\
TwitterUserFollow: 'event82'};

```
The following sample states that if there isn't an event in this list, don't do anything. You do not need to modify this section of code.
```

function trackLivefyreEvent(data) {\
var event =[eventMapdata.type];
console.log('Track:', data.type, event);

if (!event) {console.warning(data.type, 'non è mappato a un evento in AA');\
return;
}

```
The following code differentiates the event types that `event82` records. The conversion variable, `eVar83` records the type of user interaction, and the script sets up `eVar83` to separate the user interaction data by type. So `eVar83` allows you to break out the recorded data into specific types of user interactions.
```

var vars = ['events'];\
switch (event) {case 'event82': s.eVar83 = data.type;\
vars.push('eVar83');\
break;
default:
}

['generator', 'evars'].foreach(function (type) {\
var obj =[datype];
for (var d in obj) {if (obj.hasOwnProperty(d) &amp;&amp;[evarMapd]) {\
s[[evarMapd]] =[objd];\
vars.push([evarMapd]);
}});

s.linkTrackVars = vars.join(',');\
s.linkTrackEvents = event;\
s.events = event;

console.log('linkTrackVars:', s.linkTrackVars);\
console.log('linkTrackEvents:', s.linkTrackEvents);\
console.log('events:', s.events);

s.tl();
}

```
The following code sample adds a handler to listen to all the events that happen. It uses the page load rule on load, waits for events to exist, then sets up handler for all events from the App and tracks them. You do not need to modify this code.
```

/**
* Aggiunge un gestore di analisi per tutti gli eventi di analisi da Livefyre. Per ogni evento, imposta i dati su un oggetto globale e quindi invia l'evento.

*/function addAnalyticsHandler() {Livefyre.analytics.addHandler(function (events) {(events)|| []).foreach(function (data) {console.log('Event handling:', data.type);
trackLivefyreEvent(data);
});
});
}

```
## More Info

For more information on the topics discussed on this page, see:

* [Report Suite Manager](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)
* [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html)
* [Rules](https://marketing.adobe.com/resources/help/en_US/dtm/rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)

