---
description: Puoi utilizzare Livefyre Identity con Facebook per consentire agli utenti di utilizzare i loro accessi Facebook per interagire con le app sul tuo sito.
title: Creare un’app Facebook da utilizzare con Livefyre Identity
exl-id: ec320865-6ea3-4f6f-a5f6-31f3d5cbdc93
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 1%

---

# Creare un&#39;app Facebook da utilizzare con Livefyre Identity{#create-a-facebook-app-for-use-with-livefyre-identity}

Puoi utilizzare Livefyre Identity con Facebook per consentire agli utenti di utilizzare i loro accessi Facebook per interagire con le app sul tuo sito.

Per consentire agli utenti di accedere con le loro credenziali Facebook, Livefyre richiede le seguenti informazioni dell&#39;app Facebook:

* ID app
* Segreto app

Per creare un’app Facebook da utilizzare con Livefyre Identity:

1. Vai a [https://developers.facebook.com/apps](https://developers.facebook.com/apps).
1. Accedi al tuo account sviluppatore Facebook.
1. Fai clic su **[!UICONTROL Add New App]** o seleziona un&#39;app esistente da utilizzare con Livefyre Identity.
1. Fare clic su **[!UICONTROL Settings]**, quindi su **[!UICONTROL Basic]**. Immettere un indirizzo **[!UICONTROL Contact Email]**, **[!UICONTROL Display Name]**, **[!UICONTROL Privacy Policy URL]** e **[!UICONTROL Terms of Service URL]**.
1. Fare clic sul segno più ( **[!UICONTROL +]**) accanto a **[!UICONTROL Products]**.
1. Fare clic su **[!UICONTROL Set Up]** in **[!UICONTROL Facebook Login]**.
1. Fai clic su **[!UICONTROL Settings]** e configura quanto segue:

   * Impostare **[!UICONTROL Client OAuth Login]** su **[!UICONTROL Yes]**.
   * Impostare **[!UICONTROL Web OAuth Login]** su **[!UICONTROL Yes]**.
   * Impostare **[!UICONTROL Use Strict Mode for Redirect URIs]** su **[!UICONTROL Yes]**.
   * Impostare **[!UICONTROL Enforce HTTPS for Web OAuth Login]** su **[!UICONTROL Yes]**.
   * In **[!UICONTROL Valid OAuth redirect URLs]**, aggiungi l’URL `https://identity.livefyre.com/{networkName}/api/v1.0/public/profile/social/complete/facebook_fyre` (dove `{networkName}` è il nome di rete fornito da Livefyre).

1. Alla voce **[!UICONTROL App Review]**:

   * Rendi l&#39;app pubblica.
   * Assicurati che i **[!UICONTROL Approved Items]** per **[!UICONTROL Login Permissions]** includano `email`, `public_profile` e `user_friends`.

Una volta completata, la pagina Dashboard dello sviluppatore di Facebook elencherà l’App ID e il Segreto app da utilizzare nelle impostazioni di integrazione di Studio.
