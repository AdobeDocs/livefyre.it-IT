---
description: Potete utilizzare l'identità Livefyre con LinkedIn per consentire agli utenti di utilizzare i propri accessi LinkedIn per interagire con le app sul sito.
seo-description: Potete utilizzare l'identità Livefyre con LinkedIn per consentire agli utenti di utilizzare i propri accessi LinkedIn per interagire con le app sul sito.
seo-title: Creare un'app LinkedIn da utilizzare con l'identità Livefyre
solution: Experience Manager
title: Creare un'app LinkedIn da utilizzare con l'identità Livefyre
uuid: c5112f24-a4e0-4526-afe8-b8f27a3b2854
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Creare un'app LinkedIn da utilizzare con l'identità Livefyre{#create-a-linkedin-app-for-use-with-livefyre-identity}

Potete utilizzare l'identità Livefyre con LinkedIn per consentire agli utenti di utilizzare i propri accessi LinkedIn per interagire con le app sul sito.

Per abilitare l'accesso a LinkedIn, Livefyre richiede le seguenti informazioni sull'app LinkedIn:

* Chiave consumer (chiave API)
* Segreto consumer (Segreto API)

Per creare un'app LinkedIn da utilizzare con l'identità Livefyre:

1. Andate a https://www.linkedin.com/secure/developer ed effettuate l'accesso al vostro account LinkedIn per creare una nuova app o selezionate un'app esistente da usare con Identità Livefyre.
1. Fai clic su **[!UICONTROL Create Application]**.
1. Completate il modulo per creare l'applicazione.
1. In **[!UICONTROL Default Application Permissions]**, abilitate le autorizzazioni **[!UICONTROL r_basicprofile]** e **[!UICONTROL r_emailaddress]** app.
1. Inserite il valore **[!UICONTROL OAuth 2.0 Authorized Redirect URL]** come `https://identity.livefyre.com/{network-name}.fyre.co/api/v1.0/public/profile/social/complete/linkedin_fyre`.
1. Salvate l'app.
1. In **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > LinkedIn]**, passate l’ **[!UICONTROL Enable LinkedIn Login]** interruttore a **[!UICONTROL On]**.
1. Immettete l'ID client LinkedIn e il segreto cliente LinkedIn.
1. Fai clic su **[!UICONTROL Save Settings]**.

Al termine, la pagina dei dettagli dell'app di LinkedIn elenca la chiave API dell'app (Chiave consumatore) e il Segreto API (Segreto consumatore) da utilizzare nella pagina Impostazioni integrazione di Studio.
