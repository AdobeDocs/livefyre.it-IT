---
description: Definite le impostazioni per la richiesta di diritti per i post di Instagram
  e Twitter.
seo-description: Definite le impostazioni per la richiesta di diritti per i post di
  Instagram e Twitter.
seo-title: Configurare Rights Management
solution: Experience Manager
title: Configurare Rights Management
uuid: 3 ffcbc 95-484 f -4 eba-b 817-658 c 1 d 658 bf 8
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Configurare Rights Management{#set-up-rights-management}

Definite le impostazioni per la richiesta di diritti per i post di Instagram e Twitter.

Prima di definire le Impostazioni richieste di diritti, dovete configurare uno o più account sociali per Instagram o Twitter. Per ulteriori informazioni su come configurare un account social, consultate [Aggiungere un account social](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/t-configure-social-accout-instagram.md#t_configure_social_accout_instagram).

>[!NOTE]
>
>Potete configurare la gestione dei diritti solo a livello di rete. Non potete configurare la gestione dei diritti specifica per il sito.

1. In Livefyre Studio, andate a **[!UICONTROL Network]****[!UICONTROL Settings > Rights Management]**.

   >[!NOTE]
   >
   >Per configurare gli account Rights Management, dovrete disporre delle autorizzazioni a livello di rete Moderatore o Amministratori.

1. Selezionate **[!UICONTROL +Add New Account]** se non avete impostato nessun account Rights Management.
1. Fate clic **[!UICONTROL Create New Setting]** sotto la rete social che desiderate utilizzare per Rights Management.

   >[!NOTE]
   >
   >Per gli account Instagram, devi disporre di un account business di Instagram per richiedere i diritti con automazione parziale. Per ulteriori informazioni sui diversi tipi di account Istagram e su come utilizzarli, consultate [Informazioni su Account Instagram](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

1. Compila i campi visualizzati. Tutti i campi sono obbligatori.

   * **[!UICONTROL Display name:]** Immettete un nome per identificare l'account di Twitter o Instagram da utilizzare per l'account Richiesta diritti. Questo nome è interno.
   * ****[!UICONTROL Enabled:]Attivata per impostazione predefinita. Abilita la gestione dei diritti per l'account.
   * **[!UICONTROL Approval hashtag:]** L'hashtag che verrà utilizzato dal proprietario del contenuto per indicare che il contenuto è autorizzato a utilizzare il contenuto.
   * **[!UICONTROL Terms and conditions:]** Collegamento ai termini e condizioni della rete per il riutilizzo del contenuto. Questo campo fa distinzione tra maiuscole e minuscole.
   * **[!UICONTROL Network and sites:]** Rete o sito per il quale questo account può richiedere diritti di riutilizzo del contenuto. Per rendere disponibile questo account nell'intera rete, seleziona il primo elemento nell'elenco o limiti a siti specifici utilizzando il tasto Comando/CTRL.
   * **[!UICONTROL Default message:]** Messaggio da visualizzare con la richiesta diritti. Potete ignorare questo messaggio quando richiedete i diritti.

      * Livefyre presenta uno dei messaggi predefiniti ai moderatori quando un moderatore invia una richiesta a un autore di contenuto. I moderatori possono generare un altro messaggio predefinito o modificare il messaggio prima dell'invio. I messaggi devono includere la handle di Twitter o Instagram dell'autore ({handle}), l'hashtag di approvazione ({granttag}) e un collegamento ai Termini e alle condizioni ({termslink}).

         **[!UICONTROL Note:]** {handle}, {granttag} e {termslink} sono tutti con distinzione tra maiuscole e minuscole.

         **[!UICONTROL Note:]** Per impedire l'uso dannoso, Twitter racchiude gli URL inclusi con [la formattazione t. co](https://t.co/) . Per evitare che il messaggio predefinito superi i 140 caratteri, Livefyre consiglia di includere gli URL nel messaggio predefinito.

      * Procedure ottimali per la scrittura dei messaggi di richiesta dei diritti:

         * Crea più messaggi predefiniti in modo da non suonare come un robot. Salva ogni messaggio predefinito prima di creare il messaggio predefinito successivo.
         * Incoraggiate i moderatori a personalizzare questa nota prima dell'invio, per evitare che le richieste della rete vengano sottoposte a tag Spam.

1. Fate clic per **[!UICONTROL Save Settings]** aggiungere l'account Request Request (Richiesta rights).
Inviare una richiesta di diritti dalla Libreria risorse. Per informazioni su come inviare una richiesta di diritti dalla Libreria risorse, consultate [Inviare una richiesta](../c-how-requesting-rights-works/t-send-a-rights-request-to-own-a-digital-asset.md#t_send_a_rights_request_to_own_a_digital_asset) di Rights Request.