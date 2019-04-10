---
description: Consentite agli utenti di selezionare la frequenza e il contenuto della
  notifica.
seo-description: Consentite agli utenti di selezionare la frequenza e il contenuto
  della notifica.
seo-title: Notifiche e-mail
solution: Experience Manager
title: Notifiche e-mail
uuid: 27 dad 133-bd 8 d -4949-8146-1254 c 160 d 3 af
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Notifiche e-mail{#email-notifications}

Consentite agli utenti di selezionare la frequenza e il contenuto della notifica.

**Abilita notifiche e-mail per utenti e moderatori.**

Livefyre Apps consente di abilitare le notifiche e-mail per gli utenti e i moderatori, in base a azioni specifiche. Le notifiche si basano sul momento in cui il contenuto viene postato nel flusso, consentendo agli utenti di restare coinvolti nelle conversazioni di interesse e di ricevere notifiche quando un utente ama o risponde a uno dei loro commenti.

Gli utenti e i moderatori possono rifiutare o ritirare la notifica e-mail e possono impostare la frequenza con cui ricevere i messaggi e-mail. In questa sezione viene illustrato come configurare e personalizzare le notifiche e-mail.

* Opzioni e-mail utente: opzioni di notifica utente disponibili.
* Opzioni e-mail moderatore: opzioni di notifica moderatore disponibili.
* Opzioni e-mail di identità Livefyre: e-mail inviate come parte di Livefyre Identity. Tali e-mail sono pertinenti solo ai clienti Livefyre Identity.
* Sincronizzazione dati con Livefyre: mantenere le preferenze sincronizzate con Livefyre.
* Personalizzazione delle e-mail: personalizzazioni e-mail disponibili.

Utilizzate **Impostazioni > Impostazioni integrazione > Impostazione impostazione** notifiche e-mail per personalizzare le notifiche e-mail per la rete.

>[!NOTE]
>
>Per garantire che gli utenti finali non ricevano posta non desiderata, non vengono inviate notifiche e-mail dall'ambiente Livefyre UAT.

**Opzioni e-mail utente**

Livefyre consente di consentire agli utenti di ricevere notifiche e-mail sull'attività del sito. Utilizzate le impostazioni di integrazione di Livefyre fornite in Livefyre per consentire agli utenti di selezionare le proprie preferenze per le pianificazioni di notifica.

>[!NOTE]
>
>Le e-mail vengono inviate solo per il contenuto pubblicato manualmente nel flusso e non per il contenuto recuperato da socialsync.

Per consentire agli utenti di impostare le preferenze di notifica, includete una sezione Notifiche e-mail nelle impostazioni utente per il sistema di profilo utente. Aggiungi i campi corrispondenti allo schema del database del profilo utente, quindi gestisci le impostazioni dell'utente utilizzando Ping per Pull. (Collaborate con il Gestore integrazione tecnica per definire le frequenze predefinite per la rete. Se siete clienti Enterprise Profiles, trasmettete le impostazioni predefinite selezionate al team di consegna di Livefyre per la configurazione nel database Livefyre.)

Gli utenti sul sito possono seguire una conversazione e iniziare a ricevere le notifiche e-mail facendo clic sul **[!UICONTROL +Follow]** pulsante nell'editor dei commenti. Le preferenze di notifica sono definite a livello di rete di Livefyre. Qualsiasi impostazione utente si applica a tutti i siti e le conversazioni nella rete.

**Valori predefiniti raccomandati**

* Commenti in una conversazione l'm seguente: ** digest orario**
* A qualcuno piace uno dei miei commenti: ** digest orario**
* Un utente risponde a uno dei miei commenti: ** immediatamente**
* Segui automaticamente le conversazioni quando lascio un commento: ** off** (non selezionata)

**Nota**: Le notifiche e-mail sono basate sul contenuto ora approvato per l'inclusione nel flusso.

Livefyre offre due opzioni di frequenza e-mail:

* Immediatamente
* Riassunto orario

**Immediatamente**

Le e-mail inviate mostrano immediatamente il testo, il titolo dell'articolo, il nome utente dell'autore e un **collegamento di risposta** che porta l'utente al contenuto della pagina. Tali e-mail includono anche un collegamento **di annullamento della sottoscrizione** nel piè di pagina, che consente agli utenti di annullare l'iscrizione alle notifiche e-mail per tale raccolta. Facendo clic su** Annulla iscrizione**, le passeranno a una pagina di conferma per informarli che sono state annullate dalla raccolta.

**Riassunto orario**

Le e-mail inviate in un riassunto orario vengono visualizzate in tutto il contenuto, risposte al contenuto e mi piacciono per il contenuto entro l'ultima ora (o così) per app che l'utente segue. Se l'utente sta seguendo più app nella rete, riceveranno un messaggio e-mail per ogni app.

>[!NOTE]
>
>Nelle conversazioni senza nuovo contenuto per più ore, gli utenti con digest orario abilitato riceveranno un avviso immediatamente dopo un nuovo post di contenuto.

**Opzioni e-mail moderatore**

I moderatori possono scegliere di ricevere e-mail per il contenuto pubblicato in un'app che segue, e per i commenti segnalati in spam o offensivi in un'app che stanno moderando. **Nota:** Non viene inviata alcuna e-mail quando gli utenti segnalano un commento con Non d'accordo o Fuori argomento, poiché queste categorie non sono considerate importanti per la notifica moderatore.

I campi moderator_ comments e moderator_ flags devono essere aggiunti anche allo schema del database della pagina del moderatore per consentire ai moderatori di aggiornare la frequenza delle notifiche e-mail e di rifiutare se desiderano. Livefyre consiglia di impostare **su mai questi due campi di notifica e-mail moderatore**. Le opzioni includono **mai** (impostazione predefinita), **immediatamente**e **spesso**.

**E-mail moderatore (contenuto con segnalazione):**

Quando il contenuto viene segnalato in un'app moderata, l'e-mail inviata al moderatore visualizzerà il contenuto contrassegnato, il nome utente che ha segnalato il contenuto e di nuovo un collegamento alla pagina del contenuto.

Quando un utente modifica le preferenze di notifica e-mail sul sito nel sistema di profilo, sincronizzate l'aggiornamento al sistema remoto di Livefyre utilizzando Ping per Pull.

**Sincronizzazione dati con Livefyre**

## Personalizzazione delle e-mail {#section_jxb_c5k_yy}

Diversi campi nei modelli di notifica e-mail possono essere modificati in base al tuo stile e marchio.

* **[!UICONTROL From Email Address]**

   L '«indirizzo e-mail» per tutte le notifiche e-mail può essere personalizzato in modo da essere coerente con il tuo marchio. Livefyre consiglia **noreply@customerdomain.com**, sostituendo **customerdomainwith**your domain name. (Il valore predefinito è **noreply@livefyre.com**.) Passate il vostro «indirizzo e-mail» preferito al Gestore Technical Integration Manager per la configurazione nel database di Livefyre per la vostra rete.

   >[!NOTE]
   >
   >Lasciate vuoto questo campo per disattivare le notifiche e-mail per la rete

* **[!UICONTROL Email Logo]**

   Il logo visualizzato nelle notifiche e-mail può essere personalizzato per visualizzare il logo aziendale, anziché quello predefinito Livefyre, utilizzando la scheda Branding della **pagina Impostazioni** di rete di Studio. Questa personalizzazione è disponibile solo a livello di rete, non a livello di sito ed è disponibile solo per clienti Livefyre a pagamento.

* **[!UICONTROL Custom Templates]**

   Se desiderato, è possibile implementare un modello e-mail completamente personalizzato. Tuttavia, questo richiede un certo sforzo di sviluppo e potrebbe sostenere costi di servizi professionali. Contattate l'Account Manager per informazioni dettagliate.



App che utilizzano questa funzione:

* [Carosello](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Commenti](/help/using/c-about-apps/c-comments/c-comments.md)
* [Scheda Funzioni](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Media Wall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Recensioni](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)

