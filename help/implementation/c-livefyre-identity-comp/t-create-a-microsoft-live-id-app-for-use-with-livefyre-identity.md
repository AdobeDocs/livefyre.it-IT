---
description: Potete utilizzare Identità Livefyre con Microsoft Live Identity per consentire agli utenti di utilizzare i propri accessi Facebook per interagire con le App sul sito.
seo-description: Potete utilizzare Identità Livefyre con Microsoft Live Identity per consentire agli utenti di utilizzare i propri accessi Facebook per interagire con le App sul sito.
seo-title: Creare un'app di identità Microsoft Live da utilizzare con l'identità Livefyre
solution: Experience Manager
title: Creare un'app di identità Microsoft Live da utilizzare con l'identità Livefyre
uuid: 0c13e1bc-817f-43ed-85d5-09c9e95b6234
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Creare un'app di identità Microsoft Live da utilizzare con l'identità Livefyre{#create-a-microsoft-live-identity-app-for-use-with-livefyre-identity}

Potete utilizzare Identità Livefyre con Microsoft Live Identity per consentire agli utenti di utilizzare i propri accessi Facebook per interagire con le App sul sito.

Per consentire agli utenti di accedere con le proprie credenziali Microsoft Live Identity, Livefyre richiede le seguenti informazioni Microsoft Live Identity:

* ID client (chiave privata)
* Segreto cliente (password)

Per creare un'app Microsoft Live Identity da utilizzare con Livefyre Identity:

1. Creazione o accesso a un account Microsoft Live all'indirizzo [https://apps.dev.microsoft.com](https://apps.dev.microsoft.com/)
1. Create una nuova app o selezionatela per l'utilizzo con l'identità Livefyre.
1. Fare clic **[!UICONTROL Add Platform]**, quindi selezionare Web come tipo di piattaforma.
1. Accertatevi che l' **[!UICONTROL Allow Implicit Flow]** opzione sia selezionata e immettete l'URL di reindirizzamento, utilizzando il nome di rete anziché {nome-rete}: `https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/mslive_fyre`.
1. Generare una nuova coppia password/chiave per ottenere la chiave privata.
1. In **[!UICONTROL Livefyre Integration Settings Livefyre Identity Microsoft Live]**, passate l’ **[!UICONTROL Enable Microsoft Live Login]** interruttore a **[!UICONTROL On]**.
1. Immettere l'ID client Microsoft Live e il Segreto client Microsoft Live.
1. Fai clic su **[!UICONTROL Save Settings]**.

Al termine, nella pagina dei dettagli dell'app di Microsoft Live Identity verranno elencati l'ID client (chiave di consumo) dell'app e il Segreto cliente (Segreto consumatore) per l'utilizzo nella pagina Impostazioni integrazione di Studio.
