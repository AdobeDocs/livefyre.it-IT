---
description: Puoi utilizzare Livefyre Identity con Microsoft Live Identity per consentire agli utenti di utilizzare i loro accessi Facebook per interagire con le app sul tuo sito.
title: Creare un’app Microsoft Live Identity da utilizzare con Livefyre Identity
exl-id: 7702c956-ecb5-424a-9866-d6f73d4d4bc9
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---

# Creare un&#39;app Microsoft Live Identity da utilizzare con Livefyre Identity{#create-a-microsoft-live-identity-app-for-use-with-livefyre-identity}

Puoi utilizzare Livefyre Identity con Microsoft Live Identity per consentire agli utenti di utilizzare i loro accessi Facebook per interagire con le app sul tuo sito.

Per consentire agli utenti di accedere con le proprie credenziali di Microsoft Live Identity, Livefyre richiede le seguenti informazioni di Microsoft Live Identity:

* ID client (chiave privata)
* Segreto client (password)

Per creare un’app Microsoft Live Identity da utilizzare con Livefyre Identity:

1. Crea o accedi a un account Microsoft Live all&#39;indirizzo [https://apps.dev.microsoft.com](https://apps.dev.microsoft.com/)
1. Crea una nuova app o selezionane una esistente da utilizzare con Livefyre Identity.
1. Fare clic su **[!UICONTROL Add Platform]**, quindi selezionare Web come tipo di piattaforma.
1. Assicurati che l&#39;opzione **[!UICONTROL Allow Implicit Flow]** sia selezionata e immetti l&#39;URL di reindirizzamento utilizzando il nome di rete anziché {network-name}: `https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/mslive_fyre`.
1. Genera una nuova coppia di password/chiave per ottenere la chiave privata.
1. In **[!UICONTROL Livefyre Integration Settings Livefyre Identity Microsoft Live]**, imposta l&#39;opzione **[!UICONTROL Enable Microsoft Live Login]** su **[!UICONTROL On]**.
1. Immettere l&#39;ID client Microsoft Live e il segreto client Microsoft Live.
1. Clic **[!UICONTROL Save Settings]**.

Al termine, la pagina dei dettagli dell’app di Microsoft Live Identity elenca l’ID client (chiave di consumo) e il segreto client (segreto di consumo) dell’app da utilizzare nella pagina Impostazioni integrazione di Studio.
