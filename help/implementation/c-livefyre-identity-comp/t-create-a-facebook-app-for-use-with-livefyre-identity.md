---
description: Potete utilizzare Livefyre Identity con Facebook per consentire agli utenti di utilizzare i propri accessi Facebook per interagire con le app sul vostro sito.
seo-description: Potete utilizzare Livefyre Identity con Facebook per consentire agli utenti di utilizzare i propri accessi Facebook per interagire con le app sul vostro sito.
seo-title: Creare un'app Facebook da utilizzare con Livefyre Identity
solution: Experience Manager
title: Creare un'app Facebook da utilizzare con Livefyre Identity
uuid: a 7 f 7 be 4 e -8986-4 e 79-831 a -0 bb 0 ae 555599
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Creare un&#39;app Facebook da utilizzare con Livefyre Identity{#create-a-facebook-app-for-use-with-livefyre-identity}

Potete utilizzare Livefyre Identity con Facebook per consentire agli utenti di utilizzare i propri accessi Facebook per interagire con le app sul vostro sito.

Per consentire agli utenti di accedere con le credenziali Facebook, Livefyre richiede le seguenti informazioni sull&#39;app Facebook:

* ID app
* Segreto app

Per creare un&#39;app Facebook da utilizzare con Livefyre Identity:

1. Andate a [https://developers.facebook.com/apps](https://developers.facebook.com/apps).
1. Accedete al vostro account sviluppatore Facebook.
1. Fate clic **[!UICONTROL Add New App]** o selezionate un&#39;app esistente da utilizzare con Livefyre Identity.
1. Fate clic **[!UICONTROL Settings]** su **[!UICONTROL Basic]**, Immettete **[!UICONTROL Contact Email]** un indirizzo **[!UICONTROL Display Name]****[!UICONTROL Privacy Policy URL]**, e **[!UICONTROL Terms of Service URL]**.
1. Fare clic sul segno più ( **[!UICONTROL +]**) accanto **[!UICONTROL Products]** a.
1. Fate clic **[!UICONTROL Set Up]** su **[!UICONTROL Facebook Login]**.
1. Fate clic **[!UICONTROL Settings]** su e configurate quanto segue:

   * Impostato **[!UICONTROL Client OAuth Login]** su **[!UICONTROL Yes]**.
   * Impostato **[!UICONTROL Web OAuth Login]** su **[!UICONTROL Yes]**.
   * Impostato **[!UICONTROL Use Strict Mode for Redirect URIs]** su **[!UICONTROL Yes]**.
   * Impostato **[!UICONTROL Enforce HTTPS for Web OAuth Login]** su **[!UICONTROL Yes]**.
   * Sotto **[!UICONTROL Valid OAuth redirect URLs]**, aggiungete l&#39;URL `https://identity.livefyre.com/{networkName}/api/v1.0/public/profile/social/complete/facebook_fyre` (dove `{networkName}` è il nome di rete fornito da Livefyre).

1. Sotto **[!UICONTROL App Review]**:

   * Rendi pubblica l&#39;app.
   * Assicurarsi che l&#39; **[!UICONTROL Approved Items]****[!UICONTROL Login Permissions]** inclusione `email`sia `public_profile`, e `user_friends`.

Al termine, nella pagina Dashboard dello sviluppatore di Facebook viene elencato l&#39;ID app e il Segreto app per l&#39;utilizzo nelle impostazioni integrazione di Studio.
