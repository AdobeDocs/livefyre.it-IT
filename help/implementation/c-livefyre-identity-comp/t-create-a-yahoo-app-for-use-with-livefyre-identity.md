---
description: Potete utilizzare Livefyre Identity con Yahoo! per consentire agli utenti
  di utilizzare il proprio Yahoo! login per interagire con App sul sito.
seo-description: Potete utilizzare Livefyre Identity con Yahoo! per consentire agli
  utenti di utilizzare il proprio Yahoo! login per interagire con App sul sito.
seo-title: Create un Yahoo! App da utilizzare con Livefyre Identity
solution: Experience Manager
title: Create un Yahoo! App da utilizzare con Livefyre Identity
uuid: 6863 cd 2 e-eb 0 d -465 b-b 706-88 ecaccf 41 bc
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Create un Yahoo! App da utilizzare con Livefyre Identity{#create-a-yahoo-app-for-use-with-livefyre-identity}

Potete utilizzare Livefyre Identity con Yahoo! per consentire agli utenti di utilizzare il proprio Yahoo! login per interagire con App sul sito.

Per consentire agli utenti di accedere con le credenziali Yahoo, Livefyre richiede le seguenti informazioni sull'app Yahoo:

* ID client (chiave consumatore)
* Segreto cliente (Segreto consumatore)

Per creare un aahoo! app da utilizzare con Livefyre Identity:

1. Andate a [https://developer.yahoo.com/apps/](https://developer.yahoo.com/apps/)e accedete al vostro Yahoo! per creare un nuovo o selezionare un'app esistente da utilizzare con Livefyre Identity.
1. Seleziona **[!UICONTROL Application Type: Web Application]**.
1. Immetti **[!UICONTROL Callback Domain:]**`https://identity.livefyre.com`
1. Selezionate **[!UICONTROL API Permissions: Profiles (Social Directory)]** e **[!UICONTROL Read Public]**.

   Al termine, la pagina dei dettagli dell'app di Yahoo indicherà l'ID client dell'app (Chiave consumatore) e Segreto cliente (Segreto consumatore) da utilizzare nella pagina Impostazioni integrazione di Studio.

   >[!NOTE]
   >
   >Se abilitate Yahoo! accedere senza creare un aahoo! e se in Studio lasciate vuoto i campi ID client e Segreto cliente, Livefyre utilizzerà openid per registrare questi utenti nelle app di Livefyre. Oauth e personalizzazione personalizzata non saranno disponibili in questo caso.