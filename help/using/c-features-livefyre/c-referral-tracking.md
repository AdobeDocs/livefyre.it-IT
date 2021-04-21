---
description: Monitora i clic di nuovo alla pagina dal traffico di riferimento.
title: Tracciamento dei riferimenti
exl-id: 44cc221c-1603-4e6e-ae4a-1b993f7dc446
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 1%

---

# Tracciamento riferimento{#referral-tracking}

Monitora i clic di nuovo alla pagina dal traffico di riferimento.

Livefyre aggiunge una variabile di riferimento all&#39;URL quando un commento viene pubblicato o condiviso su un social network e per i permalink inclusi nelle e-mail di Livefyre. Utilizza questa variabile per tenere traccia del traffico di riferimento dalle app Livefyre alle proprietà social o di proprietà.

Le app Livefyre ti consentono di tenere traccia dei flussi di dati derivanti dal traffico di riferimento, consentendoti di analizzare il traffico del sito.

## Tracciamento del traffico di riferimento Livefyre {#section_nsy_qp4_xz}

Il traffico di riferimento di Livefyre dai social network ed e-mail può essere monitorato ispezionando i parametri della stringa di query negli URL delle pagine e implementando il codice sulla pagina per tracciarlo attraverso il provider di analisi. Livefyre aggiunge un collegamento di riferimento all&#39;URL quando un commento viene pubblicato o condiviso su un social network, e per i permalink inclusi nelle e-mail di Livefyre.

## Esempio di implementazione {#section_xvs_x44_xz}

Se il traffico proveniva da una notifica basata su StreamHub, sarà presente un parametro di stringa di query hubRefSrc con un valore di e-mail, facebook, twitter, linkedin o permalink. Il nome del parametro hubRefSrc può essere configurato a livello di rete dal team di consegna Livefyre.

Per eseguire l’integrazione con una piattaforma di analisi, la pagina deve cercare hubRefSrc al caricamento e registrare il traffico, se presente.

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
* [Note](../c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
