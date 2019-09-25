---
description: Per abilitare un accesso tramite social network, utilizzate Studio per aggiungere le credenziali delle vostre app per social network all'integrazione Livefyre e personalizzate il metodo di accesso.
seo-description: Per abilitare un accesso tramite social network, utilizzate Studio per aggiungere le credenziali delle vostre app per social network all'integrazione Livefyre e personalizzate il metodo di accesso.
seo-title: Utilizzo di Studio per collegare le app Social all'implementazione Livefyre
title: Utilizzo di Studio per collegare le app Social all'implementazione Livefyre
uuid: be14869c-e0df-48cd-a1f3-99eb953dd9ce
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Utilizzo di Studio per collegare le app Social all'implementazione Livefyre{#using-studio-to-connect-your-social-apps-to-your-livefyre-implementation}

Per abilitare un accesso tramite social network, utilizzate Studio per aggiungere le credenziali delle vostre app per social network all'integrazione Livefyre e personalizzate il metodo di accesso.

## Personalizzazione del metodo di login {#section_v4c_hv2_3z}

La modalità di accesso consente di personalizzare le informazioni che gli utenti vedranno al momento dell'accesso alle app. È possibile personalizzare la finestra modale.

* **** Logo: Caricate un logo da usare nei modelli di accesso.
* **** Famiglia font: Selezionate un font che corrisponda al marchio.
* **** Colore marchio: Immettete un colore esadecimale da usare per testo specifico all’interno del modale.
* **** URL termini e condizioni: Immettete l’URL della pagina Condizioni generali della società. Questo campo è obbligatorio per l'uso con l'identità Livefyre.

## Traduzione dell'identità Livefyre {#section_xxt_z52_3z}

Potete creare e modificare i set di conversione per le stringhe di testo in Identità Livefyre.

Consultate Set di traduzioni per ulteriori informazioni sull'utilizzo dei set di traduzioni con Identità Livefyre.

Per ulteriori informazioni sulle stringhe specifiche che è possibile personalizzare per l'identità Livefyre, consultate Identità Livefyre.

## Abilita login con e-mail {#section_dlv_wzt_bbb}

Consentite agli utenti di utilizzare i loro indirizzi e-mail per accedere e interagire con le app sul sito.

Per abilitare l'accesso con un account nativo Livefyre:

1. Andate a **[!UICONTROL Integration Settings]** Livefyre Studio.
1. Passate all’ **[!UICONTROL Enable Login with Email]** interruttore **[!UICONTROL On]**.

## Abilitare il login mediante un account Facebook {#section_ph3_515_bbb}

Collegate l'account Facebook a Livefyre per consentire agli utenti di utilizzare i propri accessi Facebook per interagire con le app sul sito.

Per attivare l’accesso con un account Facebook:

1. Passate all’ **[!UICONTROL Enable Login with Facebook]** interruttore **[!UICONTROL ON]**.

1. Aggiungete l’app Facebook **[!UICONTROL App ID]** e **[!UICONTROL App Secret]**.

   Questi valori sono elencati nel dashboard degli sviluppatori di Facebook per l'app, disponibile da [https://developers.facebook.com/apps/](https://developers.facebook.com/apps/675503539257343/dashboard/).

## Abilita login con Google {#section_fq3_kb5_bbb}

Collegate il vostro account Google+ a Livefyre per consentire agli utenti di utilizzare i loro accessi Google+ per interagire con le app sul sito.

Per abilitare l'accesso con un account Google+:

1. Passate all’ **[!UICONTROL Enable Login with Google]** interruttore **[!UICONTROL ON]**.

1. Aggiungi l’app Google **[!UICONTROL Client ID]** e **[!UICONTROL Client secret]**.

   Questi valori sono elencati nell’interfaccia di progetto della piattaforma Google Cloud, disponibile da [https://console.cloud.google.com/](https://console.cloud.google.com/apis/library). Per recuperare queste informazioni, andate a **[!UICONTROL API Manager > Credentials]** e fate clic sul nome del progetto.

## Abilitare un login mediante un account Twitter {#section_iyz_wb5_bbb}

Collegate il vostro account Twitter a Livefyre per consentire agli utenti di utilizzare i propri accessi Twitter per interagire con le app sul sito.

Per attivare l’accesso con un account Twitter:

1. Passate all’ **[!UICONTROL Enable Login with Twitter]** interruttore **[!UICONTROL ON]**.

1. Aggiungete le app Twitter **[!UICONTROL Consumer Key (API Key)]** e **[!UICONTROL Consumer Secret (API Secret)]**.

   Questi valori sono elencati nella **[!UICONTROL Keys and Access Tokens]** pagina dell'app Twitter, disponibile da [https://apps.twitter.com/](https://apps.twitter.com/).

## Abilita login con un Yahoo! Account {#section_s1q_3c5_bbb}

Connetti il tuo Yahoo! account a Livefyre per consentire agli utenti di utilizzare il loro Yahoo! login per interagire con le app sul sito.

Per abilitare l'accesso con un account Yahoo! account:

1. Passate all’ **[!UICONTROL Enable Login with Yahoo!]** interruttore **[!UICONTROL ON]**.

1. Aggiungi il tuo Yahoo! dell’app **[!UICONTROL Client ID]** e **[!UICONTROL Client Secret]**.

   Questi valori sono elencati nello Yahoo! pagina dei dettagli dell'app, disponibile da [developer.yahoo.com/apps](https://developer.yahoo.com/apps).

## Abilitare il login utilizzando un account Microsoft Live {#section_z42_4c5_bbb}

Collegate l'account Microsoft Live ID a Livefyre per consentire agli utenti di utilizzare i propri accessi Microsoft Live ID per interagire con le app sul sito.

Per abilitare l'accesso con un account Microsoft Live ID:

1. In **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > Microsoft Live]**, passate l’ **[!UICONTROL Enable Microsoft Live Login]** interruttore a **[!UICONTROL On]**.

1. Inserite il **[!UICONTROL Microsoft Live Client ID (Private Key)]** campo e **[!UICONTROL Microsoft Live Client Secret (Password)]**.

1. Fai clic su **[!UICONTROL Save Settings]**.

   I valori **[!UICONTROL Microsoft Live Client ID (Private Key)]** e **[!UICONTROL Microsoft Live Client Secret (Password)]** sono elencati nella pagina dei dettagli dell'app Microsoft Live ID.

## Collegare le app Social all'identità Livefyre {#section_on2_vc5_bbb}

Consentite agli utenti di utilizzare l'implementazione Identità Livefyre per le app sul sito.

1. Creare un'app.
1. Andate a **[!UICONTROL Studio]** &gt; **[!UICONTROL Settings]** &gt; **[!UICONTROL Integration Settings]**&gt; **[!UICONTROL Livefyre Identity]**.

1. Immetti le credenziali app richieste per l'app che hai creato.