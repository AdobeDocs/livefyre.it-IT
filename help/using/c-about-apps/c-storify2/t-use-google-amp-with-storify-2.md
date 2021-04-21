---
description: Utilizza le API Livefyre per aggiungere la funzionalità Google AMP alla tua pagina Storify 2 per mantenere il contenuto interattivo e SEO-friendly.
title: Utilizzare Google AMP con Storify 2
exl-id: 2fee8655-ac9f-484e-a042-9b7ac7151fcc
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# Utilizzare Google AMP con Storify 2{#use-google-amp-with-storify}

Utilizza le API Livefyre per aggiungere la funzionalità Google AMP alla tua pagina Storify 2 per mantenere il contenuto interattivo e SEO-friendly.

Per utilizzare Google AMP con Storify 2, devi creare una pagina per l’app Storify 2 con il markup AMP di Google.

La versione AMP delle richieste di app viene aggiornata dalla pagina originale (usa il parametro **pollInterval** nell&#39;API **amp-live-list** per impostare l&#39;intervallo per le richieste di aggiornamento). Per garantire che i visitatori sulla pagina AMP ricevano rapidamente il contenuto più aggiornato, mantieni un TTL a bassa cache sulle pagine AMP di Storify 2.

Le risorse non immagini (ad esempio, i video) incluse come post in un’app Storify 2 devono utilizzare HTTPS come specificato dalle specifiche AMP. Gli URL AMP che utilizzano la rete CDN (Content Delivery Network) di Google Cloud utilizzano HTTPS.

Per utilizzare Google AMP con Storify 2:

1. Crea un modello convalidato AMP sul sito.
1. Utilizza una o più delle seguenti API Google AMP per personalizzare la tua pagina Google AMP:
   1. [amp-](https://www.ampproject.org/docs/reference/components/amp-iframe) iframe per personalizzare il display Storify 2
   1. [amp-live-](https://www.ampproject.org/docs/reference/components/amp-live-list) list per personalizzare l&#39;intervallo di tempo per gli aggiornamenti
   1. [amp-social-](https://www.ampproject.org/docs/reference/components/amp-social-share) shareto aggiungere un pulsante di condivisione social
1. Includi il contenuto della seguente pagina Storify 2 AMP nel CSS per la pagina Storify 2 all’interno del tag `<style amp-custom>` : [https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css](https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css)
1. Includi il contenuto della seguente API di markup AMP Storify 2 nel modello Google AMP: `https://api.livefyre.com/app-service/v4/bootstrap/{{APP_ID}}/amp` dove {{APP_ID}} è l&#39;ID app per l&#39;app Storify 2 in Livefyre Studio.
   1. L&#39;unico parametro di query è **pollInterval**, che è l&#39;intervallo in cui l&#39;app controllerà la disponibilità di aggiornamenti (in millisecondi).
   1. L’URL include il contenuto dei post più recenti (inclusi Tweet, video, ecc.)
   1. La pagina dell’editore deve ottenere il contenuto da questo URL ogni volta che vuoi che la pagina Google AMP venga aggiornata.
