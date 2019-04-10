---
description: Monitora il clic sulla pagina dal traffico di riferimento.
seo-description: Monitora il clic sulla pagina dal traffico di riferimento.
seo-title: Tracciamento del riferimento
solution: Experience Manager
title: Tracciamento del riferimento
uuid: 7 daf 615 d -0 c 07-49 d 1-adb 2-1 ac 67 ea 563 e 7
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Tracciamento del riferimento{#referral-tracking}

Monitora il clic sulla pagina dal traffico di riferimento.

Livefyre aggiunge una variabile di riferimento all'URL quando un commento viene postato o condiviso su un social network e per i permalinmi inclusi nelle e-mail di Livefyre. Utilizzate questa variabile per tenere traccia del traffico di riferimento da Livefyre Apps alle vostre proprietà social o proprietà.

Livefyre Apps consente di tenere traccia dei flussi di dati derivanti dal traffico di riferimento, consentendo di analizzare il traffico del sito.

## Tracciamento del traffico di Livefyre {#section_nsy_qp4_xz}

Il traffico di Livefyre da social network ed e-mail potrebbe essere tracciato analizzando i parametri delle stringhe query negli URL delle pagine e implementando il codice sulla pagina per tenerne traccia attraverso il fornitore di analisi. Livefyre aggiunge un collegamento di riferimento all'URL quando un commento viene postato o condiviso su un social network e per i permalinmi inclusi nelle e-mail di Livefyre.

## Esempio di implementazione {#section_xvs_x44_xz}

Se il traffico proviene da una notifica basata su streamhub, si verificherà un parametro di stringa di query hubrefsrc con un valore di posta elettronica, Facebook, Twitter, linkedin o permalink. Il nome del parametro hubrefsrc può essere configurato a livello di rete dal team di consegna di Livefyre.

Per poter essere integrato con una piattaforma di analisi, la pagina deve cercare hubrefsrc in fase di caricamento e registrare il traffico se presente.

Ad esempio:

```
(function () { 
   var qs = document.location.search.substring(1), 
      param = 'hubRefSrc', 
      valueRegex = new RegExp(param+'=([^&]+)'), 
      match = qs.match(valueRegex), 
      referrer; 
   if (match) { 
      // StreamHub generated traffic! 
      referrer = match[1]; 
      console.log('StreamHub referred via', referrer); 
   } else { 
      // StreamHub did not refer this traffic 
   } 
}())
```



App che utilizzano questa funzione:

* [Chat](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Commenti](/help/using/c-about-apps/c-comments/c-comments.md)
* [Recensioni](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sidenotes](../c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)

