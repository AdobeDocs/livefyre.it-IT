---
description: Crea app Livefyre da zero per creare esperienze personalizzate e visualizzazioni di dati.
seo-description: Crea app Livefyre da zero per creare esperienze personalizzate e visualizzazioni di dati.
seo-title: Integrazione di Livefyre con l'integrazione di terze parti
solution: Experience Manager
title: Integrare Livefyre in un CMS
uuid: 5a3e18e8-8568-45bb-9070-d0fa43dd819b
translation-type: tm+mt
source-git-commit: 40cd8c2c89c17134bfcda510527dd6fff41400b5

---


# Implementazione di Livefyre con l'integrazione di terze parti

Crea app Livefyre da zero per creare esperienze personalizzate e visualizzazioni di dati.

Potete creare un'app Livefyre da zero utilizzando Livefyre e i dati social tramite l'API Bootstrap e Stream.

Per le app Livefyre che richiedono l'autenticazione, consultate Integrazione delle identità per informazioni sulle piattaforme di autenticazione di terze parti supportate.

Per implementare le app di conversazione (commenti, chat, blog dal vivo, note):

1. Esegui integrazione con l'app.
a. Create una raccolta utilizzando CollectionMeta Token.
b. Integrate le app Livefyre nei siti mediante la struttura di codice Livefyre.js incorporato.

   * Per ulteriori informazioni sull'utilizzo della struttura del codice da incorporare di Livefyre.js, consultate [Incorporare un'app](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

   * Per informazioni su come integrare l'app Commenti, vedere [Commenti](/help/using/c-about-apps/c-comments/c-comments.md).

   * Per informazioni su come integrare l'app Chat, consulta [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md).

   * Per informazioni su come integrare l'app Live Blog, consulta [Live Blog](/help/using/c-about-apps/c-liveblog-app/c-liveblog-app.md).

   * Per informazioni su come integrare l'app Sidenotes, vedi [Note](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md).

1. Eseguire l'integrazione dell'autenticazione.
a. Create token di autenticazione utente per trasmettere e archiviare i dati utente in Livefyre.
b. Integrare piattaforme di autenticazione e utenti di terze parti. Per un elenco delle piattaforme supportate, vedete Integrazione [](/help/implementation/t-about-identity-integration/t-about-identity-integration.md)identità.

1. Esegui personalizzazioni app. Opzioni Personalizzazione app per adattarle al proprio marchio e stile e aggiungere funzionalità personalizzate.

Per creare un’app di visualizzazione (Mappa, Muro file multimediale, Tendenza, Carosello, Filmstrip, Storify, Feature Card, Mosaico, Sondaggi):

1. Esegui integrazione con l'app.
a. Create una raccolta utilizzando CollectionMeta Token.
b. Integrate le app Livefyre nei siti mediante la struttura di codice Livefyre.js incorporato. Per ulteriori informazioni sull'utilizzo della struttura del codice da incorporare di Livefyre.js, consultate [Incorporare un'app](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

   * Per informazioni su come integrare l’app Mappa, consultate [Mappa](/help/using/c-about-apps/c-map-app/c-map-app.md).

   * Per informazioni su come integrare l’app Media Wall, vedi [Media Wall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md).

   * Per informazioni su come integrare l'app di tendenze, vedi [Tendenza](/help/using/c-about-apps/c-trending-app/c-trending-app.md).

1. Eseguire l'integrazione dell'autenticazione.
a. Create token di autenticazione utente per trasmettere e archiviare i dati utente in Livefyre.
b. Integrare piattaforme di autenticazione e utenti di terze parti. Per un elenco delle piattaforme supportate, vedete Integrazione [](/help/implementation/t-about-identity-integration/t-about-identity-integration.md)identità.

>[!NOTE]
>
>Livefyre non supporta le app Carosello, Filmstrip, Storify, Feature Card, Mosaic e Polls tramite Livefyre.js.
Integra queste app utilizzando il processo [Crea un'app](/help/using/c-about-apps/c-create-an-app.md) .