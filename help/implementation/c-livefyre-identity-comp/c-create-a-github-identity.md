---
description: Potete utilizzare Livefyre Identity con identità github per consentire
  agli utenti di utilizzare i propri accessi github per interagire con le app sul
  sito.
seo-description: Potete utilizzare Livefyre Identity con identità github per consentire
  agli utenti di utilizzare i propri accessi github per interagire con le app sul
  sito.
seo-title: Creare un'app identità github da utilizzare con Livefyre Identity
title: Creare un'app identità github da utilizzare con Livefyre Identity
uuid: cf 56164 c -1521-4 a 42-89 cb -39483764807 e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Creare un'app identità github da utilizzare con Livefyre Identity{#create-a-github-identity-app-for-use-with-livefyre-identity}

Potete utilizzare Livefyre Identity con identità github per consentire agli utenti di utilizzare i propri accessi github per interagire con le app sul sito.

Per consentire agli utenti di accedere con le credenziali identità github, Livefyre richiede le seguenti informazioni identità github:

* ID client (chiave privata)
* Segreto cliente (password)

Per creare un'app identità github da utilizzare con Livefyre Identity:

1. Create o accedete a un account github in [](https://github.com/settings/developers).
1. Registrate una nuova o selezionate un'app esistente da utilizzare con Livefyre Identity.
1. Immettere tutte le informazioni sul modulo. Immettete il **[!UICONTROL Authorization callback URL]**nome di rete, anziché `{network-name}: {network-name}: https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/github_fyre`il nome.

1. In **[!UICONTROL Livefyre Integration Settings Livefyre Identity GitHub]**, attivate l' **[!UICONTROL Enable GitHub Login]****[!UICONTROL On]**interruttore.

1. Immettete l'ID client github e il segreto cliente github.
1. Fate clic **[!UICONTROL Save Settings]**su.

Una volta completato, la pagina dei dettagli dell'app github visualizza l'ID client dell'app (Chiave consumatore) e Segreto cliente (Segreto consumatore) da utilizzare nella pagina Impostazioni integrazione di Studio.
