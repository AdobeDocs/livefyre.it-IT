---
description: Potete utilizzare Identità Livefyre con Facebook per consentire agli utenti di utilizzare i loro accessi Facebook per interagire con le App sul sito.
seo-description: Potete utilizzare Identità Livefyre con Facebook per consentire agli utenti di utilizzare i loro accessi Facebook per interagire con le App sul sito.
seo-title: Creare un'app Facebook da utilizzare con l'identità Livefyre
solution: Experience Manager
title: Creare un'app Facebook da utilizzare con l'identità Livefyre
uuid: a7f7be4e-8986-4e79-831a-0bb0ae555599
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---


# Creare un&#39;app Facebook da utilizzare con Livefyre Identity{#create-a-facebook-app-for-use-with-livefyre-identity}

Potete utilizzare Identità Livefyre con Facebook per consentire agli utenti di utilizzare i loro accessi Facebook per interagire con le App sul sito.

Per consentire ai vostri utenti di accedere con le loro credenziali Facebook, Livefyre richiede le seguenti informazioni per l&#39;app Facebook:

* ID app
* Segreto app

Per creare un&#39;app Facebook da usare con l&#39;identità Livefyre:

1. Andate a [https://developers.facebook.com/apps](https://developers.facebook.com/apps).
1. Accedete al vostro account sviluppatore di Facebook.
1. Fate clic su **[!UICONTROL Add New App]** o selezionate un&#39;app esistente da usare con Identità Livefyre.
1. Fare clic su **[!UICONTROL Settings]**, quindi su **[!UICONTROL Basic]**. Immettere un indirizzo **[!UICONTROL Contact Email]**, **[!UICONTROL Display Name]**, **[!UICONTROL Privacy Policy URL]** e **[!UICONTROL Terms of Service URL]**.
1. Fare clic sul segno più ( **[!UICONTROL +]**) accanto a **[!UICONTROL Products]**.
1. Fare clic su **[!UICONTROL Set Up]** in **[!UICONTROL Facebook Login]**.
1. Fare clic su **[!UICONTROL Settings]** e configurare quanto segue:

   * Impostare **[!UICONTROL Client OAuth Login]** su **[!UICONTROL Yes]**.
   * Impostare **[!UICONTROL Web OAuth Login]** su **[!UICONTROL Yes]**.
   * Impostare **[!UICONTROL Use Strict Mode for Redirect URIs]** su **[!UICONTROL Yes]**.
   * Impostare **[!UICONTROL Enforce HTTPS for Web OAuth Login]** su **[!UICONTROL Yes]**.
   * In **[!UICONTROL Valid OAuth redirect URLs]**, aggiungete l&#39;URL `https://identity.livefyre.com/{networkName}/api/v1.0/public/profile/social/complete/facebook_fyre` (dove `{networkName}` è il nome di rete fornito da Livefyre).

1. Sotto **[!UICONTROL App Review]**:

   * Rendi l&#39;app pubblica.
   * Assicurarsi che **[!UICONTROL Approved Items]** per **[!UICONTROL Login Permissions]** includa `email`, `public_profile` e `user_friends`.

Al termine, la pagina Dashboard dello sviluppatore di Facebook elenca l&#39;App ID e il Segreto app da utilizzare nelle impostazioni di integrazione di Studio.
