---
description: Puoi utilizzare Livefyre Identity con Google per consentire agli utenti di utilizzare i propri accessi Google per interagire con app sul tuo sito.
seo-description: Puoi utilizzare Livefyre Identity con Google per consentire agli utenti di utilizzare i propri accessi Google per interagire con app sul tuo sito.
seo-title: Creare un progetto Google da utilizzare con Livefyre Identity
solution: Experience Manager
title: Creare un progetto Google da utilizzare con Livefyre Identity
uuid: b 0 a 6 bb 8 a-abea -4 f 5 c -92 ed 60183 e 1 e d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Creare un progetto Google da utilizzare con Livefyre Identity{#create-a-google-project-for-use-with-livefyre-identity}

Puoi utilizzare Livefyre Identity con Google per consentire agli utenti di utilizzare i propri accessi Google per interagire con app sul tuo sito.

Per consentire agli utenti di accedere con le loro credenziali Google, Livefyre richiede le informazioni di Google Project seguenti:

* ID client
* Segreto cliente

Per creare un progetto Google da utilizzare con Livefyre Identity:

1. Andate a [https://console.cloud.google.com/project](https://console.cloud.google.com/project) e accedete al vostro account Google per creare una nuova app o selezionate un&#39;app esistente da utilizzare con Livefyre Identity.
1. Dal pannello del progetto per l&#39;app, fate clic **[!UICONTROL Enable and Manage APIs]** su.
1. Dalla pagina Panoramica API, in API Social, fai clic per attivare l&#39;API Google +.
1. Dalla pagina Credenziali API, selezionate **[!UICONTROL Credentials > New credentials > OAuth]** ID client. Nella **[!UICONTROL Create client ID]** pagina che si apre:

   * Seleziona tipo applicazione: Applicazione Web.
   * Inserite un **[!UICONTROL Name]** per **[!UICONTROL Client ID]**.
   * Lascia **[!UICONTROL Authorized JavaScript origins]** vuoto il campo.
   * Enter **[!UICONTROL Authorized redirect URIs]**: `https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/google_fyre` (where **[!UICONTROL {networkName}]** is your Livefyre provided network name. Ad esempio: ** [!UICONTROL labs]** in **[!UICONTROL `labs.fyre.co`]**.)
   * Fate clic su **[!UICONTROL Create]** per salvare le credenziali.

Al termine, la pagina Gestione API di Google &gt; Credenziali elenca l&#39;ID client e il segreto cliente del progetto da utilizzare nella pagina Impostazioni integrazione di Studio.
