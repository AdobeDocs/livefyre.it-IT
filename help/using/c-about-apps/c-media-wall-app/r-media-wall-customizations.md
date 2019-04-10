---
description: Modificate le opzioni di dimensione, larghezza e interazione dell'app
  Media Wall.
seo-description: Modificate le opzioni di dimensione, larghezza e interazione dell'app
  Media Wall.
seo-title: Personalizzazioni di Media Wall
solution: Experience Manager
title: Personalizzazioni di Media Wall
uuid: 79 aecd 92-3937-4 bb 4-a 1 a 6-b 090 fb 39 afb 0
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Personalizzazioni di Media Wall{#media-wall-customizations}

Modificate le opzioni di dimensione, larghezza e interazione dell'app Media Wall.



Le immagini multimediali scorrono le immagini live e altri contenuti in una parete social in tempo reale, visualizzando tutte le attività che circondano un evento.

Se abilitata, gli utenti possono pubblicare testo, immagini o video direttamente su questa app. I tipi di file supportati includono:

* Immagine: JPEG, GIF, PNG
* Video: Quicktime/MOV, MP 4, MPEG, webm
* Audio: WAV, WAVE, X-MS-WMA, FLAC, OGG, MPEG

* **[!UICONTROL Items to load]**

   Imposta il numero iniziale di elementi di contenuto visualizzati.

* **[!UICONTROL Load content with animation.]** Attivate questa opzione per caricare Media Wall su una pagina con animazione. Disattivate questa opzione per caricare Media Wall su una pagina senza animazione.
* **[!UICONTROL Number of columns.]** Impostate il numero di colonne per Media Wall. Il numero di colonne resta invariato, indipendentemente dalle dimensioni della finestra o del browser. Se selezionate Automatico, il numero di colonne si regola per visualizzare un numero ottimizzato di colonne per le dimensioni dello schermo.
* **[!UICONTROL Fit content to width]**. Quando questa opzione è disattivata, il contenuto viene ritagliato in un quadrato. Attivate questa opzione per visualizzare un'intera immagine nella scheda, che riempie l'intera scheda o meno.
* **[!UICONTROL Include content modal]**

   Consente agli utenti di fare clic su una foto nel flusso per aprirla in una finestra a comparsa sovrapposta.

* **[!UICONTROL Require rights]**. Abilitare questa opzione per visualizzare solo il contenuto con lo stato richiesta di diritti di «Aderito».
* **[!UICONTROL Hide social branding when rights granted]** Attivate questa opzione per rimuovere il logo per la rete social media (Twitter o Instagram) quando vengono concessi diritti per una parte del contenuto.

* **[!UICONTROL Upload Button]**

   * **[!UICONTROL Allow user posts]**. Selezionate se consentire agli utenti di pubblicare testo, foto o video con il pulsante di caricamento.
   * **[!UICONTROL Require Media]**. Attivate e attivate per richiedere agli utenti di caricare solo contenuti di foto o video mediante il pulsante Carica.
   * Potete modificare il testo predefinito per i seguenti campi Pulsante Carica:

      * **[!UICONTROL Upload Button Text]**. Testo per il pulsante Carica. Il testo predefinito è "What's mind?"
      * **[!UICONTROL Comment Modal Title]**. Titolo del sito modale usato dai visitatori per pubblicare contenuto. Il testo predefinito è "Post Your Comment" (Pubblicare il commento).
      * **[!UICONTROL Comment Modal Button]**. Il testo dei visitatori del sito di pulsanti fa clic per pubblicare il contenuto. Il testo predefinito è "Post Your Comment" (Pubblicare il commento).

* **[!UICONTROL Call-to-action button]** Potete utilizzare il pulsante Call-to-action con un catalogo di prodotti per indirizzare gli utenti a un prodotto o al sito per ulteriori azioni.

   * **[!UICONTROL Call-to-action button]** Attivate l'interruttore per visualizzare il pulsante Call-to-action.
   * **[!UICONTROL Require rights to display products]** Attivate l'attivazione per richiedere che il proprietario del contenuto abbia concesso i diritti per il contenuto prima che venga visualizzato un pulsante Call-to-action.

      >[!NOTE]
      >
      >Il contenuto viene visualizzato anche se i diritti non sono concessi per il contenuto, ma il pulsante Call-to-action non viene visualizzato con il contenuto a meno che non siano concessi diritti per il contenuto.

   * **[!UICONTROL Call-to-action header text]** Le parole da visualizzare nell'intestazione sopra il pulsante Call-to-action nel modale del contenuto. Il testo predefinito è "Shop these products: ".
   * **[!UICONTROL Call-to-action button text]** Le parole da visualizzare nel pulsante Call-to-action nel modale del contenuto. Il testo predefinito è "Buy Now: ".
   * **[!UICONTROL Product display options]** Scegliete se visualizzare il nome della foto e del prodotto con il pulsante di invito all'azione.

      >[!NOTE]
      >
      >I pulsanti di nome foto e nome prodotto evidenziano il blu quando sono attivati.

   * **[!UICONTROL Product URL referral tracking]** Attivate l'attivazione per tracciare i riferimenti da questa app alla pagina del prodotto associata.
   * **[!UICONTROL Referral tracking key-value pairs]** Aggiungi parametri per specificare ulteriormente il tracciamento dei riferimenti dal contenuto dell'app alla pagina del prodotto associata.

* **[!UICONTROL Product page filter]**.
   * **[!UICONTROL Filter UGC by Product ID]**. Selezionate questa opzione per creare un'app per più pagine di prodotto. Filtrare UGC specifico per il prodotto per ogni pagina di prodotto. Potete selezionare una o più cartelle per associare raccolte specifiche all'app.
   * **[!UICONTROL Select Product folders]**. Selezionate le cartelle di prodotto di livello principale da usare per filtrare UGC. Usate CTRL/Comando + clic per selezionare più cartelle. Livefyre utilizza la cartella per determinare quali prodotti visualizzare nell'app in diverse pagine.
   * **[!UICONTROL Show related content]**. Attivate questa opzione per visualizzare il contenuto pubblicato nell'app, ma contrassegnato con un ID prodotto diverso. Una volta visualizzato il contenuto specifico per l'app, Livefyre visualizza il contenuto per altri prodotti e contenuti non associati a un prodotto. Livefyre priorità il contenuto con lo stesso ID prodotto, quindi il contenuto pubblicato nell'app con altri ID prodotto, quindi il contenuto pubblicato nell'app senza ID prodotto.

Potete personalizzare Media Wall utilizzando:

* **[!UICONTROL Style]** e **[!UICONTROL Config]** opzioni per tutte le app in **[!UICONTROL App Designer]**. Consultate Personalizzazione delle app per informazioni dettagliate sullo standard **[!UICONTROL Style]** e **[!UICONTROL Config]** opzioni per tutte le app in **[!UICONTROL App Designer]**.

* Strumenti di integrazione. Per [ulteriori informazioni su come personalizzare un Media Wall mediante Strumenti di integrazione, consultate Integrazione](/help/implementation/c-app-integrations/c-media-wall-integration.md) di Media Wall.

