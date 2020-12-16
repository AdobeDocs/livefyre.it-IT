---
description: Potete utilizzare l'identità Livefyre con LinkedIn per consentire agli utenti di utilizzare i propri accessi LinkedIn per interagire con le app sul sito.
seo-description: Potete utilizzare l'identità Livefyre con LinkedIn per consentire agli utenti di utilizzare i propri accessi LinkedIn per interagire con le app sul sito.
seo-title: Creare un'app LinkedIn da utilizzare con l'identità Livefyre
solution: Experience Manager
title: Creare un'app LinkedIn da utilizzare con l'identità Livefyre
uuid: c5112f24-a4e0-4526-afe8-b8f27a3b2854
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---


# Creare un&#39;app LinkedIn da utilizzare con Livefyre Identity{#create-a-linkedin-app-for-use-with-livefyre-identity}

Potete utilizzare l&#39;identità Livefyre con LinkedIn per consentire agli utenti di utilizzare i propri accessi LinkedIn per interagire con le app sul sito.

Per abilitare l&#39;accesso a LinkedIn, Livefyre richiede le seguenti informazioni sull&#39;app LinkedIn:

* Chiave consumer (chiave API)
* Segreto consumer (Segreto API)

Per creare un&#39;app LinkedIn da utilizzare con l&#39;identità Livefyre:

1. Andate a https://www.linkedin.com/secure/developer ed effettuate l&#39;accesso al vostro account LinkedIn per creare una nuova app o selezionate un&#39;app esistente da usare con Identità Livefyre.
1. Clic **[!UICONTROL Create Application]**.
1. Completate il modulo per creare l&#39;applicazione.
1. In **[!UICONTROL Default Application Permissions]**, abilita le autorizzazioni per l&#39;app **[!UICONTROL r_basicprofile]** e **[!UICONTROL r_emailaddress]**.
1. Immettere **[!UICONTROL OAuth 2.0 Authorized Redirect URL]** come `https://identity.livefyre.com/{network-name}.fyre.co/api/v1.0/public/profile/social/complete/linkedin_fyre`.
1. Salvate l&#39;app.
1. In **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > LinkedIn]**, passare l&#39;interruttore **[!UICONTROL Enable LinkedIn Login]** su **[!UICONTROL On]**.
1. Immettete l&#39;ID client LinkedIn e il segreto cliente LinkedIn.
1. Clic **[!UICONTROL Save Settings]**.

Al termine, la pagina dei dettagli dell&#39;app di LinkedIn elenca la chiave API dell&#39;app (Chiave consumatore) e il Segreto API (Segreto consumatore) da utilizzare nella pagina Impostazioni integrazione di Studio.
