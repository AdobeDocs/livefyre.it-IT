---
description: Per abilitare un login mediante social network, utilizzate Studio per
  aggiungere le credenziali delle app social all'integrazione di Livefyre e personalizzate
  il modale di accesso.
seo-description: Per abilitare un login mediante social network, utilizzate Studio
  per aggiungere le credenziali delle app social all'integrazione di Livefyre e personalizzate
  il modale di accesso.
seo-title: Utilizzo di Studio per collegare le app social all'implementazione di Livefyre
title: Utilizzo di Studio per collegare le app social all'implementazione di Livefyre
uuid: be 14869 c-e 0 df -48 cd-a 1 f 3-99 eb 953 dd 9 ce
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Utilizzo di Studio per collegare le app social all'implementazione di Livefyre{#using-studio-to-connect-your-social-apps-to-your-livefyre-implementation}

Per abilitare un login mediante social network, utilizzate Studio per aggiungere le credenziali delle app social all'integrazione di Livefyre e personalizzate il modale di accesso.

## Personalizzazione della modale di accesso {#section_v4c_hv2_3z}

Il modale di accesso consente di personalizzare le informazioni che gli utenti vedranno quando accedono alle app. Potete personalizzare la finestra modale.

* **Logo:** Caricate un logo da usare nei vostri metodi di accesso.
* **Famiglia di font:** Selezionate un font che corrisponda al vostro marchio.
* **Colore marchio:** Immettete un colore esadecimale da usare per il testo specifico nel modale.
* **URL termini e condizioni:** Immettete l'URL per la pagina Condizioni generali della vostra azienda. Questo campo è necessario per l'utilizzo con Livefyre Identity.

## Traduzione di Livefyre Identity {#section_xxt_z52_3z}

In Identità Livefyre potete creare e modificare i set di conversione per le stringhe di testo.

Consultate Set di traduzioni per ulteriori informazioni sull'uso dei set di traduzione con Livefyre Identity.

Per ulteriori informazioni sulle stringhe specifiche che potete personalizzare per Livefyre Identity, consultate Identità Livefyre.

## Abilita login con e-mail {#section_dlv_wzt_bbb}

Consentire agli utenti di utilizzare i propri indirizzi e-mail per accedere e interagire con app sul sito.

Per abilitare l'accesso con un account nativo Livefyre:

1. Andate a **[!UICONTROL Integration Settings]** Livefyre Studio.
1. Attivate l' **[!UICONTROL Enable Login with Email]****[!UICONTROL On]**interruttore.

## Abilitare l'accesso con un account Facebook {#section_ph3_515_bbb}

Collegate l'account Facebook a Livefyre per consentire agli utenti di utilizzare i propri accessi Facebook per interagire con le app sul vostro sito.

Per abilitare l'accesso con un account Facebook:

1. Attivate l' **[!UICONTROL Enable Login with Facebook]****[!UICONTROL ON]**interruttore.

1. Add your Facebook app’s **[!UICONTROL App ID]** and **[!UICONTROL App Secret]**.

   Questi valori sono elencati nel dashboard sviluppatori di Facebook per l'app, disponibile da [https://developers.facebook.com/apps/](https://developers.facebook.com/apps/675503539257343/dashboard/).

## Abilitare l'accesso con Google {#section_fq3_kb5_bbb}

Collegate l'account Google + a Livefyre per consentire agli utenti di utilizzare i propri accessi Google + per interagire con le app sul sito.

Per abilitare l'accesso con un account Google +:

1. Attivate l' **[!UICONTROL Enable Login with Google]****[!UICONTROL ON]**interruttore.

1. Add your Google app’s **[!UICONTROL Client ID]** and **[!UICONTROL Client secret]**.

   Questi valori sono elencati nell'interfaccia del progetto Google Cloud Platform, disponibile da [https://console.cloud.google.com/](https://console.cloud.google.com/apis/library). Per recuperare queste informazioni, accedete e **[!UICONTROL API Manager > Credentials]**fate clic sul nome del progetto.

## Attivare un login con un account Twitter {#section_iyz_wb5_bbb}

Collegate l'account Twitter a Livefyre per consentire agli utenti di utilizzare i propri accessi Twitter per interagire con le app sul sito.

Per abilitare l'accesso con un account Twitter:

1. Attivate l' **[!UICONTROL Enable Login with Twitter]****[!UICONTROL ON]**interruttore.

1. Add your Twitter app’s **[!UICONTROL Consumer Key (API Key)]** and **[!UICONTROL Consumer Secret (API Secret)]**.

   Questi valori sono elencati nella **[!UICONTROL Keys and Access Tokens]** pagina dell'app Twitter, disponibile da [https://apps.twitter.com/](https://apps.twitter.com/).

## Abilitare l'accesso con Yahoo! Account {#section_s1q_3c5_bbb}

Connect Your Yahoo! a Livefyre per consentire agli utenti di utilizzare il proprio Yahoo! login per interagire con App sul sito.

Per abilitare l'accesso con Yahoo! account:

1. Attivate l' **[!UICONTROL Enable Login with Yahoo!]****[!UICONTROL ON]**interruttore.

1. Aggiungi il tuo Yahoo! dell'app **[!UICONTROL Client ID]** e **[!UICONTROL Client Secret]**.

   Questi valori sono elencati in Yahoo! pagina dei dettagli dell'app, disponibile da [developer.yahoo.com/apps](https://developer.yahoo.com/apps).

## Abilitare l'accesso con un account Microsoft Live {#section_z42_4c5_bbb}

Collegate l'account ID Live a Livefyre per consentire agli utenti di utilizzare i propri accessi ID Live per interagire con le app sul sito.

Per abilitare l'accesso con un account ID Live:

1. In **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > Microsoft Live]**, attivate l' **[!UICONTROL Enable Microsoft Live Login]****[!UICONTROL On]**interruttore.

1. Immettete l' **[!UICONTROL Microsoft Live Client ID (Private Key)]** e **[!UICONTROL Microsoft Live Client Secret (Password)]**.

1. Fate clic **[!UICONTROL Save Settings]**su.

   I **[!UICONTROL Microsoft Live Client ID (Private Key)]** valori e **[!UICONTROL Microsoft Live Client Secret (Password)]** sono elencati nella pagina dei dettagli dell'app ID Live di Microsoft Live.

## Collegate le app social a Livefyre Identity {#section_on2_vc5_bbb}

Consentite agli utenti di utilizzare l'implementazione dell'identità Livefyre per le app sul sito.

1. Create un'app.
1. Passa a **[!UICONTROL Studio]** > **[!UICONTROL Settings]** > **[!UICONTROL Integration Settings]**> **[!UICONTROL Livefyre Identity]**.

1. Immettete le credenziali App richieste per l'app creata.