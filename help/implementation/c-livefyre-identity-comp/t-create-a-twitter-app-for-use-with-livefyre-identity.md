---
description: Potete utilizzare Identità Livefyre con Twitter per consentire agli utenti di utilizzare i propri accessi Twitter per interagire con le App sul sito.
seo-description: Potete utilizzare Identità Livefyre con Twitter per consentire agli utenti di utilizzare i propri accessi Twitter per interagire con le App sul sito.
seo-title: Creare un'app Twitter da utilizzare con l'identità Livefyre
solution: Experience Manager
title: Creare un'app Twitter da utilizzare con l'identità Livefyre
uuid: 841cce7c-618d-4154-85a3-1de96d04bb69
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---


# Creare un&#39;app Twitter da utilizzare con Livefyre Identity{#create-a-twitter-app-for-use-with-livefyre-identity}

Potete utilizzare Identità Livefyre con Twitter per consentire agli utenti di utilizzare i propri accessi Twitter per interagire con le App sul sito.

Per abilitare l&#39;accesso a Twitter, Livefyre richiede le seguenti informazioni per l&#39;app Twitter:

* Chiave consumer (chiave API)
* Segreto consumer (Segreto API)

Per creare un&#39;app Twitter da usare con l&#39;identità Livefyre:

1. Andate a https://apps.twitter.com/[](https://apps.twitter.com/) e accedete al vostro account Twitter per creare una nuova app o selezionate un&#39;app esistente da utilizzare con Livefyre Identity.
1. Dalla pagina Settings (Impostazioni) per l&#39;app:

   * Immettere **[!UICONTROL Callback URL:]** `https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/twitter_fyre` (dove **{networkName}** è il nome di rete fornito da Livefyre. Ad esempio:** [!UICONTROL labs]** in **[!UICONTROL `labs.fyre.co`]**.)
   * Deselezionare **[!UICONTROL Enable Callback Locking]**.
   * Seleziona **[!UICONTROL Allow this application to be used to Sign in with Twitter]**.

1. Dalla scheda **[!UICONTROL Permissions]**, selezionare **[!UICONTROL Access: Read only]**.

Al termine, nella pagina Gestione applicazione di Twitter > Tasti e Token di accesso verrà elencata la chiave consumer (Chiave API) dell&#39;app e il Segreto consumer (Segreto API) da utilizzare nella pagina Impostazioni integrazione di Studio.
