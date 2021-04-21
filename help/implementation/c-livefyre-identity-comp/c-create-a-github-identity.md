---
description: Puoi utilizzare Livefyre Identity con GitHub Identity per consentire agli utenti di utilizzare i loro accessi GitHub per interagire con le app sul tuo sito.
title: Creare un’app GitHub Identity da utilizzare con Livefyre Identity
exl-id: f25ffd0e-ea4f-42ac-abfc-c02018421b85
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 0%

---

# Creare un’app GitHub Identity da utilizzare con Livefyre Identity{#create-a-github-identity-app-for-use-with-livefyre-identity}

Puoi utilizzare Livefyre Identity con GitHub Identity per consentire agli utenti di utilizzare i loro accessi GitHub per interagire con le app sul tuo sito.

Per consentire agli utenti di accedere con le proprie credenziali GitHub Identity, Livefyre richiede le seguenti informazioni GitHub Identity:

* ID client (chiave privata)
* Segreto client (password)

Per creare un’app GitHub Identity da utilizzare con Livefyre Identity:

1. Crea o accedi a un account GitHub in [](https://github.com/settings/developers).
1. Registra una nuova app o selezionane una esistente da utilizzare con Livefyre Identity.
1. Immettere tutte le informazioni sul modulo. Inserisci il **[!UICONTROL Authorization callback URL]** utilizzando il nome della rete anziché `{network-name}: {network-name}: https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/github_fyre`.

1. In **[!UICONTROL Livefyre Integration Settings Livefyre Identity GitHub]**, imposta l&#39;opzione **[!UICONTROL Enable GitHub Login]** su **[!UICONTROL On]**.

1. Immetti l’ID client GitHub e il segreto client GitHub.
1. Clic **[!UICONTROL Save Settings]**.

Una volta completata, la pagina dei dettagli dell’app di GitHub Identity elenca l’ID client (chiave di consumo) e il segreto client (segreto di consumo) dell’app da utilizzare nella pagina Impostazioni integrazione di Studio.
