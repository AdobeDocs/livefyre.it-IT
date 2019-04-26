---
description: Potete utilizzare Livefyre Identity con Microsoft Live Identity per consentire
  agli utenti di utilizzare i propri accessi Facebook per interagire con le app sul
  vostro sito.
seo-description: Potete utilizzare Livefyre Identity con Microsoft Live Identity per
  consentire agli utenti di utilizzare i propri accessi Facebook per interagire con
  le app sul vostro sito.
seo-title: Creare un'app identità Microsoft Live da utilizzare con Livefyre Identity
solution: Experience Manager
title: Creare un'app identità Microsoft Live da utilizzare con Livefyre Identity
uuid: 0 c 13 e 1 bc -817 f -43 ed -85 d 5-09 c 9 e 95 b 6234
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Creare un'app identità Microsoft Live da utilizzare con Livefyre Identity{#create-a-microsoft-live-identity-app-for-use-with-livefyre-identity}

Potete utilizzare Livefyre Identity con Microsoft Live Identity per consentire agli utenti di utilizzare i propri accessi Facebook per interagire con le app sul vostro sito.

Per consentire agli utenti di accedere con le credenziali Identità live Microsoft, Livefyre richiede le seguenti informazioni identità live Microsoft:

* ID client (chiave privata)
* Segreto cliente (password)

Per creare un'app di identità Microsoft Live da utilizzare con Livefyre Identity:

1. Create o accedete a un account Microsoft Live all'indirizzo [https://apps.dev.microsoft.com](https://apps.dev.microsoft.com/)
1. Create una nuova o selezionate un'app esistente da utilizzare con Livefyre Identity.
1. Fate clic **[!UICONTROL Add Platform]**su, quindi selezionate Web come tipo di piattaforma.
1. Verificate che l **[!UICONTROL Allow Implicit Flow]** 'opzione sia selezionata e immettete l'URL di reindirizzamento, utilizzando il nome di rete invece di {network-name}: `https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/mslive_fyre`.
1. Generate una nuova coppia password/chiave per ottenere la chiave privata.
1. In **[!UICONTROL Livefyre Integration Settings Livefyre Identity Microsoft Live]**, attivate l' **[!UICONTROL Enable Microsoft Live Login]****[!UICONTROL On]**interruttore.
1. Immettete l'ID client Microsoft Live e Microsoft Live Client Secret.
1. Fate clic **[!UICONTROL Save Settings]**su.

Una volta completato, la pagina dei dettagli dell'app di Microsoft Live Identity includerà l'ID client dell'app (Chiave consumatore) e Segreto cliente (Segreto consumatore) da utilizzare nella pagina Impostazioni integrazione di Studio.
