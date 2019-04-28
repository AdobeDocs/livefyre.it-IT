---
description: Crea app Livefyre da zero per creare esperienze personalizzate e visualizzazioni dati.
seo-description: Crea app Livefyre da zero per creare esperienze personalizzate e visualizzazioni dati.
seo-title: Integrare Livefyre con l'integrazione di terze parti
solution: Experience Manager
title: Integrare Livefyre in un CMS
uuid: 5 a 3 e 18 e 8-8568-45 bb -9070-d 0 fa 43 dd 819 b
translation-type: tm+mt
source-git-commit: 40cd8c2c89c17134bfcda510527dd6fff41400b5

---


# Implementazione di Livefyre con l&#39;integrazione di terze parti

Crea app Livefyre da zero per creare esperienze personalizzate e visualizzazioni dati.

Potete creare una app Livefyre da zero consumando Livefyre e i dati social utilizzando l&#39;API Bootstrap e Flusso.

Per Livefyre Apps che richiedono l&#39;autenticazione, consultate Integrazione identità per informazioni sulle piattaforme di autenticazione di terze parti supportate.

Per implementare le app di conversazione (Commenti, Chat, Blog live, Sidenotes):

1. Eseguire l&#39;integrazione con le app.
a. Create una raccolta utilizzando il token collectionmeta.
b. Integrate Livefyre Apps ai siti utilizzando la struttura del codice di incorporamento di Livefyre. js.

   * Per ulteriori informazioni su come utilizzare la struttura di codice di Livefyre. js, consultate [Incorpora un&#39;app](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

   * Per informazioni su come integrare l&#39;App commenti, vedere [Commenti](/help/using/c-about-apps/c-comments/c-comments.md).

   * Per informazioni su come integrare l&#39;app chat, consultate [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md).

   * Per informazioni su come integrare l&#39;app blog live, consultate [Blog live](/help/using/c-about-apps/c-liveblog-app/c-liveblog-app.md).

   * Per informazioni su come integrare App Sidenotes, consultate [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md).

1. Eseguire l&#39;integrazione con l&#39;autenticazione.
a. Create token autenticazione utente per trasmettere e memorizzare i dati utente in Livefyre.
b. Integrare le piattaforme di terze parti e di autenticazione. Per un elenco delle piattaforme supportate, consultate [Integrazione identità](/help/implementation/t-about-identity-integration/t-about-identity-integration.md).

1. Esegui personalizzazioni app. Opzioni Personalizzazione app per adattare il branding e lo stile e aggiungere funzionalità personalizzate.

Per creare un&#39;app di visualizzazione (Mappa, Media Wall, Tendenza, Carosello, Filmstrip, Storify, scheda Funzioni, Mosaic, Sondaggi):

1. Eseguire l&#39;integrazione con le app.
a. Create una raccolta utilizzando il token collectionmeta.
b. Integrate Livefyre Apps ai siti utilizzando la struttura del codice di incorporamento di Livefyre. js. Per ulteriori informazioni su come utilizzare la struttura di codice di Livefyre. js, consultate [Incorpora un&#39;app](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

   * Per informazioni su come integrare l&#39;app Mappa, consultate [Mappa](/help/using/c-about-apps/c-map-app/c-map-app.md).

   * Per informazioni su come integrare l&#39;app Media Wall, consultate [Media Wall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md).

   * Per informazioni su come integrare l&#39;app di tendenza, consulta [Tendenza](/help/using/c-about-apps/c-trending-app/c-trending-app.md).

1. Eseguire l&#39;integrazione con l&#39;autenticazione.
a. Create token autenticazione utente per trasmettere e archiviare i dati utente in Livefyre.
b. Integrare le piattaforme di terze parti e di autenticazione. Per un elenco delle piattaforme supportate, consultate [Integrazione identità](/help/implementation/t-about-identity-integration/t-about-identity-integration.md).

>[!NOTE]
>
>Livefyre non supporta carosello, Filmstrip, Storify, Feature Card, Mosaic e Polls Apps mediante Livefyre. js.
Integrate queste app mediante il [processo Crea app](/help/using/c-about-apps/c-create-an-app.md) .