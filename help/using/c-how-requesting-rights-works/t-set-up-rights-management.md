---
description: Definite le impostazioni per richiedere i diritti per i post di Instagram e Twitter.
seo-description: Definite le impostazioni per richiedere i diritti per i post di Instagram e Twitter.
seo-title: Configurare Rights Management
solution: Experience Manager
title: Configurare Rights Management
uuid: 3ffcbc95-484f-4eba-b817-658c1d658bf8
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Configurare Rights Management{#set-up-rights-management}

Definite le impostazioni per richiedere i diritti per i post di Instagram e Twitter.

Prima di poter definire le impostazioni delle richieste di diritti, dovete configurare uno o più account social per Instagram o Twitter. Per ulteriori informazioni su come configurare un account social, consultate [Aggiungere un account](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/t-configure-social-accout-instagram.md#t_configure_social_accout_instagram)social.

>[!NOTE]
>
>Puoi configurare la gestione dei diritti solo a livello di rete. Non potete configurare la gestione dei diritti specifica per il sito.

1. In Livefyre Studio, andate a **[!UICONTROL Network]****[!UICONTROL Settings > Rights Management]**.

   >[!NOTE]
   >
   >Per impostare gli account Rights Management, è necessario disporre delle autorizzazioni a livello di rete di Moderatore o Amministratore.

1. Selezionate **[!UICONTROL +Add New Account]** se non avete configurato alcun account Rights Management.
1. Fate clic **[!UICONTROL Create New Setting]** sotto il social network che desiderate utilizzare per Rights Management.

   >[!NOTE]
   >
   >Per gli account Instagram, è necessario disporre di un account aziendale Instagram per richiedere i diritti con automazione parziale. Per ulteriori informazioni sui diversi tipi di account Instagram e su come utilizzarli, consultate [Informazioni sugli account](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)Instagram.

1. Compila i campi visualizzati. Tutti i campi sono obbligatori.

   * **[!UICONTROL Display name:]** Immettete un nome visualizzato per identificare l’account Twitter o Instagram da utilizzare per l’account Richiesta diritti. Questo nome è solo interno.
   * **[!UICONTROL Enabled:]**Impostare su attivato per impostazione predefinita. Abilita la gestione dei diritti per l’account.
   * **[!UICONTROL Approval hashtag:]** L'hashtag usato dal proprietario del contenuto per indicare che acconsente a utilizzare il contenuto.
   * **[!UICONTROL Terms and conditions:]** Collegamento alle Condizioni generali della rete per il riutilizzo dei contenuti. Questo campo fa distinzione tra maiuscole e minuscole.
   * **[!UICONTROL Network and sites:]** La rete o il sito per il quale questo account può richiedere diritti di riutilizzo del contenuto. Per rendere questo account disponibile in tutta la rete, selezionare il primo elemento nell'elenco o limitare a siti specifici utilizzando il tasto Comando/CTRL.
   * **[!UICONTROL Default message:]** Un messaggio da visualizzare con la richiesta dei diritti. Puoi ignorare questo messaggio quando richiedi i diritti.

      * Livefyre presenta uno dei messaggi predefiniti ai moderatori quando un moderatore invia una richiesta a un autore di contenuto. I moderatori possono generare un altro messaggio predefinito o modificare il messaggio prima dell'invio. I messaggi devono includere l'handle Twitter o Instagram dell'autore ({handle}), l'hashtag di approvazione ({GrantTag}) e un collegamento ai Termini e Condizioni ({termLink}).

         **[!UICONTROL Note:]** {handle}, {GrantTag} e {termLink} sono tutti con distinzione tra maiuscole e minuscole.

         **[!UICONTROL Note:]** Per evitare un uso dannoso, Twitter racchiude qualsiasi URL incluso con [formattazione t.co](https://t.co/) . Per evitare che il messaggio predefinito superi i 140 caratteri, Livefyre consiglia di non includere gli URL nel messaggio predefinito.

      * Procedure ottimali per la scrittura di messaggi di richiesta di diritti:

         * Crea più messaggi predefiniti in modo da non sembrare un robot. Salva ciascun messaggio predefinito prima di creare il messaggio predefinito successivo.
         * Incoraggiate i moderatori a personalizzare questa nota prima dell'invio, per evitare che alle richieste della rete venga assegnato il tag Spam.

1. Fate clic **[!UICONTROL Save Settings]** per aggiungere il vostro account Rights Request.
Inviate una richiesta di diritti dalla Libreria risorse. Consultate [Inviare una richiesta](../c-how-requesting-rights-works/t-send-a-rights-request-to-own-a-digital-asset.md#t_send_a_rights_request_to_own_a_digital_asset) di diritti per ulteriori informazioni su come inviare una richiesta di diritti dalla Libreria risorse.