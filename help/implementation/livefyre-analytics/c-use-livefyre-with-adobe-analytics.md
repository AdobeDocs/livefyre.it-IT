---
description: nulle
seo-description: nulle
seo-title: Utilizzo di Livefyre con  Adobe Analytics e Dynamic Tag Manager (DTM) lk xavvn   vefyre con  Adobe Analytics e Dynamic Tag Manager (DTM)
uuid: 9a1c25c0-c474-46ff-82ac-e89357007c7f
translation-type: tm+mt
source-git-commit: 573e815799fbae2c2c4f1d98a01ea0ae04108a34
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 1%

---


# Utilizzo di Livefyre con  Adobe Analytics e Dynamic Tag Manager (DTM){#use-livefyre-with-adobe-analytics-and-dynamic-tag-manager-dtm}

Configurate  Adobe Analytics e Dynamic Tag Manager (DTM) per raccogliere i dati per le app Livefyre.

## Passaggio 1: Configurare gli eventi in  Adobe Analytics {#section_iks_kgd_4cb}

Mappatura degli eventi Livefyre su uno o più eventi di successo personalizzati in  Adobe Analytics Report Suite Manager.

Per ulteriori informazioni su Report Suite Manager, vedere [Report Suite Manager](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html).

1. Accedete a  Adobe Analytics come utente amministratore.
1. Apri  Adobe Analytics Admin Report Suite Manager.
1. Create una nuova suite di rapporti o sceglietene una esistente.
1. Modificate la suite di rapporti facendo clic sulla suite di rapporti da modificare, quindi andate a **[!UICONTROL Edit Settings > Conversion > Success Events]**.
1. Mappare gli eventi Livefyre su uno o più eventi di successo personalizzati.

## Passaggio 2: Imposta variabili di conversione

Mappatura delle variabili di conversione Livefyre (eVar) su variabili di conversione in  Adobe Analytics Admin Report Suite Manager. Le variabili di conversione si comportano come una funzione di ordinamento per determinare in che modo intendete identificare i dati raccolti dagli eventi Livefyre.

1. In Report Suite Manager fare clic su **[!UICONTROL Edit Settings > Conversion > Conversion Variables]**.
1. Scegliete le variabili di conversione personalizzate (eVar) da usare e mappatele sulle variabili di conversione Livefyre. Per mappare una variabile di conversione Livefyre su una variabile di conversione personalizzata:
* Abilita la variabile di conversione
* Denominate la variabile di conversione
* Attribuire un tipo alla variabile di conversione
1. Salvare le variabili di conversione personalizzate.

## Passaggio 3: Utilizzo di Gestione dinamica dei tag per aggiungere la suite di rapporti con gli eventi Livefyre {#section_t15_2hd_4cb}

Aggiungi  Adobe Analytics a DTM per far funzionare Analytics. A tal fine, create una nuova proprietà e un nuovo strumento e aggiungete alla proprietà la nuova suite di rapporti con gli eventi Livefyre. Per ulteriori informazioni su Gestione dinamica dei tag, vedere [Gestione dinamica dei tag](https://docs.adobe.com/content/help/en/dtm/using/c-overview.html).

Non è necessario eseguire questo passaggio se si dispone già di una proprietà o di uno strumento impostato per la suite di rapporti impostata con gli eventi Livefyre.

1. In Gestione dinamica dei tag, crea o modifica una proprietà esistente.
1. Creare o modificare uno strumento Adobe Analytics  esistente.
1. Se non esiste uno strumento Adobe Analytics  esistente, fare clic sul pulsante **[!UICONTROL Add a Tool]**.
Impostate i seguenti parametri per lo strumento:

   * Impostare **[!UICONTROL Tool Type]** su **[!UICONTROL Adobe Analytics]**.
   * Abilita **[!UICONTROL Automatic Configuration]**.
   * Abilita **[!UICONTROL Authenticate via Marketing Cloud]**.
1. Aggiungete o confermate il nome della suite di rapporti con gli eventi Livefyre al campo **[!UICONTROL Report Suites]**.

## Passaggio 4: Imposta una regola di caricamento pagina per impostare la gestione di Analytics {#section_jfj_j3d_4cb}

Imposta una regola di caricamento pagina per inserire tutti i dati. La regola di caricamento delle pagine consente di inserire JavaScript personalizzato nella regola che registra l’evento al caricamento della pagina.

>[!NOTE]
>
>Non utilizzate le regole basate su eventi o le regole di chiamata diretta.

1. In Gestione dinamica dei tag, seleziona la scheda **[!UICONTROL Rules]**.
1. Clic **[!UICONTROL Page Load Rules]**.
1. Fare clic sul pulsante **[!UICONTROL Create New Rule]**.
1. Aprire la sezione **[!UICONTROL Conditions]** facendo clic sul pulsante **[!UICONTROL Plus]**.
1. Attiva la regola. Scegliete i tipi di trigger **[!UICONTROL DOM Ready]** o **[!UICONTROL Onload]** se desiderate ritardare o implementare la regola in modo asincrono.
1. (Facoltativo) Aggiungete ulteriori parametri per limitare le pagine in cui sono visualizzate le app Livefyre. Per ulteriori informazioni sulle opzioni di configurazione aggiuntive, vedere [DTM](https://docs.adobe.com/content/help/en/dtm/using/c-overview.html).
1. In **[!UICONTROL Javascript/ Third Party Tags]** fare clic sulla scheda **[!UICONTROL Non-sequential]**, quindi su **[!UICONTROL Add New Script]**.
1. Selezionare **[!UICONTROL Sequential HTML]** come tipo di script.
1. Aggiungere lo script seguente nell&#39;editor di codice e fare clic su **[!UICONTROL Save Code]**.

   Lo script seguente richiama la regola di chiamata diretta `livefyre_analytics` dopo il caricamento di Livefyre JavaScript. L&#39;esempio di script seguente verifica ogni 400 ms per verificare se `livefyre.analytics` si trova sulla pagina. Dopo il caricamento della pagina, livefyre.analytics invia le informazioni di tracciamento.

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

## Passaggio 5: Crea una regola di chiamata diretta per creare la configurazione  mapping Adobe Analytics per Livefyre {#section_gvp_b1g_pdb}

Esistono altri modi per implementare Livefyre con DTM utilizzando eventi personalizzati,  campi dell&#39;interfaccia utente Adobe Analytics in DTM ed elementi di dati. Questo documento utilizza JavaScript personalizzato per ottenere lo stesso effetto.

1. In Gestione dinamica dei tag selezionare la scheda **Regole**, quindi fare clic su **Regole chiamate dirette**.
1. Fare clic sul pulsante **Crea nuova regola**.
1. Denominate la nuova regola **Livefyre Analytics**.
1. Espandere l&#39;area di configurazione **condition**.
1. Nel campo **String** immettere `livefyre_analytics`.
1. Espandete la sezione Tag Javascript / 3rd party e fate clic sul pulsante **Aggiungi nuovo script**.
1. Immettere **Livefyre Analytics Config** nella casella di input **Tag Name**.
1. Selezionare **Javascript non sequenziale**.
1. Immettete il seguente codice di configurazione Livefyre nell&#39;editor del codice e fate clic sul pulsante **Salva codice**.

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

1. Fare clic su **Salva regola**.

## Passaggio 6: Approvare le modifiche per la regola di caricamento pagina {#section_pxc_11t_ycb}

1. Vai alla scheda **[!UICONTROL Approvals]**.
1. Clic **[!UICONTROL Approve]**.
1. Fare clic su **[!UICONTROL Yes, approve]** per confermare l&#39;approvazione.
1. Vai a **[!UICONTROL Overview > Publish Queue]**.
1. Selezionate la regola da pubblicare.
1. Clic **[!UICONTROL Publish Selected]**.
1. Fate clic su **[!UICONTROL Publish]** per confermare la pubblicazione.

## Script {#section_xkb_vft_mcb}

Il codice di esempio seguente mappa le eVar specifiche alle eVar Livefyre disponibili. Il nome della variabile di conversione Livefyre ( `eVar`) (ad esempio, `appId`) viene mappato sul nome configurato in Report Suite Manager (ad esempio, `eVar81`). Modificate i nomi `eVar` in questo script impostando le variabili di conversione personalizzate.


```
var s = _satellite.getToolsByType`('sc')[0]`.getS(); 
var evarMap = { 
  appId: 'eVar81', 
  appType: 'eVar82' 
};
```

Il seguente codice di esempio mappa gli eventi specifici impostati in Report Suite Manager con gli eventi Livefyre disponibili. In questo esempio, `event82` è configurato come qualsiasi evento di interazione con l&#39;utente senza distinguere quale tipo di evento di interazione con l&#39;utente (ad esempio, come collegamento o condivisione di contenuto). Questo è un modo efficiente per registrare tutte le informazioni di interazione dell&#39;utente in un blocco. Puoi anche mappare gli eventi nell&#39;interfaccia utente di DTM Analytics con un riferimento a Data Element.

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

L&#39;esempio seguente afferma che se non è presente un evento in questo elenco, non eseguire alcuna operazione. Non è necessario modificare questa sezione di codice.

```
function trackLivefyreEvent(data) {  
  var event = eventMap[data.type]; 
  console.log('Track:', data.type, event); 
   
  if (!event) { 
    console.warn(data.type, 'is not mapped to an event in AA');  
    return; 
  }
```

Il codice seguente distingue i tipi di evento che `event82` registra. La variabile di conversione `eVar83` registra il tipo di interazione utente e lo script imposta `eVar83` per separare i dati di interazione utente per tipo. `eVar83` consente quindi di suddividere i dati registrati in tipi specifici di interazioni dell&#39;utente.

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

L&#39;esempio di codice seguente aggiunge un gestore per ascoltare tutti gli eventi che si verificano. Utilizza la regola di caricamento della pagina al momento del caricamento, attende l&#39;esistenza di eventi, quindi configura il gestore per tutti gli eventi dall&#39;app e li tiene traccia. Non è necessario modificare questo codice.

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
