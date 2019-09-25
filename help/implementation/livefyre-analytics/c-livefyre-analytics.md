---
description: nulle
seo-description: nulle
seo-title: Utilizzo di Livefyre con altri strumenti di Analytics
solution: Experience Manager
title: Utilizzo di Livefyre con altri strumenti di Analytics
uuid: 26c835f6-aced-41f7-ababe-418afce8a829
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Utilizzo di Livefyre con altri strumenti di Analytics{#use-livefyre-with-other-analytics-tool}

Potete utilizzare gli strumenti di analisi per raccogliere dati sulle interazioni degli utenti con le app Livefyre. Puoi utilizzare Adobe Analytics o uno strumento di tua scelta.

Per utilizzare Livefyre con uno strumento di vostra scelta (non Adobe Analytics), seguite la procedura descritta in questa pagina.

## Passaggio 1: Impostazione del gestore eventi {#section_ngm_gzl_pdb}

Configurate un gestore eventi sulle pagine in cui vengono utilizzate le app Livefyre. Questo consente di raccogliere i dati dalle app in quella pagina che puoi utilizzare per l'analisi.

Aggiungete Livefyre.js a una pagina per impostare il gestore eventi. Livefyre.js viene caricato in modo asincrono. Per ridurre le dimensioni dei file e migliorare le prestazioni di caricamento, l'analisi non è disponibile immediatamente. È necessario eseguire il polling dell'oggetto Analytics fino a quando i dati non sono disponibili. Posizionare lo script in un punto qualsiasi della pagina o includerlo in un pacchetto all'interno dei propri script compilati.

```
/** 
 * Handler for Livefyre analytics batch events. 
 * @param {Array.<string>} events Array of events that have been fired since 
 * the last batch send. 
 */ 
function analyticsHandler(events) { 
  // Send to analytics 
  console.log(events); 
} 
 
var attempts = 0; 
 
function pollForAnalytics() { 
  if (Livefyre && Livefyre.analytics) { 
    Livefyre.analytics.addHandler(analyticsHandler); 
    return; 
  } 
  if (attempts === 10) { 
    return; 
  } 
  attempts++; 
  setTimeout(pollForAnalytics, 500); 
} 
 
pollForAnalytics(); 
```

## Passaggio 2: Implementa la funzione gestore

Una volta che la funzionalità Livefyre.analytics sarà disponibile sulla pagina, implementate la funzione analyticsHandler per inviare gli eventi ricevuti al provider di analisi di vostra scelta.

1. Il gestore di analisi riceve un array di eventi che devono essere ripetuti e inviati singolarmente o in batch, se il provider lo supporta.
1. Mappare i dati dell'evento ricevuti dal gestore in un formato richiesto dal provider di analisi.
1. Inviate i dati al vostro provider di analisi.

