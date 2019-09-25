---
description: Potete utilizzare Identità Livefyre con identità GitHub per consentire agli utenti di utilizzare i loro accessi GitHub per interagire con le app sul sito.
seo-description: Potete utilizzare Identità Livefyre con identità GitHub per consentire agli utenti di utilizzare i loro accessi GitHub per interagire con le app sul sito.
seo-title: Creare un'app di identità GitHub da utilizzare con l'identità Livefyre
title: Creare un'app di identità GitHub da utilizzare con l'identità Livefyre
uuid: cf56164c-1521-4a42-89cb-39483764807e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Creare un'app di identità GitHub da utilizzare con l'identità Livefyre{#create-a-github-identity-app-for-use-with-livefyre-identity}

Potete utilizzare Identità Livefyre con identità GitHub per consentire agli utenti di utilizzare i loro accessi GitHub per interagire con le app sul sito.

Per consentire agli utenti di accedere con le proprie credenziali di identità GitHub, Livefyre richiede le seguenti informazioni di identità GitHub:

* ID client (chiave privata)
* Segreto cliente (password)

Per creare un'app di identità GitHub da utilizzare con l'identità Livefyre:

1. Create o accedete a un account GitHub all'indirizzo [](https://github.com/settings/developers).
1. Registra una nuova app o seleziona un'app esistente da utilizzare con Livefyre Identity.
1. Immettere tutte le informazioni sul modulo. Inserite il **[!UICONTROL Authorization callback URL]**, utilizzando il nome della rete anziché `{network-name}: {network-name}: https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/github_fyre`.

1. In **[!UICONTROL Livefyre Integration Settings Livefyre Identity GitHub]**, passate l’ **[!UICONTROL Enable GitHub Login]** interruttore a **[!UICONTROL On]**.

1. Immettete l’ID client GitHub e il segreto cliente GitHub.
1. Fai clic su **[!UICONTROL Save Settings]**.

Al termine, nella pagina dei dettagli dell'app di GitHub Identity verranno elencati l'ID client dell'app (Chiave di consumo) e il Segreto cliente (Segreto di consumo) per l'utilizzo nella pagina Impostazioni integrazione di Studio.
