---
title: Utilizzare Livefyre con altri strumenti di Analytics
description: Utilizzare Livefyre con altri strumenti di Analytics
exl-id: da29e281-5095-4e99-a248-19390f2059a2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# Utilizzare Livefyre con altro strumento di Analytics{#use-livefyre-with-other-analytics-tool}

Puoi utilizzare gli strumenti di analisi per raccogliere dati sulle interazioni degli utenti con le app Livefyre. Puoi utilizzare Adobe Analytics o uno strumento di tua scelta.

Per utilizzare Livefyre con uno strumento di tua scelta (non Adobe Analytics), segui la procedura descritta in questa pagina.

## Passaggio 1: Imposta gestore eventi {#section_ngm_gzl_pdb}

Imposta un gestore di eventi sulle pagine in cui utilizzi le app Livefyre. Ciò ti consente di raccogliere i dati dalle app di quella pagina che puoi utilizzare per l’analisi.

Aggiungi Livefyre.js a una pagina per configurare il gestore eventi. Livefyre.js viene caricato in modo asincrono. Per ridurre le dimensioni dei file e migliorare le prestazioni di caricamento, analytics non è disponibile immediatamente. È necessario eseguire il polling dell’oggetto analytics fino a quando i dati non sono disponibili. Posiziona questo script in qualsiasi punto della pagina o lo raggruppa all’interno dei tuoi script compilati.

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

## Passaggio 2: Implementare la funzione handler

Una volta che la funzionalità Livefyre.analytics è disponibile sulla pagina, implementa la funzione analyticsHandler per inviare gli eventi ricevuti al provider di analisi desiderato.

1. Il gestore analytics riceve un array di eventi che devono essere ripetuti e inviati singolarmente o come batch, se il provider lo supporta.
1. Mappa i dati dell&#39;evento ricevuti dal gestore in un formato richiesto dal provider di analisi.
1. Invia i dati al tuo provider di analisi.
