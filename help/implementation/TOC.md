---
product: livefyre
audience: end-user
user-guide-title: Guida all'implementazione di Livefyre
translation-type: tm+mt
source-git-commit: 3664bc1c51d2b372c358385127a1ca9c2f0cfef8
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 3%

---


# Guida all&#39;implementazione di Livefyre {#implementation}

+ [Guida all&#39;implementazione di Livefyre](home.md)
+ Introduzione {#getting-started}
   + [Guida introduttiva all&#39;integrazione con Livefyre](c-getting-started/c-getting-started.md)
   + Implementation Process {#implementation-process}
      + [Processo di implementazione](c-getting-started/c-implementation-process/c-implementation-process.md)
      + [Tipi di integrazione delle app](c-getting-started/c-implementation-process/c-app-integration-types.md)
      + [Implementazione app](c-getting-started/designer-app-implementation.md)
      + [Implementazione di Livefyre con l&#39;integrazione di terze parti](c-app-integrations/implement-livefyre-3rd-party.md)
      + [Architettura](c-getting-started/c-implementation-process/c-architecture.md)
      + [Incorporare un&#39;app](c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)
      + [Aggiungere l&#39;autenticazione a un&#39;app tramite Livefyre.js](c-getting-started/c-implementation-process/c-add-authetication-to-an-app-using-livefyre.js.md)
      + [Crea token lato server](c-getting-started/c-implementation-process/c-build-server-side-tokens.md)
      + [CollectionMeta Token](c-getting-started/c-implementation-process/c-collectionmeta-tokent.md)
      + [Token autenticazione utente](c-getting-started/c-implementation-process/c-user-auth-token.md)
      + [Creare una raccolta utilizzando CollectionMeta Token](t-create-a-collectionmeta-token.md)
      + [Creazione di un checksum](c-creating-a-checksum.md)
+ Integrazione identità {#identity-integration}
   + [Integrazione identità](t-about-identity-integration/t-about-identity-integration.md)
   + [Pacchetto di autenticazione](t-about-identity-integration/c-authorization-package.md)
   + [Oggetto AuthDelegate](t-about-identity-integration/c-building-an-auth-delegate.md)
   + [Registrazione delle autorizzazioni utente a sistemi esterni (facoltativo)](t-about-identity-integration/c-posting-user-permissions-to-external-systems.md)
   + Implementa SSO {#implementing-sso}
      + [Implementazione SSO](t-about-identity-integration/c-implementing-sso/c-implementing-sso.md)
      + [Debug delegato autenticazione](t-about-identity-integration/c-implementing-sso/c-debugging-auth.md)
   + Sincronizzazione con Livefyre {#sync-ping-for-pull}
      + [Sincronizzazione con Livefyre tramite Ping per pull](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-sync-with-livefyre-using-ping-for-pull.md)
      + [Creazione dell&#39;endpoint di pull](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-build-the-pull-endpoint.md)
      + [Registra l&#39;endpoint con Studio](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/c-register-the-endpoint-with-studio.md)
      + [Creare il ping](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-build-the-ping.md)
      + [Struttura richiesta pull](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-pull-request-structure.md)
      + [Creare il ping per la risposta pull](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/c-build-the-ping-for-pull-response.md)
+ Identità Livefyre {#livefyre-identity}
   + [Identità Livefyre](c-livefyre-identity-comp/c-livefyre-identity-comp.md)
   + [Abilita identità Livefyre](c-livefyre-identity-comp/t-enable-livefyre-identity.md)
   + Utilizzo delle app social con identità Livefyre {#use-social-apps-with-livefyre-identity}
      + [Creare le app per social network](c-livefyre-identity-comp/t-create-your-social-apps.md)
      + [Creare un&#39;app Facebook da utilizzare con l&#39;identità Livefyre](c-livefyre-identity-comp/t-create-a-facebook-app-for-use-with-livefyre-identity.md)
      + [Creare un&#39;app Twitter da utilizzare con l&#39;identità Livefyre](c-livefyre-identity-comp/t-create-a-twitter-app-for-use-with-livefyre-identity.md)
      + [Crea uno Yahoo! App da utilizzare con identità Livefyre](c-livefyre-identity-comp/t-create-a-yahoo-app-for-use-with-livefyre-identity.md)
      + [Creare un&#39;app di identità Microsoft Live da utilizzare con l&#39;identità Livefyre](c-livefyre-identity-comp/t-create-a-microsoft-live-id-app-for-use-with-livefyre-identity.md)
      + [Creare un&#39;app LinkedIn da utilizzare con l&#39;identità Livefyre](c-livefyre-identity-comp/t-create-a-linkedin-app-for-use-with-livefyre-identity.md)
      + [Creare un&#39;app di identità GitHub da utilizzare con l&#39;identità Livefyre](c-livefyre-identity-comp/c-create-a-github-identity.md)
      + [Utilizzo di Studio per collegare le app Social all&#39;implementazione Livefyre](c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md)
   + [Aggiungi Livefyre.js alla pagina](c-livefyre-identity-comp/t-add-livefyre.js-to-the-page.md)
   + [Inizializza identità Livefyre](c-livefyre-identity-comp/t-initialize-livefyre-identity.md)
   + [E-mail per identità Livefyre](c-livefyre-identity-comp/c-emails-for-livefyre-identity.md)
   + [Janrain Capture/Backplane](c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md)
   + Installazione {#installation}
      + [Installazione delle librerie](c-installing-libraries/c-installing-libraries.md)
      + [Classi e metodi](c-installing-libraries/c-methods-livefyre.md)
      + [Metodi di rete](c-installing-libraries/c-network-methods.md)
      + [setSSL, metodo di rete](c-installing-libraries/r-setssl-method.md)
      + [Metodo di rete buildLivefyreToken](c-installing-libraries/r-buildlivefyretoken-method.md)
      + [Metodo di rete buildUserAuthToken](c-installing-libraries/r-builduserauthtoken-method.md)
      + [validateLivefyreToken, metodo di rete](c-installing-libraries/c-validatelivefyretoken-network-method.md)
      + [setUserSyncUrl, metodo di rete](c-installing-libraries/r-setusersyncurl-method.md)
      + [syncUser, metodo di rete](c-installing-libraries/r-syncuser-method.md)
      + [getUrn, metodo di rete](c-installing-libraries/r-geturn-method.md)
      + [getUrnForUser, metodo di rete](c-installing-libraries/r-geturnforuser-method.md)
      + [getNetworkName, metodo di rete](c-installing-libraries/r-getnetworkname-method.md)
      + [getSite, metodo di rete](c-installing-libraries/r-getsite-method.md)
      + [Metodi delle classi di rete](c-installing-libraries/c-network-class-methods.md)
      + [Metodi della classe Collection](c-installing-libraries/c-collection-methods.md)
      + [createOrUpdate, metodo di raccolta](c-installing-libraries/r-createorupdate-collection-method.md)
      + [Metodo di raccolta buildCollectionMetaToken](c-installing-libraries/r-buildcollectionmetatoken-collection-method.md)
      + [Metodo di raccolta buildChecksum](c-installing-libraries/r-buildchecksum-collection-method.md)
      + [getCollectionContent, metodo di raccolta](c-installing-libraries/t-getcollectioncontent-collection-method.md)
      + [getUrn, metodo di raccolta](c-installing-libraries/r-geturn-collection-method.md)
      + [Metodi della classe Site](c-installing-libraries/c-site-methods.md)
      + [Metodo del sito buildBlogCollection](c-installing-libraries/r-buildblogcollection-site-method.md)
      + [Metodo del sito buildChatCollection](c-installing-libraries/r-buildchatcollection-site-method.md)
      + [Metodo del sito buildCommentsCollection](c-installing-libraries/r-buildcommentscollection-site-method.md)
      + [Metodo del sito buildCountingCollection](c-installing-libraries/r-buildcountingcollection-site-method.md)
      + [Metodo del sito buildRatingsCollection](c-installing-libraries/r-buildratingscollection-site-method.md)
      + [Metodo del sito buildReviewsCollection](c-installing-libraries/r-buildreviewscollection-site-method.md)
      + [Metodo del sito buildSiteNoteCollection](c-installing-libraries/r-buildsitenotescollection-site-method.md)
      + [Metodo del sito buildCollection](c-installing-libraries/r-buildcollection-site-method.md)
      + [getUrn, metodo del sito](c-installing-libraries/r-geturn-site-method.md)
      + [Esempi](c-installing-libraries/c-libraries-examples.md)
   + SDK per dispositivi mobili {#mobile-sdks}
      + [SDK per dispositivi mobili](c-mobile-sdks/c-mobile-sdks.md)
      + [Livefyre iOS SDK](c-mobile-sdks/c-livefyre-ios-sdk.md)
      + [Android SDK](c-mobile-sdks/c-android-sdk.md)
+ [Livefyre.js](c-livefyre.js.md)
+ [Creazione di token Livefyre C#](c-creating-livefyre-tokens-c-.md)
+ Integrazioni app {#app-integrations}
   + [Chat](c-app-integrations/c-app-integratios-chat.md)
   + Commenti {#comments}
      + [Commenti](c-app-integrations/c-comments-integration/c-comments-integration.md)
   + [Blog dal vivo](c-app-integrations/c-live-blog-integration.md)
   + [Recensioni](c-app-integrations/c-reviews-integration.md)
   + Sidenotes {#sidenotes}
      + [Integrazione Sidenotes](c-app-integrations/c-sidenotes-integration/r-sidenotes-integration.md)
      + [Aggiunta di note a una pagina](c-app-integrations/c-sidenotes-integration/r-adding-sidenotes-to-a-page.md)
      + [Sidenotes Eventi App](c-app-integrations/c-sidenotes-integration/r-app-events.md)
      + [Opzioni di configurazione Sidenotes](c-app-integrations/c-sidenotes-integration/r-configuration-options.md)
      + [Note Stili Personalizzati](c-app-integrations/c-sidenotes-integration/r-custom-styles.md)
      + [Note Personalizzate](c-app-integrations/c-sidenotes-integration/r-custom-strings.md)
      + [Implementazione delle note](c-app-integrations/c-sidenotes-integration/r-sidenotes-implementation.md)
      + [updateAnchors, metodo](c-app-integrations/c-sidenotes-integration/update-anchors-method.md)
   + [Mappa](c-app-integrations/c-map-integration.md)
   + [Muro di supporto](c-app-integrations/c-media-wall-integration.md)
   + [Tendenza](c-app-integrations/c-trending-integration.md)
+ Personalizzazioni delle app {#app-customizations}
   + [Personalizzazioni delle app](c-app-customizations/c-app-customizations.md)
   + [Modifica delle opzioni di visualizzazione](c-app-customizations/c-change-display-options.md)
   + [Classi CSS](c-app-customizations/c-css-classes.md)
   + [Storify classi CSS](c-app-customizations/c-storify-css-classes.md)
   + [Set di traduzioni](c-app-customizations/c-translation-sets.md)
   + [Spostare il logo Livefyre](c-app-customizations/c-move-the-livefyre-logo.md)
   + [Limita file multimediali](c-app-customizations/c-restrict-media.md)
   + [Nascondi elementi app](c-app-customizations/c-hide-app-elements.md)
   + [Cambia icona @mention](c-app-customizations/c-change-mention-icon.md)
   + [Evidenzia contenuto](c-app-customizations/c-highlight-content.md)
   + [Personalizzare il timbro di data e ora](c-app-customizations/c-date-time-stamp.md)
   + Feature Content {#feature-content}
      + [Feature Content](c-app-customizations/t-feature-content.md)
      + [Abilita la funzionalità dei contenuti in Studio](c-app-customizations/t-enable-featuring-content-in-studio.md)
      + [Selezionare il contenuto da utilizzare in una specifica app](c-app-customizations/t-select-content-to-feature.md)
      + [Seleziona il contenuto da utilizzare in Studio](c-app-customizations/t-select-content-to-feature-from-studio.md)
      + [Utilizzo di CSS per lo stile di contenuto in evidenza](c-app-customizations/c-use-css-to-style-featured-content.md)
      + [API delle funzionalità](c-app-customizations/c-feature-apis.md)
   + [Connessione di Janrain a Livefyre tramite AuthDelegate](c-app-customizations/c-connecting-janrain-to-livefyre-using-authdelegate.md)
   + [Contenuto in evidenza aggregato tramite le API in evidenza](c-app-customizations/c-aggregated-featured-content-using-the-featured-apis.md)
   + Contenuto stile {#style-content}
      + [Stile contenuto gruppo utenti](c-app-customizations/c-style-user-group-content.md)
      + [Aggiunta di utenti ai gruppi](c-app-customizations/c-adding-users-to-groups.md)
   + Applica stili personalizzati {#apply-custom-styles}
      + [Applicazione di stili personalizzati](c-app-customizations/c-applying-custom-styles-.md)
      + [Aggiungi pulsanti personalizzati](c-app-customizations/t-add-custom-buttons.md)
   + Eventi JavaScript {#javascript-events}
      + [Definizioni ed esempi di eventi JavaScript](c-app-customizations/c-javascript-events.md)
      + [Eventi JavaScript per le app di visualizzazione](c-app-customizations/c-javascript-events-for-visualization-apps.md)
      + [Eventi JavaScript per Media Wall](c-app-customizations/c-javascript-events-media-wall.md)
      + [Eventi JavaScript per le app di conversazione](c-app-customizations/c-javascript-events-for-conversation-apps.md)
   + [Incorpora un&#39;app commenti](c-app-customizations/c-embed-a-comments-app.md)
   + [Tracciamento riferimento](c-app-customizations/c-referral-tracking.md)
   + [Supporto per dispositivi e browser](c-app-customizations/c-device-and-browser-support.md)
   + [Requisiti di visualizzazione Twitter](c-app-customizations/c-twitter-display-requirements.md)
+ [Criterio test di stress](c-stress-test-policy.md)
+ Analytics {#analytics}
   + [Analytics](livefyre-analytics/livefyre-analytics.md)
   + [Utilizzo di Livefyre con Adobe Analytics e Dynamic Tag Manager (DTM)](livefyre-analytics/c-use-livefyre-with-adobe-analytics.md)
   + [Utilizzo di Livefyre con altri strumenti di Analytics](livefyre-analytics/c-livefyre-analytics.md)
   + [Eventi di Livefyre Analytics](livefyre-analytics/c-livefyre-analytics-events.md)
+ [Integrazione di Livefyre con AEM](c-livefyre-aem-integration.md)
+ Argomenti avanzati {#advanced-topics}
   + [Visualizza conteggio commenti](c-advanced-topics/t-display-comment-count.md)
   + [Abilitazione della condivisione per social network](c-advanced-topics/c-enabling-social-sharing.md)
   + [Flusso attività](c-advanced-topics/c-activity-stream.md)
   + [Bootstrap HTML](c-advanced-topics/c-bootstrap-html.md)
   + [Cambia raccolta](c-advanced-topics/c-change-collection.md)
   + [Raccolte multiple](c-advanced-topics/c-multiple-collections.md)
   + [Cambia tipi di app di base](c-advanced-topics/c-switch-core-app-types.md)
   + [Contatore social](c-advanced-topics/c-social-counter.md)
   + [Utilizzare l&#39;API Bootsrap e Stream con le app Livefyre](c-advanced-topics/bootstrap-stream-api.md)
