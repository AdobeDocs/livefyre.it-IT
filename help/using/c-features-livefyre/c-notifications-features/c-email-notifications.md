---
description: Consenti agli utenti di selezionare la frequenza e il contenuto delle notifiche.
title: Notifiche e-mail
exl-id: 46821382-ac93-4523-a0ac-84535e76d367
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 0%

---

# Notifiche e-mail{#email-notifications}

Consenti agli utenti di selezionare la frequenza e il contenuto delle notifiche.

**Abilita le notifiche e-mail per i tuoi utenti e moderatori.**

Le app Livefyre ti consentono di abilitare le notifiche e-mail per i tuoi utenti e moderatori, in base ad azioni specifiche. Le notifiche si basano sull’ora in cui il contenuto viene inviato al flusso, consentendo agli utenti di rimanere coinvolti nelle conversazioni di loro interesse, e di essere avvisati quando qualcuno ama o risponde a uno dei loro commenti.

Gli utenti e i moderatori possono scegliere se effettuare o meno la notifica e-mail e possono impostare la frequenza con cui vengono ricevute le e-mail. Questa sezione descrive come configurare e personalizzare queste notifiche e-mail.

* Opzioni e-mail utente: opzioni di notifica utente disponibili.
* Opzioni e-mail moderatore: opzioni di notifica del moderatore disponibili.
* Opzioni E-Mail Di Livefyre Identity: e-mail inviate come parte di Livefyre Identity. Queste e-mail sono pertinenti solo per i clienti Livefyre Identity.
* Sincronizzazione dei dati con Livefyre: mantenere la sincronizzazione delle preferenze con Livefyre.
* Personalizzazione delle e-mail: personalizzazioni e-mail disponibili.

Utilizza le opzioni **Impostazioni > Impostazioni integrazione > Impostazione notifica e-mail** per personalizzare le notifiche e-mail per la tua rete.

>[!NOTE]
>
>Per garantire che gli utenti finali non ricevano e-mail non intenzionali, non vengono inviate notifiche e-mail dall’ambiente Livefyre UAT.

**Opzioni e-mail utente**

Livefyre consente agli utenti di ricevere notifiche e-mail relative all’attività del sito. Utilizza le impostazioni di integrazione del profilo utente fornite da Livefyre per consentire agli utenti di selezionare le loro preferenze per le pianificazioni delle notifiche.

>[!NOTE]
>
>Le e-mail vengono inviate solo per i contenuti inviati manualmente nel flusso e non per i contenuti estratti da SocialSync.

Per consentire agli utenti di impostare le proprie preferenze di notifica, includi una sezione Notifica e-mail nelle Impostazioni utente per il tuo sistema di profilo utente. Aggiungi i campi corrispondenti allo schema del database del profilo utente, quindi gestisci le impostazioni utente utilizzando Ping for Pull. (Collabora con Technical Integration Manager per definire le frequenze predefinite per la rete. Se sei un cliente di Enterprise Profiles, passa i valori predefiniti selezionati al team di consegna Livefyre per la configurazione nel database Livefyre.)

Gli utenti sul tuo sito possono quindi seguire una conversazione e iniziare a ricevere notifiche e-mail facendo clic sul pulsante **[!UICONTROL +Follow]** sull’editor dei commenti. Le preferenze di notifica sono definite a livello di rete Livefyre. Tutte le impostazioni utente verranno applicate a tutti i siti e conversazioni della rete.

**Valori predefiniti consigliati**

* Qualcuno commenta in una conversazione che sto seguendo:** digest orario**
* A qualcuno piace uno dei miei commenti:** digest orario**
* Qualcuno risponde a uno dei miei commenti:** immediatamente**
* Segui automaticamente le conversazioni quando lascio un commento:** off** (non selezionato)

**Nota**: Le notifiche e-mail si basano sull’ora in cui il contenuto è approvato per l’inclusione nel flusso.

Livefyre offre due opzioni di frequenza e-mail:

* Immediatamente
* Digest orario

**Immediatamente**

Le e-mail inviate visualizzano immediatamente il testo del post, il titolo dell’articolo, il nome utente dell’autore e un collegamento **Risposta** che porta l’utente al contenuto della pagina. Queste e-mail includono anche un collegamento **Annulla sottoscrizione** nel piè di pagina, che consente agli utenti di annullare l’iscrizione alle notifiche e-mail per quella raccolta. Facendo clic su **Annulla sottoscrizione **verranno visualizzati in una pagina di conferma per informarli che è stato annullato l’abbonamento alla raccolta.

**Digest orario**

Le e-mail inviate in un riepilogo orario visualizzano tutti i contenuti, le risposte ai contenuti e i Mi piace sul contenuto nell’ultima ora (o giù di lì) per app che l’utente sta seguendo. Se l&#39;utente segue più app nella tua rete, riceverà un&#39;e-mail digest per ogni app.

>[!NOTE]
>
>Nelle conversazioni senza nuovi contenuti per più di diverse ore, gli utenti con digest orario abilitato riceveranno un avviso immediatamente dopo un nuovo post di contenuto.

**Opzioni e-mail moderatore**

I moderatori possono scegliere di ricevere e-mail per i contenuti pubblicati in un’app che stanno seguendo e per i commenti contrassegnati come Spam o Offensive in un’app che stanno moderando. **Nota:** non verrà inviata alcuna e-mail quando gli utenti contrassegnano un commento con Non accordo o Off-Topic, in quanto queste categorie non sono ritenute importanti per la notifica del moderatore.

I campi moderator_comments e moderator_flags devono essere aggiunti allo schema di database delle impostazioni del profilo utente del moderatore per consentire ai moderatori di aggiornare la frequenza delle notifiche e-mail e di rinunciare, se lo desiderano. Livefyre consiglia di impostare questi due campi di notifica e-mail del moderatore su **mai**. Le opzioni includono **mai** (predefinito), **immediatamente** e **spesso**.

**E-mail moderatore (contenuto contrassegnato):**

Quando il contenuto viene contrassegnato in un&#39;app moderata, l&#39;e-mail inviata al moderatore visualizza il contenuto che è stato contrassegnato, il nome utente che ha segnalato il contenuto e un collegamento alla pagina del contenuto.

Quando un utente modifica le preferenze di notifica e-mail sul tuo sito nel tuo sistema di profilo, sincronizza l’aggiornamento al sistema di profili remoti Livefyre utilizzando il ping for Pull di Livefyre.

**Sincronizzazione dei dati con Livefyre**

## Personalizzazione delle e-mail {#section_jxb_c5k_yy}

Diversi campi nei modelli di notifica e-mail possono essere modificati per adattarli al tuo stile e marchio.

* **[!UICONTROL From Email Address]**

   Il &quot;da indirizzo e-mail&quot; per tutte le notifiche e-mail può essere personalizzato per essere coerente con il tuo marchio. Livefyre consiglia **noreply@customerdomain.com**, sostituendo **customerdomain** con il nome di dominio. (Il valore predefinito è **noreply@livefyre.com**.) Passa il tuo &quot;da indirizzo e-mail&quot; preferito al tuo Technical Integration Manager per la configurazione nel database Livefyre per la tua rete.

   >[!NOTE]
   >
   >Lascia vuoto questo campo per disabilitare le notifiche e-mail per la tua rete

* **[!UICONTROL Email Logo]**

   Il logo visualizzato nelle notifiche e-mail può essere personalizzato per visualizzare il logo della tua azienda, anziché il logo Livefyre predefinito, utilizzando la scheda Branding della pagina **Impostazioni di rete** di Studio. Questa personalizzazione è disponibile solo a livello di rete, non a livello di sito, ed è disponibile solo per i clienti Livefyre a pagamento.

* **[!UICONTROL Custom Templates]**

   È possibile implementare un modello e-mail completamente personalizzato se lo desideri. Tuttavia, ciò richiederà un certo impegno nello sviluppo e potrebbe comportare costi per i servizi professionali. Contatta il tuo Account Manager per maggiori informazioni.



App che utilizzano questa funzione:

* [Carosello](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Commenti](/help/using/c-about-apps/c-comments/c-comments.md)
* [Scheda tecnica](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Parete multimediale](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Recensioni](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
