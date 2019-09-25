---
description: Potete utilizzare Identità Livefyre con Facebook per consentire agli utenti di utilizzare i loro accessi Facebook per interagire con le App sul sito.
seo-description: Potete utilizzare Identità Livefyre con Facebook per consentire agli utenti di utilizzare i loro accessi Facebook per interagire con le App sul sito.
seo-title: Creare un'app Facebook da utilizzare con l'identità Livefyre
solution: Experience Manager
title: Creare un'app Facebook da utilizzare con l'identità Livefyre
uuid: a7f7be4e-8986-4e79-831a-0bb0ae55599
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Creare un'app Facebook da utilizzare con l'identità Livefyre{#create-a-facebook-app-for-use-with-livefyre-identity}

Potete utilizzare Identità Livefyre con Facebook per consentire agli utenti di utilizzare i loro accessi Facebook per interagire con le App sul sito.

Per consentire ai vostri utenti di accedere con le loro credenziali Facebook, Livefyre richiede le seguenti informazioni per l'app Facebook:

* ID app
* Segreto app

Per creare un'app Facebook da usare con l'identità Livefyre:

1. Andate a [https://developers.facebook.com/apps](https://developers.facebook.com/apps).
1. Accedete al vostro account sviluppatore di Facebook.
1. Fai clic **[!UICONTROL Add New App]** o seleziona un'app esistente da utilizzare con l'identità Livefyre.
1. Fate clic **[!UICONTROL Settings]**, quindi **[!UICONTROL Basic]**. Immettete un **[!UICONTROL Contact Email]** indirizzo **[!UICONTROL Display Name]**, **[!UICONTROL Privacy Policy URL]** e **[!UICONTROL Terms of Service URL]**.
1. Fare clic sul segno più ( **[!UICONTROL +]**) accanto a **[!UICONTROL Products]**.
1. Fare clic su **[!UICONTROL Set Up]** sotto **[!UICONTROL Facebook Login]**.
1. Fate clic su **[!UICONTROL Settings]** e configurate le seguenti impostazioni:

   * Impostate **[!UICONTROL Client OAuth Login]** su **[!UICONTROL Yes]**.
   * Impostate **[!UICONTROL Web OAuth Login]** su **[!UICONTROL Yes]**.
   * Impostate **[!UICONTROL Use Strict Mode for Redirect URIs]** su **[!UICONTROL Yes]**.
   * Impostate **[!UICONTROL Enforce HTTPS for Web OAuth Login]** su **[!UICONTROL Yes]**.
   * In **[!UICONTROL Valid OAuth redirect URLs]**, aggiungete l’URL `https://identity.livefyre.com/{networkName}/api/v1.0/public/profile/social/complete/facebook_fyre` (dove `{networkName}` è il nome di rete Livefyre).

1. In **[!UICONTROL App Review]**:

   * Rendi l'app pubblica.
   * Accertatevi che **[!UICONTROL Approved Items]** per **[!UICONTROL Login Permissions]** include `email`, `public_profile`e `user_friends`.

Al termine, la pagina Dashboard dello sviluppatore di Facebook elenca l'App ID e il Segreto app da utilizzare nelle impostazioni di integrazione di Studio.
