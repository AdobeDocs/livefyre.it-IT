---
description: Consente agli utenti di selezionare la frequenza e il contenuto delle notifiche.
seo-description: Consente agli utenti di selezionare la frequenza e il contenuto delle notifiche.
seo-title: Notifiche e-mail
solution: Experience Manager
title: Notifiche e-mail
uuid: 27dad133-bd8d-4949-8146-1254c160d3af
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Notifiche e-mail{#email-notifications}

Consente agli utenti di selezionare la frequenza e il contenuto delle notifiche.

**Abilita notifiche e-mail per utenti e moderatori.**

Le app Livefyre consentono di abilitare le notifiche e-mail per utenti e moderatori, in base ad azioni specifiche. Le notifiche si basano sull'ora in cui il contenuto viene pubblicato nel flusso, consentendo agli utenti di rimanere coinvolti nelle conversazioni che gli interessano e di ricevere notifiche quando qualcuno gradisce o risponde a uno dei loro commenti.

Gli utenti e i moderatori possono scegliere se accettare o rifiutare le notifiche e-mail e impostare la frequenza con cui vengono ricevute le e-mail. Questa sezione descrive come configurare e personalizzare queste notifiche e-mail.

* Opzioni e-mail utente: opzioni di notifica utente disponibili.
* Opzioni e-mail moderatore: opzioni di notifica del moderatore disponibili.
* Opzioni e-mail identità Livefyre: e-mail inviate come parte dell'identità Livefyre. Questi messaggi e-mail sono pertinenti solo per i clienti Livefyre Identity.
* Sincronizzazione dati con Livefyre: mantenere la sincronizzazione delle preferenze con Livefyre.
* Personalizzazione delle e-mail: personalizzazioni e-mail disponibili.

Utilizzate le opzioni **Impostazioni &gt; Impostazioni integrazione &gt; Impostazione** notifiche e-mail per personalizzare le notifiche e-mail per la rete.

>[!NOTE]
>
>Per garantire che gli utenti finali non ricevano e-mail non desiderate, non vengono inviate notifiche e-mail dall'ambiente UAT di Livefyre.

**Opzioni e-mail utente**

Livefyre consente agli utenti di ricevere notifiche e-mail relative alle attività del sito. Utilizzate le impostazioni di integrazione del profilo utente fornite da Livefyre per consentire agli utenti di selezionare le proprie preferenze per le pianificazioni delle notifiche.

>[!NOTE]
>
>Le e-mail vengono inviate solo per il contenuto pubblicato manualmente nel flusso e non per il contenuto estratto da SocialSync.

Per consentire agli utenti di impostare le proprie preferenze di notifica, includete una sezione Notifica e-mail nelle Impostazioni utente per il sistema del profilo utente. Aggiungete i campi corrispondenti allo schema del database del profilo utente, quindi gestite le impostazioni utente utilizzando Ping for Pull. (utilizzate Technical Integration Manager per definire le frequenze predefinite per la rete. Se siete clienti Enterprise Profiles, passate i valori predefiniti selezionati al team di distribuzione Livefyre per la configurazione nel database Livefyre.

Gli utenti del sito possono quindi seguire una conversazione e iniziare a ricevere notifiche e-mail facendo clic sul **[!UICONTROL +Follow]** pulsante nell’editor dei commenti. Le preferenze di notifica sono definite a livello di rete Livefyre. Qualsiasi impostazione utente si applica a tutti i siti e le conversazioni della rete.

**Valori predefiniti consigliati**

* Qualcuno commenta in una conversazione che sto seguendo:** digest orario**
* A qualcuno piace uno dei miei commenti:** digest orario**
* Qualcuno risponde a uno dei miei commenti:** immediatamente**
* Seguire automaticamente le conversazioni quando lascio un commento:** disattivato* (non selezionato)

**Nota**: Le notifiche e-mail si basano sull'ora in cui il contenuto è approvato per l'inclusione nel flusso.

Livefyre offre due opzioni di frequenza e-mail:

* Immediatamente
* Riepilogo orario

**Immediatamente**

Le e-mail inviate visualizzano immediatamente il testo del post, il titolo dell'articolo, il nome utente dell'autore e un collegamento **Rispondi** che porta l'utente al contenuto della pagina. Questi messaggi e-mail includono anche un collegamento per l' **annullamento della sottoscrizione** nel piè di pagina, che consente agli utenti di annullare la sottoscrizione alle notifiche e-mail relative a tale raccolta. Facendo clic su **unsubscription **i partecipanti verranno indirizzati a una pagina di conferma per informarli che è stato annullato l'abbonamento alla raccolta.

**Riepilogo orario**

Le e-mail inviate in un riassunto orario visualizzano tutti i contenuti, le risposte ai contenuti e i like sul contenuto nell'ultima ora (o giù di lì) per l'app che l'utente sta seguendo. Se l'utente sta seguendo più app nella rete, riceverà un'e-mail digest per ciascuna app.

>[!NOTE]
>
>Nelle conversazioni senza nuovi contenuti per più ore, gli utenti con digest orario abilitato riceveranno un avviso immediatamente dopo un nuovo post di contenuto.

**Opzioni e-mail moderatore**

I moderatori possono scegliere di ricevere e-mail per il contenuto pubblicato in un'app che stanno seguendo e per i commenti contrassegnati come Spam o Offensive in un'app che stanno moderando. **** Nota: Non verrà inviata alcuna e-mail quando gli utenti contrassegnano un commento con Non d'accordo o Disattivato, in quanto queste categorie non sono considerate importanti per la notifica del moderatore.

I campi moderator_comments e moderator_flags devono essere aggiunti anche allo schema di database delle impostazioni del profilo utente del moderatore per consentire ai moderatori di aggiornare la frequenza delle notifiche e-mail e di rifiutare se lo desiderano. Livefyre consiglia di impostare questi due campi di notifica e-mail per moderatori in modo che **non vengano mai** impostati. Le opzioni includono **mai** (predefinito), **immediatamente** e **spesso**.

**E-mail moderatore (contenuto contrassegnato):**

Quando il contenuto viene contrassegnato in un'app moderata, l'e-mail inviata al moderatore mostra il contenuto contrassegnato, il nome utente che ha segnalato il contenuto e un collegamento alla pagina del contenuto.

Quando un utente modifica le proprie preferenze di notifica e-mail sul sito nel sistema del profilo, sincronizzate l’aggiornamento al sistema del profilo remoto Livefyre utilizzando il ping for Pull di Livefyre.

**Sincronizzazione dei dati con Livefyre**

## Personalizzazione delle e-mail {#section_jxb_c5k_yy}

Diversi campi nei modelli di notifica e-mail possono essere modificati per adattarli allo stile e al marchio.

* **[!UICONTROL From Email Address]**

   L'"indirizzo e-mail del mittente" per tutte le notifiche e-mail può essere personalizzato per essere coerente con il tuo marchio. Livefyre consiglia di **noreply@customerdomain.com**, sostituendo **** il dominio personalizzato con il nome di dominio. Il valore predefinito è **noreply@livefyre.com**. Trasmettete il vostro "da indirizzo e-mail" preferito al vostro Technical Integration Manager per la configurazione nel database Livefyre per la rete.

   >[!NOTE]
   >
   >Lasciate vuoto questo campo per disabilitare le notifiche e-mail per la rete

* **[!UICONTROL Email Logo]**

   Il logo visualizzato nelle notifiche e-mail può essere personalizzato per visualizzare il logo aziendale, anziché il logo Livefyre predefinito, utilizzando la scheda Branding della pagina Impostazioni **di** rete di Studio. Questa personalizzazione è disponibile solo a livello di rete, non a livello di sito, ed è disponibile solo per i clienti Livefyre a pagamento.

* **[!UICONTROL Custom Templates]**

   È possibile implementare un modello e-mail completamente personalizzato, se lo desiderate. Tuttavia, ciò richiederà un certo sforzo di sviluppo e potrebbe comportare costi per i servizi professionali. Contattate il vostro Account Manager per informazioni dettagliate.



App che utilizzano questa funzione:

* [Carosello](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Commenti](/help/using/c-about-apps/c-comments/c-comments.md)
* [Scheda](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Muro di supporto](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Recensioni](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)

