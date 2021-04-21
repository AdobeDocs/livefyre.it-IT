---
description: Per abilitare un accesso social, utilizza Studio per aggiungere le credenziali delle tue app social all’integrazione Livefyre e personalizzare il modale di accesso.
title: Utilizzo di Studio per collegare le app Social all’implementazione Livefyre
exl-id: 2ccb9737-8c59-4c1d-93d3-61f913b3cdd6
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# Utilizzo di Studio per collegare le app Social all&#39;implementazione Livefyre{#using-studio-to-connect-your-social-apps-to-your-livefyre-implementation}

Per abilitare un accesso social, utilizza Studio per aggiungere le credenziali delle tue app social all’integrazione Livefyre e personalizzare il modale di accesso.

## Personalizzazione del modale di accesso {#section_v4c_hv2_3z}

Il modale di accesso ti consente di personalizzare le informazioni che gli utenti vedranno al momento di accedere alle tue app. Puoi personalizzare la finestra modale.

* **Logo:** carica un logo da utilizzare nei modelli di accesso.
* **Famiglia di font:** seleziona un font che corrisponda al tuo marchio.
* **Colore marchio:** immetti un colore esadecimale da utilizzare per un testo specifico all’interno del modale.
* **URL termini e condizioni:** inserisci l’URL della pagina Termini e condizioni della tua azienda. Questo campo è necessario per l’utilizzo con Livefyre Identity.

## Traduzione di Livefyre Identity {#section_xxt_z52_3z}

Puoi creare e modificare i set di traduzione per le stringhe di testo in Livefyre Identity.

Per ulteriori informazioni sull’utilizzo dei set di traduzione con Livefyre Identity, consulta Set di traduzione .

Per ulteriori informazioni sulle stringhe specifiche che puoi personalizzare per Livefyre Identity, consulta Livefyre Identity .

## Abilita accesso con e-mail {#section_dlv_wzt_bbb}

Consenti agli utenti di utilizzare i loro indirizzi e-mail per accedere e interagire con le app sul tuo sito.

Per abilitare l’accesso utilizzando un account nativo Livefyre:

1. Passa a **[!UICONTROL Integration Settings]** in Livefyre Studio.
1. Passa l’interruttore **[!UICONTROL Enable Login with Email]** a **[!UICONTROL On]**.

## Abilitare l’accesso utilizzando un account Facebook {#section_ph3_515_bbb}

Collega il tuo account Facebook a Livefyre per consentire agli utenti di utilizzare i loro accessi Facebook per interagire con le app sul tuo sito.

Per abilitare l&#39;accesso utilizzando un account Facebook:

1. Passa l’interruttore **[!UICONTROL Enable Login with Facebook]** a **[!UICONTROL ON]**.

1. Aggiungi i **[!UICONTROL App ID]** e **[!UICONTROL App Secret]** dell’app Facebook.

   Questi valori sono elencati nel dashboard per sviluppatori Facebook per l&#39;app, disponibile da [https://developers.facebook.com/apps/](https://developers.facebook.com/apps/675503539257343/dashboard/).

## Abilita accesso con Google {#section_fq3_kb5_bbb}

Collega il tuo account Google+ a Livefyre per consentire agli utenti di utilizzare i loro accessi a Google+ per interagire con le app sul tuo sito.

Per abilitare l&#39;accesso utilizzando un account Google+:

1. Passa l’interruttore **[!UICONTROL Enable Login with Google]** a **[!UICONTROL ON]**.

1. Aggiungi le **[!UICONTROL Client ID]** e **[!UICONTROL Client secret]** dell’app Google.

   Questi valori sono elencati nell’interfaccia di progetto di Google Cloud Platform, disponibile da [https://console.cloud.google.com/](https://console.cloud.google.com/apis/library). Per recuperare queste informazioni, vai su **[!UICONTROL API Manager > Credentials]** e fai clic sul nome del progetto.

## Abilitare un login utilizzando un account Twitter {#section_iyz_wb5_bbb}

Collega il tuo account Twitter a Livefyre per consentire agli utenti di utilizzare i loro accessi Twitter per interagire con le app sul tuo sito.

Per abilitare l&#39;accesso utilizzando un account Twitter:

1. Passa l’interruttore **[!UICONTROL Enable Login with Twitter]** a **[!UICONTROL ON]**.

1. Aggiungi i **[!UICONTROL Consumer Key (API Key)]** e **[!UICONTROL Consumer Secret (API Secret)]** dell’app Twitter.

   Questi valori sono elencati nella pagina **[!UICONTROL Keys and Access Tokens]** dell’app Twitter, disponibile da [https://apps.twitter.com/](https://apps.twitter.com/).

## Abilita l&#39;accesso utilizzando un Yahoo! Account {#section_s1q_3c5_bbb}

Collega il tuo Yahoo! account a Livefyre per consentire agli utenti di utilizzare il loro Yahoo! accessi per interagire con le app sul sito.

Per abilitare l&#39;accesso utilizzando un Yahoo! account:

1. Passa l’interruttore **[!UICONTROL Enable Login with Yahoo!]** a **[!UICONTROL ON]**.

1. Aggiungi il tuo Yahoo! dell’app **[!UICONTROL Client ID]** e **[!UICONTROL Client Secret]**.

   Questi valori sono elencati in Yahoo! pagina dei dettagli dell&#39;app, disponibile da [developer.yahoo.com/apps](https://developer.yahoo.com/apps).

## Abilitare l&#39;accesso utilizzando un account Microsoft Live {#section_z42_4c5_bbb}

Collega il tuo account Microsoft Live ID a Livefyre per consentire agli utenti di utilizzare i loro accessi a Microsoft Live ID per interagire con le app sul tuo sito.

Per abilitare l&#39;accesso tramite un account Microsoft Live ID:

1. In **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > Microsoft Live]**, imposta l&#39;opzione **[!UICONTROL Enable Microsoft Live Login]** su **[!UICONTROL On]**.

1. Inserisci i valori **[!UICONTROL Microsoft Live Client ID (Private Key)]** e **[!UICONTROL Microsoft Live Client Secret (Password)]**.

1. Clic **[!UICONTROL Save Settings]**.

   I valori **[!UICONTROL Microsoft Live Client ID (Private Key)]** e **[!UICONTROL Microsoft Live Client Secret (Password)]** sono elencati nella pagina dei dettagli dell&#39;app Microsoft Live ID.

## Collegare le app social a Livefyre Identity {#section_on2_vc5_bbb}

Abilita i tuoi utenti a utilizzare la tua implementazione di Livefyre Identity per le app sul tuo sito.

1. Crea un&#39;app.
1. Passa a **[!UICONTROL Studio]** > **[!UICONTROL Settings]** > **[!UICONTROL Integration Settings]** **[!UICONTROL Livefyre Identity]**.

1. Immetti le credenziali dell’app richieste per l’app creata.
