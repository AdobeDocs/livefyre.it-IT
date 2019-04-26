---
description: Potete utilizzare Livefyre Identity con Twitter per consentire agli utenti
  di utilizzare i propri accessi Twitter per interagire con le app sul sito.
seo-description: Potete utilizzare Livefyre Identity con Twitter per consentire agli
  utenti di utilizzare i propri accessi Twitter per interagire con le app sul sito.
seo-title: Creare un'app Twitter da utilizzare con Livefyre Identity
solution: Experience Manager
title: Creare un'app Twitter da utilizzare con Livefyre Identity
uuid: 841 cce 7 c -618 d -4154-85 a 3-1 de 96 d 04 bb 69
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Creare un'app Twitter da utilizzare con Livefyre Identity{#create-a-twitter-app-for-use-with-livefyre-identity}

Potete utilizzare Livefyre Identity con Twitter per consentire agli utenti di utilizzare i propri accessi Twitter per interagire con le app sul sito.

Per abilitare l'accesso Twitter, Livefyre richiede le seguenti informazioni sull'app Twitter:

* Chiave consumer (chiave API)
* Segreto consumatore (Segreto API)

Per creare un'app Twitter da utilizzare con Livefyre Identity:

1. Andate a [https://apps.twitter.com/](https://apps.twitter.com/)e accedete al vostro account Twitter per creare una nuova app o selezionate un'app esistente da utilizzare con Livefyre Identity.
1. Dalla pagina Settings (Impostazioni) dell'app:

   * Immettete ( **[!UICONTROL Callback URL:]**`https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/twitter_fyre` dove **{networkname}** è il nome di rete fornito da Livefyre). Ad esempio: ** [!UICONTROL labs]** in **[!UICONTROL `labs.fyre.co`]**.)
   * Deseleziona **[!UICONTROL Enable Callback Locking]**.
   * Seleziona **[!UICONTROL Allow this application to be used to Sign in with Twitter]**.

1. Dalla **[!UICONTROL Permissions]** scheda, selezionate **[!UICONTROL Access: Read only]**.

Al termine, la pagina Gestione applicazione Twitter > Chiavi e accesso ai token visualizzerà il tasto Consumer (Chiave API) dell'app e il Segreto cliente (Segreto API) per l'utilizzo nella pagina Impostazioni integrazione di Studio.
