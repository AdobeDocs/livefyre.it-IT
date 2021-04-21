---
description: Crea app Livefyre da zero per creare esperienze personalizzate e visualizzazioni di dati.
title: Integrare Livefyre in un CMS
exl-id: 05d85792-de97-47b1-90cc-ad7e841754b5
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Implementare Livefyre con l’integrazione di terze parti

Crea app Livefyre da zero per creare esperienze personalizzate e visualizzazioni di dati.

Puoi creare un’app Livefyre da zero utilizzando Livefyre e dati social tramite l’API Bootstrap e Stream.

Per le app Livefyre che richiedono l’autenticazione, consulta Integrazione di identità per informazioni sulle piattaforme di autenticazione di terze parti supportate.

Per implementare le app di conversazione (Commenti, Chat, Live Blog, Note a margine):

1. Eseguire l’integrazione con l’app.
a) Creare una raccolta utilizzando il token CollectionMeta .
b) Integra le app Livefyre nei siti utilizzando la struttura del codice di incorporamento Livefyre.js .

   * Per ulteriori informazioni su come utilizzare la struttura del codice di incorporamento Livefyre.js, consulta [Incorporare un&#39;app](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

   * Per informazioni su come integrare l&#39;app Commenti, consulta [Commenti](/help/using/c-about-apps/c-comments/c-comments.md).

   * Per informazioni su come integrare l&#39;app Chat, consulta [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md).

   * Per informazioni su come integrare l&#39;app Live Blog, vedi [Live Blog](/help/using/c-about-apps/c-liveblog-app/c-liveblog-app.md).

   * Per informazioni su come integrare l&#39;app Sidenotes, consulta [Note a margine](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md).

1. Esegui l’integrazione di autenticazione.
a) Crea token di autenticazione utente per passare e archiviare i dati utente in Livefyre.
b) Integrare piattaforme di autenticazione e utenti di terze parti. Per un elenco delle piattaforme supportate, consulta [Integrazione delle identità](/help/implementation/t-about-identity-integration/t-about-identity-integration.md).

1. Esegui personalizzazioni app. Opzioni di personalizzazione app per abbinare branding e stile e aggiungere funzionalità personalizzate.

Per creare un’app di visualizzazione (Mappa, Muro di supporto, Tendenza, Carosello, Filmstrip, Storify, Feature Card, Mosaic, Polls):

1. Eseguire l’integrazione con l’app.
a) Creare una raccolta utilizzando il token CollectionMeta .
b) Integra le app Livefyre nei siti utilizzando la struttura del codice di incorporamento Livefyre.js . Per ulteriori informazioni su come utilizzare la struttura del codice di incorporamento Livefyre.js, consulta [Incorporare un&#39;app](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

   * Per informazioni su come integrare l&#39;app mappa, consulta [Mappa](/help/using/c-about-apps/c-map-app/c-map-app.md).

   * Per informazioni su come integrare Media Wall App, consulta [Media Wall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md).

   * Per informazioni su come integrare l’app di tendenza, consulta [Tendenza](/help/using/c-about-apps/c-trending-app/c-trending-app.md).

1. Esegui l’integrazione di autenticazione.
a) Crea token di autenticazione utente per passare e archiviare i dati utente in Livefyre.
b) Integrare piattaforme di autenticazione e utenti di terze parti. Per un elenco delle piattaforme supportate, consulta [Integrazione delle identità](/help/implementation/t-about-identity-integration/t-about-identity-integration.md).

>[!NOTE]
>
>Livefyre non supporta le app Carosello, Filmstrip, Storify, Feature Card, Mosaic e Polls utilizzando Livefyre.js.

Integra queste app utilizzando il processo [Crea un&#39;app](/help/using/c-about-apps/c-create-an-app.md) .
