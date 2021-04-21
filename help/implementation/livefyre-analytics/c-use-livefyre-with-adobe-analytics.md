---
description: Imposta Adobe Analytics e Dynamic Tag Manager (DTM) per raccogliere i dati per le app Livefyre.
exl-id: a866782d-fca6-48bf-9fb8-5080e396919b
translation-type: tm+mt
source-git-commit: 24d016fbb2771487f8105b2ca0bb0d03dd60cfc1
workflow-type: tm+mt
source-wordcount: '1017'
ht-degree: 1%

---

# Utilizzare Livefyre con Adobe Analytics e Dynamic Tag Manager (DTM){#use-livefyre-with-adobe-analytics-and-dynamic-tag-manager-dtm}

Imposta Adobe Analytics e Dynamic Tag Manager (DTM) per raccogliere i dati per le app Livefyre.

## Passaggio 1: Configurare eventi in Adobe Analytics {#section_iks_kgd_4cb}

Mappatura di eventi Livefyre su uno o più eventi di successo personalizzati in Adobe Analytics Report Suite Manager.

Per ulteriori informazioni su Report Suite Manager, consulta [Report Suite Manager](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html).

1. Accedi ad Adobe Analytics come utente amministratore.
1. Apri Adobe Analytics Admin Report Suite Manager.
1. Crea una nuova suite di rapporti o scegliine una esistente.
1. Modifica la suite di rapporti facendo clic sulla suite di rapporti da modificare, quindi passa a **[!UICONTROL Edit Settings > Conversion > Success Events]**.
1. Mappa gli eventi Livefyre su uno o più eventi di successo personalizzati.

## Passaggio 2: Imposta variabili di conversione

Mappa le variabili di conversione Livefyre (eVar) su variabili di conversione in Adobe Analytics Admin Report Suite Manager. Le variabili di conversione agiscono come una funzione di ordinamento per determinare come si intende identificare i dati raccolti dagli eventi Livefyre.

1. In Report Suite Manager fai clic su **[!UICONTROL Edit Settings > Conversion > Conversion Variables]**.
1. Scegli le variabili di conversione personalizzate (eVar) da utilizzare e mappale sulle variabili di conversione Livefyre. Per mappare una variabile di conversione Livefyre su una variabile di conversione personalizzata:
* Abilitare la variabile di conversione
* Denomina la variabile di conversione
* Assegna alla variabile di conversione un tipo
1. Salva le variabili di conversione personalizzate.

## Passaggio 3: Usa DTM per aggiungere la suite di rapporti con gli eventi Livefyre {#section_t15_2hd_4cb}

Aggiungi Adobe Analytics a DTM per far funzionare Analytics. A questo scopo, crea una nuova proprietà e un nuovo strumento e aggiungi la nuova suite di rapporti con eventi Livefyre alla proprietà . Per ulteriori informazioni su DTM, consulta [DTM](https://docs.adobe.com/content/help/en/dtm/using/c-overview.html).

Non è necessario eseguire questo passaggio se disponi già di una proprietà o di uno strumento configurato per la suite di rapporti configurata con eventi Livefyre.

1. In DTM, crea o modifica una proprietà esistente.
1. Crea o modifica uno strumento Adobe Analytics esistente.
1. Se uno strumento Adobe Analytics esistente non esiste, fai clic sul pulsante **[!UICONTROL Add a Tool]** .
Imposta i seguenti parametri per lo strumento:

   * Impostare **[!UICONTROL Tool Type]** su **[!UICONTROL Adobe Analytics]**.
   * Abilita **[!UICONTROL Automatic Configuration]**.
   * Abilita **[!UICONTROL Authenticate via Marketing Cloud]**.
1. Aggiungi o conferma il nome della suite di rapporti con eventi Livefyre al campo **[!UICONTROL Report Suites]** .

## Passaggio 4: Imposta una regola di caricamento pagina per impostare la gestione di Analytics {#section_jfj_j3d_4cb}

Imposta una regola di caricamento pagina per richiamare tutti i dati. La regola di caricamento della pagina consente di inserire un codice JavaScript personalizzato nella regola che registra l’evento al caricamento della pagina.

>[!NOTE]
>
>Non utilizzare regole basate su eventi o regole di chiamata diretta.

1. In DTM, seleziona la scheda **[!UICONTROL Rules]** .
1. Clic **[!UICONTROL Page Load Rules]**.
1. Fai clic sul pulsante **[!UICONTROL Create New Rule]** .
1. Apri la sezione **[!UICONTROL Conditions]** facendo clic sul pulsante **[!UICONTROL Plus]** .
1. Attiva la regola. Scegli i tipi di trigger **[!UICONTROL DOM Ready]** o **[!UICONTROL Onload]** se desideri ritardare o implementare la regola in modo asincrono.
1. (Facoltativo) Aggiungi parametri aggiuntivi per limitare le pagine che visualizzano le app Livefyre. Per ulteriori informazioni sulle opzioni di configurazione aggiuntive, consulta [DTM](https://docs.adobe.com/content/help/en/dtm/using/c-overview.html).
1. In **[!UICONTROL Javascript/ Third Party Tags]**, fai clic sulla scheda **[!UICONTROL Non-sequential]** , quindi fai clic su **[!UICONTROL Add New Script]**.
1. Seleziona **[!UICONTROL Sequential HTML]** come tipo di script.
1. Aggiungi il seguente script nell&#39;editor di codice e fai clic su **[!UICONTROL Save Code]**.

   Lo script seguente chiama la regola di chiamata diretta `livefyre_analytics` dopo il caricamento di JavaScript Livefyre. L&#39;esempio di script seguente controlla ogni 400 ms per vedere se `livefyre.analytics` è sulla pagina. Dopo il caricamento della pagina, livefyre.analytics invia le informazioni di tracciamento.

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

1. Clic **[!UICONTROL Save Code]**.
1. Clic **[!UICONTROL Save Rule]**.

## Passaggio 5: Creare una regola di chiamata diretta per costruire la configurazione di mappatura Adobe Analytics per Livefyre {#section_gvp_b1g_pdb}

Esistono altri modi per implementare Livefyre con DTM utilizzando eventi personalizzati, campi dell’interfaccia utente di Adobe Analytics all’interno di DTM ed elementi dati. Questo documento utilizza JavaScript personalizzato per ottenere lo stesso effetto.

1. In DTM seleziona la scheda **Regole** , quindi fai clic su **Regole di chiamata diretta**.
1. Fai clic sul pulsante **Crea nuova regola** .
1. Denomina la nuova regola **Livefyre Analytics**.
1. Espandi l’area di configurazione **condition**.
1. Nel campo **String**, immetti `livefyre_analytics`.
1. Espandi la sezione Javascript / Tag di terze parti e fai clic sul pulsante **Aggiungi nuovo script** .
1. Immetti **Configurazione Livefyre Analytics** nella casella di input **Nome tag** .
1. Seleziona **Javascript non sequenziale**.
1. Immetti il seguente codice di configurazione Livefyre nell&#39;editor di codice e fai clic sul pulsante **Salva codice** .

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

   * Aggiunge un gestore di analisi per tutti gli eventi di analisi da Livefyre. Per ogni evento, imposta i dati su un oggetto globale e quindi invia l&#39;evento.

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

1. Fai clic su **Salva regola**.

## Passaggio 6: Approva le modifiche per la regola di caricamento pagina {#section_pxc_11t_ycb}

1. Vai alla scheda **[!UICONTROL Approvals]** .
1. Clic **[!UICONTROL Approve]**.
1. Fai clic su **[!UICONTROL Yes, approve]** per confermare l’approvazione.
1. Vai a **[!UICONTROL Overview > Publish Queue]**.
1. Seleziona la regola da pubblicare.
1. Clic **[!UICONTROL Publish Selected]**.
1. Fai clic su **[!UICONTROL Publish]** per confermare la pubblicazione.

## Script {#section_xkb_vft_mcb}

Il codice di esempio seguente mappa le eVar specifiche sugli eVar Livefyre disponibili. Il nome della variabile di conversione Livefyre ( `eVar`) (ad esempio, `appId`) viene mappato sul nome configurato in Report Suite Manager (ad esempio, `eVar81`). Modifica i nomi `eVar` in questo script con le variabili di conversione personalizzate.


```
var s = _satellite.getToolsByType`('sc')[0]`.getS(); 
var evarMap = { 
  appId: 'eVar81', 
  appType: 'eVar82' 
};
```

Il codice di esempio seguente mappa gli eventi specifici impostati in Report Suite Manager con gli eventi Livefyre disponibili. In questo esempio, `event82` viene impostato come qualsiasi evento di interazione dell’utente senza differenziare quale tipo di evento di interazione dell’utente (ad esempio, il collegamento o la condivisione di contenuto). Questo è un modo efficiente per registrare tutte le informazioni di interazione dell’utente in un blocco. Puoi anche mappare gli eventi nell’interfaccia utente di DTM Analytics con riferimento agli elementi dati.

```
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
```

L&#39;esempio seguente afferma che se nell&#39;elenco non è presente un evento, non eseguire alcuna operazione. Non è necessario modificare questa sezione di codice.

```
function trackLivefyreEvent(data) {  
  var event = eventMap[data.type]; 
  console.log('Track:', data.type, event); 
   
  if (!event) { 
    console.warn(data.type, 'is not mapped to an event in AA');  
    return; 
  }
```

Il codice seguente distingue i tipi di evento registrati da `event82`. La variabile di conversione `eVar83` registra il tipo di interazione dell&#39;utente e lo script si imposta `eVar83` per separare i dati di interazione dell&#39;utente in base al tipo. Quindi `eVar83` consente di suddividere i dati registrati in tipi specifici di interazioni dell&#39;utente.

```
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
   
  console.log('linkTrackVars:', s.linkTrackVars);  
  console.log('linkTrackEvents:', s.linkTrackEvents);  
  console.log('events:', s.events); 
   
  s.tl(); 
}
```

Il codice di esempio seguente aggiunge un gestore per ascoltare tutti gli eventi che si verificano. Usa la regola di caricamento della pagina al caricamento, attende l&#39;esistenza di eventi, quindi imposta il gestore per tutti gli eventi dall&#39;app e li tiene traccia. Non è necessario modificare questo codice.

```
/** 
* Adds an analytics handler for all analytics events from Livefyre. For each event, it sets the data on a global object and then dispatches the event. 
*/ 
function addAnalyticsHandler() { 
  Livefyre.analytics.addHandler(function (events) { 
    (events || []).forEach(function (data) { 
      console.log('Event handled:', data.type); 
      trackLivefyreEvent(data); 
    }); 
  }); 
}
```

## Ulteriori informazioni

Per ulteriori informazioni sugli argomenti trattati in questa pagina, vedi:

* [Report Suite Manager](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html)
* [DTM](https://docs.adobe.com/content/help/en/dtm/using/c-overview.html)
* [Regole](https://docs.adobe.com/content/help/en/dtm/using/resources/rules/create-rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)
