---
description: Utilizzate le API Livefyre per aggiungere la funzionalità Google AMP alla pagina Storify 2 per mantenere i contenuti interattivi e intuitivi per il SEO.
seo-description: Utilizzate le API Livefyre per aggiungere la funzionalità Google AMP alla pagina Storify 2 per mantenere i contenuti interattivi e intuitivi per il SEO.
seo-title: Usa Google AMP con Storify 2
solution: Experience Manager
title: Usa Google AMP con Storify 2
uuid: 40c9f083-7284-43ba-ae27-53b1ff9e3954
translation-type: tm+mt
source-git-commit: 65d931e5bd04964db44f8e3a0e000ecec2652893
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---


# Usa Google AMP con Storify 2{#use-google-amp-with-storify}

Utilizzate le API Livefyre per aggiungere la funzionalità Google AMP alla pagina Storify 2 per mantenere i contenuti interattivi e intuitivi per il SEO.

Per utilizzare Google AMP con Storify 2, è necessario creare una pagina per l&#39;app Storify 2 con la marcatura AMP di Google.

La versione AMP delle richieste di aggiornamento dell&#39;app dalla pagina originale (utilizzate il parametro **pollInterval** nell&#39;API **amp-live-list** per impostare l&#39;intervallo per le richieste di aggiornamento). Per garantire che i visitatori sulla pagina AMP ottengano rapidamente il contenuto più aggiornato, mantenete un TTL a bassa cache sulle pagine AMP di Storify 2.

Le risorse non immagini (ad esempio, i video) incluse come post in un&#39;app Storify 2 devono utilizzare HTTPS come specificato dalle specifiche AMP. Gli URL AMP che utilizzano Google Cloud Content Delivery Network (CDN) utilizzano HTTPS.

Per utilizzare Google AMP con Storify 2:

1. Create un modello convalidato AMP sul sito.
1. Utilizzate una o più delle seguenti API Google AMP per personalizzare la pagina Google AMP:
   1. [amp-iframe](https://www.ampproject.org/docs/reference/components/amp-iframe) per personalizzare il display Storify 2
   1. [amp-live-list](https://www.ampproject.org/docs/reference/components/amp-live-list) per personalizzare l&#39;intervallo di tempo per gli aggiornamenti
   1. [amp-social-share](https://www.ampproject.org/docs/reference/components/amp-social-share) per aggiungere un pulsante di condivisione social network
1. Includete il contenuto della seguente pagina Storify 2 AMP nel CSS per la pagina Storify 2 all&#39;interno del `<style amp-custom>` tag: [https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css](https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css)
1. Includete il contenuto della seguente API di markup AMP di Storify 2 nel modello Google AMP: `https://api.livefyre.com/app-service/v4/bootstrap/{{APP_ID}}/amp` dove {{APP_ID}} è l&#39;ID app per l&#39;app Storify 2 in Livefyre Studio.
   1. L&#39;unico parametro di query è **pollInterval**, ovvero l&#39;intervallo in cui l&#39;app controllerà la disponibilità di aggiornamenti (in millisecondi).
   1. L’URL include contenuti dai post più recenti (inclusi Tweet, video e così via)
   1. La pagina di pubblicazione deve ottenere il contenuto da questo URL tutte le volte che si desidera aggiornare la pagina Google AMP.
