---
description: nulle
seo-description: nulle
seo-title: Utilizzo di Livefyre con altro strumento Analytics
solution: Experience Manager
title: Utilizzo di Livefyre con altro strumento Analytics
uuid: 26 c 835 f 6-aced -41 f 7-aabe -418 afce 8 a 829
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Utilizzo di Livefyre con altro strumento Analytics{#use-livefyre-with-other-analytics-tool}

Potete utilizzare gli strumenti di analisi per raccogliere dati sulle interazioni degli utenti con Livefyre Apps. Potete utilizzare Adobe Analytics o uno strumento di vostra scelta.

Per utilizzare Livefyre con uno strumento di vostra scelta (non Adobe Analytics), seguite la procedura descritta in questa pagina.

## Passaggio 1: Configurare il gestore di eventi {#section_ngm_gzl_pdb}

Configurate un gestore di eventi nelle pagine in cui utilizzate Livefyre Apps. Questo consente di raccogliere dati dalle app nella pagina che potete utilizzare per l&#39;analisi.

Aggiungete Livefyre. js a una pagina per impostare il gestore di eventi. Livefyre. js viene caricato in modo asincrono. Per ridurre le dimensioni del file e migliorare le prestazioni di caricamento, l&#39;analisi non è immediatamente disponibile. È necessario eseguire il polling dell&#39;oggetto di analisi fino a quando i dati non sono disponibili. Posizionare questo script in qualsiasi punto della pagina o aggiungerlo all&#39;interno dei propri script compilati.

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

## Passaggio 2: Funzione di implementazione del gestore

Una volta che la funzionalità Livefyre. analytics è disponibile sulla pagina, implementate la funzione analyticshandler per inviare gli eventi ricevuti al provider di analisi desiderato.

1. Il gestore di analisi riceve un array di eventi che devono essere ripetuti e inviati singolarmente oppure come batch, se il fornitore lo supporta.
1. Mappate i dati dell&#39;evento ricevuti dal gestore su un formato richiesto dal fornitore di analisi.
1. Inviate i dati al vostro provider di analisi.

