---
description: Utilizzate le API di Livefyre per aggiungere funzionalità Google AMP alla vostra pagina Storify 2 per mantenere il contenuto interattivo e SEO.
seo-description: Utilizzate le API di Livefyre per aggiungere funzionalità Google AMP alla vostra pagina Storify 2 per mantenere il contenuto interattivo e SEO.
seo-title: Utilizzo di Google AMP con Storify 2
solution: Experience Manager
title: Utilizzo di Google AMP con Storify 2
uuid: 40 c 9 f 083-7284-43 ba-ae 27-53 b 1 ff 9 e 3954
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Utilizzo di Google AMP con Storify 2{#use-google-amp-with-storify}

Utilizzate le API di Livefyre per aggiungere funzionalità Google AMP alla vostra pagina Storify 2 per mantenere il contenuto interattivo e SEO.

Per utilizzare Google AMP con Storify 2, è necessario creare una pagina per l&#39;app Storify 2 con marcatura Google AMP.

La versione AMP dell&#39;app richiede aggiornamenti dalla pagina originale (utilizzate il **parametro pollinterval** nell&#39;API **con elenco live** per impostare l&#39;intervallo per le richieste di aggiornamento). Per garantire che i visitatori della pagina AMP ricevano rapidamente il contenuto più aggiornato, mantenete un TTL basso nelle pagine Storify 2 AMP.

Le risorse non di immagine (ad esempio, video) incluse come post in un&#39;app Storify 2 devono utilizzare HTTPS come specificato dalla specifica AMP. Gli URL AMP che utilizzano Google Cloud Content Delivery Network (CDN) utilizzano HTTPS.

Per utilizzare Google AMP con Storify 2:

1. Create un modello con convalida AMP sul sito.
1. Per personalizzare la pagina Google AMP, usa una o più delle seguenti API Google AMP:
   1. [amp-iframe](https://www.ampproject.org/docs/reference/components/amp-iframe) per personalizzare la visualizzazione Storify 2
   1. [amp-live-list](https://www.ampproject.org/docs/reference/components/amp-live-list) per personalizzare l&#39;intervallo di tempo per gli aggiornamenti
   1. [amp-social-share](https://www.ampproject.org/docs/reference/components/amp-social-share) per aggiungere un pulsante di condivisione social network
1. Includete il contenuto della seguente pagina Storify 2 AMP nel CSS per la pagina Storify 2 all&#39;interno del <style amp-custom> tag: [https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css](https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css)
1. Includi i contenuti della seguente API di marcatura Storify 2 AMP nel modello Google AMP: `https://api.livefyre.com/app-service/v4/bootstrap/{{APP_ID}}/amp` dove {{APP_ ID}} è l&#39;ID app per l&#39;app Storify 2 in Livefyre Studio.
   1. L&#39;unico parametro query è **pollinterval**, ovvero l&#39;intervallo in cui l&#39;app controllerà la disponibilità di aggiornamenti (impostati in millisecondi).
   1. L&#39;URL include i contenuti dei post più recenti (inclusi tweet, video, ecc.)
   1. La pagina editore deve ottenere il contenuto da questo URL tutte le volte che si desidera aggiornare la pagina Google AMP.
