---
description: Puoi utilizzare Livefyre Identity con Twitter per consentire agli utenti di utilizzare i loro accessi Twitter per interagire con le app sul tuo sito.
title: Creare un’app Twitter da utilizzare con Livefyre Identity
exl-id: 4f2b919f-fe5d-49a3-8432-04ffb3d68ce4
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# Creare un&#39;app Twitter da utilizzare con Livefyre Identity{#create-a-twitter-app-for-use-with-livefyre-identity}

Puoi utilizzare Livefyre Identity con Twitter per consentire agli utenti di utilizzare i loro accessi Twitter per interagire con le app sul tuo sito.

Per abilitare l&#39;accesso a Twitter, Livefyre richiede le seguenti informazioni sull&#39;app Twitter:

* Chiave consumatore (chiave API)
* Segreto consumatore (segreto API)

Per creare un’app Twitter da utilizzare con Livefyre Identity:

1. Vai su [https://apps.twitter.com/](https://apps.twitter.com/) e accedi al tuo account Twitter per creare una nuova app o selezionane una esistente da utilizzare con Livefyre Identity.
1. Dalla pagina Impostazioni dell’app:

   * Inserisci **[!UICONTROL Callback URL:]** `https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/twitter_fyre` (dove **{networkName}** è il nome di rete fornito da Livefyre. Ad esempio:** [!UICONTROL labs]** in **[!UICONTROL `labs.fyre.co`]**.)
   * Deselezionare **[!UICONTROL Enable Callback Locking]**.
   * Seleziona **[!UICONTROL Allow this application to be used to Sign in with Twitter]**.

1. Dalla scheda **[!UICONTROL Permissions]** , seleziona **[!UICONTROL Access: Read only]**.

Una volta completata, la pagina Gestione applicazione > Chiavi e token di accesso di Twitter elencherà la chiave consumer (chiave API) e il segreto consumatore dell’app (segreto API) per l’utilizzo nella pagina Impostazioni integrazione di Studio.
