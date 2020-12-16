---
description: Tieni traccia dei clic che tornano alla pagina dal traffico di riferimento.
seo-description: Tieni traccia dei clic che tornano alla pagina dal traffico di riferimento.
seo-title: Tracciamento riferimento
solution: Experience Manager
title: Tracciamento riferimento
uuid: 7daf615d-0c07-49d1-adb2-1ac67ea563e7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
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

* [Chat](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Commenti](/help/using/c-about-apps/c-comments/c-comments.md)
* [Recensioni](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sidenotes](../c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)

