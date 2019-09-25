---
description: Modificate le opzioni di dimensione, larghezza e interazione dell'app Media Wall.
seo-description: Modificate le opzioni di dimensione, larghezza e interazione dell'app Media Wall.
seo-title: Personalizzazioni di Media Wall
solution: Experience Manager
title: Personalizzazioni di Media Wall
uuid: 79aecd92-3937-4bb4-a1a6-b090fb39afb0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Personalizzazioni di Media Wall{#media-wall-customizations}

Modificate le opzioni di dimensione, larghezza e interazione dell'app Media Wall.



I muri multimediali trasmettono immagini dal vivo e altri contenuti in un muro sociale in tempo reale, visualizzando tutte le attività che circondano un evento.

Se attivato, gli utenti possono inviare testo, immagini o video direttamente all'app. I tipi di file supportati includono:

* Immagine: JPEG, GIF, PNG
* Video: Quicktime/MOV, MP4, MPEG, WebM
* Audio: WAV, WAVE, X-MS-WMA, FLAC, OGG, MPEG

* **[!UICONTROL Items to load]**

   Imposta il numero iniziale di elementi di contenuto visualizzati.

* **[!UICONTROL Load content with animation.]** Attivate questa opzione per caricare il Muro multimediale su una pagina con animazione. Disattivate questa opzione per caricare il Muro di supporto su una pagina senza animazione.
* **[!UICONTROL Number of columns.]** Impostate il numero di colonne per la parete multimediale. Il numero di colonne rimane invariato, indipendentemente dalle dimensioni della finestra o del browser. Se si seleziona Automatico, il numero di colonne si regola per visualizzare un numero ottimizzato di colonne per la dimensione dello schermo.
* **[!UICONTROL Fit content to width]**. Quando questa opzione è disattivata, il contenuto viene ritagliato su un quadrato. Attivate questa opzione per visualizzare un'intera immagine nella scheda, che riempia o meno l'intera scheda.
* **[!UICONTROL Include content modal]**

   Consente agli utenti di fare clic su una foto nello streaming per aprirla in una finestra a comparsa sovrapposta.

* **[!UICONTROL Require rights]**. Abilitate questa opzione per visualizzare solo il contenuto con lo stato "Concesso" della richiesta di diritti.
* **[!UICONTROL Hide social branding when rights granted]** Attivate questa opzione per rimuovere il logo del social network di origine (Twitter o Instagram) quando vengono concessi i diritti per un contenuto.

* **[!UICONTROL Upload Button]**

   * **[!UICONTROL Allow user posts]**. Specificate se consentire agli utenti di pubblicare testo, foto o video con il pulsante di caricamento.
   * **[!UICONTROL Require Media]**. Attivate questa opzione per richiedere agli utenti di caricare solo contenuti di foto o video tramite il pulsante Carica.
   * Potete modificare il testo predefinito per i seguenti campi Pulsante Carica:

      * **[!UICONTROL Upload Button Text]**. Testo per il pulsante Carica. Il testo predefinito è "Cosa hai in mente?"
      * **[!UICONTROL Comment Modal Title]**. Titolo per i visitatori del sito modale che utilizzano per pubblicare contenuto. Il testo predefinito è "Invia commento".
      * **[!UICONTROL Comment Modal Button]**. Il testo dei visitatori del sito pulsante che fanno clic per pubblicare il contenuto. Il testo predefinito è "Invia commento".

* **[!UICONTROL Call-to-action button]** Puoi usare il pulsante Invito all’azione con un catalogo di prodotti per indirizzare gli utenti a un prodotto o al tuo sito per ulteriori azioni.

   * **[!UICONTROL Call-to-action button]** Attivate l'interruttore per visualizzare il pulsante Invito all'azione.
   * **[!UICONTROL Require rights to display products]** Attivate l'opzione per richiedere al proprietario del contenuto di concedere i diritti per il contenuto prima che venga visualizzato un pulsante Invito all'azione per il contenuto.

      >[!NOTE]
      >
      >Il contenuto viene visualizzato anche se i diritti non sono concessi per il contenuto, ma il pulsante Invito all’azione non viene visualizzato con il contenuto a meno che non siano stati concessi i diritti per il contenuto.

   * **[!UICONTROL Call-to-action header text]** Le parole da visualizzare nell’intestazione sopra il pulsante Invito all’azione nella modalità contenuto. Il testo predefinito è "Shop this products:".
   * **[!UICONTROL Call-to-action button text]** Le parole da visualizzare nel pulsante Invito all’azione nella modale del contenuto. Il testo predefinito è "Buy Now:".
   * **[!UICONTROL Product display options]** Scegliete se visualizzare il nome della foto e del prodotto mediante il pulsante Invito all’azione.

      >[!NOTE]
      >
      >I pulsanti Foto e Nome prodotto evidenziano blu quando sono attivati.

   * **[!UICONTROL Product URL referral tracking]** Passate all'attivazione per tenere traccia dei riferimenti da questa app alla pagina di prodotto associata.
   * **[!UICONTROL Referral tracking key-value pairs]** Aggiungi parametri per specificare ulteriormente il tracciamento del riferimento dal contenuto dell'app alla pagina del prodotto associata.

* **[!UICONTROL Product page filter]**.
   * **[!UICONTROL Filter UGC by Product ID]**. Selezionate questa opzione per creare un'app per più pagine di prodotto. Filtra l'UGC specifico per il prodotto nell'app per ogni pagina di prodotto. Potete selezionare una o più cartelle per associare raccolte specifiche all'app.
   * **[!UICONTROL Select Product folders]**. Selezionate le cartelle di prodotti di livello principale da usare per filtrare l’UGC. Per selezionare più cartelle, usate Ctrl/Comando + clic. Livefyre utilizza la cartella per determinare quali prodotti in quella cartella visualizzare nell'app su varie pagine.
   * **[!UICONTROL Show related content]**. Attivate questa opzione per visualizzare il contenuto pubblicato nell'app, ma con tag con un ID prodotto diverso. Dopo la visualizzazione del contenuto specifico del prodotto per l'app, Livefyre visualizza il contenuto per altri prodotti e contenuti non associati a un prodotto. Livefyre assegna priorità al contenuto con lo stesso ID prodotto, quindi al contenuto pubblicato nell'app con altri ID prodotto, quindi al contenuto pubblicato nell'app senza ID prodotto.

Puoi personalizzare Media Wall utilizzando:

* **[!UICONTROL Style]** e **[!UICONTROL Config]** le opzioni per tutte le app in **[!UICONTROL App Designer]**. Consultate Personalizzazione delle app per informazioni dettagliate sugli standard **[!UICONTROL Style]** e sulle **[!UICONTROL Config]** opzioni di tutte le app in **[!UICONTROL App Designer]**.

* Strumenti di integrazione. Per ulteriori informazioni su come personalizzare una bacheca multimediale con gli strumenti di integrazione, consulta Integrazione [di](/help/implementation/c-app-integrations/c-media-wall-integration.md) Media Wall.

