---
description: Potete utilizzare Identità Livefyre con Identità GitHub per consentire agli utenti di utilizzare i loro accessi GitHub per interagire con le App sul sito.
seo-description: Potete utilizzare Identità Livefyre con Identità GitHub per consentire agli utenti di utilizzare i loro accessi GitHub per interagire con le App sul sito.
seo-title: Creare un'app di identità GitHub da utilizzare con l'identità Livefyre
title: Creare un'app di identità GitHub da utilizzare con l'identità Livefyre
uuid: cf56164c-1521-4a42-89cb-39483764807e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---


# Creare un&#39;app di identità GitHub da utilizzare con Livefyre Identity{#create-a-github-identity-app-for-use-with-livefyre-identity}

Potete utilizzare Identità Livefyre con Identità GitHub per consentire agli utenti di utilizzare i loro accessi GitHub per interagire con le App sul sito.

Per consentire agli utenti di accedere con le proprie credenziali di identità GitHub, Livefyre richiede le seguenti informazioni di identità GitHub:

* ID client (chiave privata)
* Segreto cliente (password)

Per creare un&#39;app di identità GitHub da utilizzare con l&#39;identità Livefyre:

1. Create o accedete a un account GitHub all&#39;indirizzo [](https://github.com/settings/developers).
1. Registra una nuova app o seleziona un&#39;app esistente da utilizzare con Livefyre Identity.
1. Immettere tutte le informazioni sul modulo. Immettere il **[!UICONTROL Authorization callback URL]** utilizzando il nome della rete anziché `{network-name}: {network-name}: https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/github_fyre`.

1. In **[!UICONTROL Livefyre Integration Settings Livefyre Identity GitHub]**, passare l&#39;interruttore **[!UICONTROL Enable GitHub Login]** su **[!UICONTROL On]**.

1. Immettete l’ID client GitHub e il segreto cliente GitHub.
1. Clic **[!UICONTROL Save Settings]**.

Al termine, nella pagina dei dettagli dell&#39;app di GitHub Identity verranno elencati l&#39;ID client dell&#39;app (Chiave di consumo) e il Segreto cliente (Segreto di consumo) per l&#39;utilizzo nella pagina Impostazioni integrazione di Studio.
