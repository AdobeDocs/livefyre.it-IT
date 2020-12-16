---
description: Tieni traccia dei clic che tornano alla pagina dal traffico di riferimento.
seo-description: Tieni traccia dei clic che tornano alla pagina dal traffico di riferimento.
seo-title: Tracciamento riferimento
solution: Experience Manager
title: Tracciamento riferimento
uuid: 5206cc16-9671-4b3d-a013-be1a3e8c029d
translation-type: tm+mt
source-git-commit: bd989c97ae5cf06a5ac3deec215f865b0fe95d16
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 1%

---


# Tracciamento riferimento{#referral-tracking}

Tieni traccia dei clic che tornano alla pagina dal traffico di riferimento.

Livefyre aggiunge una variabile di riferimento all’URL quando un commento viene pubblicato o condiviso su un social network, e per i collegamenti permali inclusi nelle e-mail di Livefyre. Utilizzate questa variabile per tenere traccia del traffico di riferimento dalle app Livefyre alle proprietà social o di proprietà.

Le app Livefyre consentono di tenere traccia dei flussi di dati risultanti dal traffico dei riferimenti e di analizzare il traffico del sito.

## Tracciamento del traffico di riferimento di Livefyre {#section_nsy_qp4_xz}

Il traffico di riferimento Livefyre dai social network e dalle e-mail può essere monitorato esaminando i parametri della stringa di query negli URL delle pagine e implementando il codice sulla pagina per tenere traccia di questo problema tramite il provider di analisi. Livefyre aggiunge un collegamento di riferimento all&#39;URL quando un commento viene pubblicato o condiviso su un social network, e per i collegamenti permali inclusi nelle e-mail di Livefyre.

## Esempio di implementazione {#section_xvs_x44_xz}

Se il traffico proveniva da una notifica di StreamHub, sarà presente un parametro di stringa di query hubRefSrc con un valore di e-mail, facebook, twitter, linkedin o permalink. Il nome del parametro hubRefSrc può essere configurato a livello di rete dal team di distribuzione di Livefyre.

Per poter essere integrata con una piattaforma di analisi, la pagina deve cercare hubRefSrc al caricamento e registrare il traffico, se presente.

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

* [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md)
* [Commenti](/help/using/c-about-apps/c-comments/c-comments.md)
* [Recensioni](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md)
* [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md)