---
description: Potete utilizzare Identità Livefyre con Twitter per consentire agli utenti di utilizzare i propri accessi Twitter per interagire con le App sul sito.
seo-description: Potete utilizzare Identità Livefyre con Twitter per consentire agli utenti di utilizzare i propri accessi Twitter per interagire con le App sul sito.
seo-title: Creare un'app Twitter da utilizzare con l'identità Livefyre
solution: Experience Manager
title: Creare un'app Twitter da utilizzare con l'identità Livefyre
uuid: 841cce7c-618d-4154-85a3-1de96d04bb69
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Creare un'app Twitter da utilizzare con l'identità Livefyre{#create-a-twitter-app-for-use-with-livefyre-identity}

Potete utilizzare Identità Livefyre con Twitter per consentire agli utenti di utilizzare i propri accessi Twitter per interagire con le App sul sito.

Per abilitare l'accesso a Twitter, Livefyre richiede le seguenti informazioni per l'app Twitter:

* Chiave consumer (chiave API)
* Segreto consumer (Segreto API)

Per creare un'app Twitter da usare con l'identità Livefyre:

1. Andate a [https://apps.twitter.com/](https://apps.twitter.com/)ed effettuate l'accesso al vostro account Twitter per creare una nuova app o selezionate un'app esistente da usare con Identità Livefyre.
1. Dalla pagina Settings (Impostazioni) per l'app:

   * Inserite **[!UICONTROL Callback URL:]** (dove `https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/twitter_fyre` {networkName} **** è il nome di rete fornito da Livefyre). For example:** [!UICONTROL labs]** in **[!UICONTROL `labs.fyre.co`]**.)
   * Deselect .**[!UICONTROL Enable Callback Locking]**
   * Select **[!UICONTROL Allow this application to be used to Sign in with Twitter]**.

1. From the  tab, select .**[!UICONTROL Permissions]****[!UICONTROL Access: Read only]**

When complete, Twitter’s Application Management &gt; Keys and Access Tokens page will list the app’s Consumer Key (API Key) and Consumer Secret (API Secret) for use in Studio’s Integration Settings page.
