---
description: Modifica le opzioni di dimensione, larghezza e interazione dell’app Media Wall.
title: Personalizzazioni di muri di supporti
exl-id: bc34d8da-9e14-4226-b38d-128889bc31cc
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '718'
ht-degree: 0%

---

# Personalizzazioni di mura di supporti{#media-wall-customizations}

Modifica le opzioni di dimensione, larghezza e interazione dell’app Media Wall.



Media Walls trasmettono immagini live e altri contenuti in un muro sociale in tempo reale, visualizzando tutte le attività che circondano un evento.

Se abilitato, gli utenti possono inviare testo, immagini o video direttamente a questa app. I tipi di file supportati includono:

* Immagine: JPEG, GIF, PNG
* Video: Quicktime/MOV, MP4, MPEG, WebM
* Audio: WAV, WAVE, X-MS-WMA, FLAC, OGG, MPEG

* **[!UICONTROL Items to load]**

   Imposta il numero iniziale di elementi di contenuto visualizzati.

* **[!UICONTROL Load content with animation.]** Attivate questa opzione per caricare Media Wall su una pagina con animazione. Disattiva questa opzione per caricare Media Wall su una pagina senza animazione.
* **[!UICONTROL Number of columns.]** Impostare il numero di colonne per la parete multimediale. Il numero di colonne rimane invariato, indipendentemente dalle dimensioni della finestra o del browser. Se si seleziona Automatico, il numero di colonne si regola per visualizzare un numero ottimizzato di colonne per la dimensione dello schermo.
* **[!UICONTROL Fit content to width]**. Quando questa opzione è disattivata, il contenuto viene ritagliato in un quadrato. Attiva questa opzione per visualizzare un&#39;intera immagine nella scheda, che si riempia l&#39;intera scheda o meno.
* **[!UICONTROL Include content modal]**

   Consente agli utenti di fare clic su una foto nel flusso per aprirla in una finestra a comparsa sovrapposta.

* **[!UICONTROL Require rights]**. Abilita questa opzione per visualizzare solo il contenuto con lo stato di richiesta dei diritti &quot;Concesso&quot;.
* **[!UICONTROL Hide social branding when rights granted]** Attivate questa opzione per rimuovere il logo della rete di social media di origine (Twitter o Instagram) quando vengono concessi i diritti per un contenuto.

* **[!UICONTROL Upload Button]**

   * **[!UICONTROL Allow user posts]**. Seleziona se consentire agli utenti di pubblicare testo, foto o video con il pulsante di caricamento.
   * **[!UICONTROL Require Media]**. Attiva per richiedere agli utenti di caricare solo contenuti di foto o video utilizzando il pulsante Carica.
   * Puoi modificare il testo predefinito per i seguenti campi Pulsante di caricamento:

      * **[!UICONTROL Upload Button Text]**. Testo per il pulsante Carica. Il testo predefinito è &quot;Cosa hai in mente?&quot;
      * **[!UICONTROL Comment Modal Title]**. Il titolo del sito modale utilizzato dai visitatori per pubblicare contenuti. Il testo predefinito è &quot;Pubblica il tuo commento&quot;.
      * **[!UICONTROL Comment Modal Button]**. Il testo del pulsante dei visitatori del sito clicca per pubblicare il contenuto. Il testo predefinito è &quot;Pubblica il tuo commento&quot;.

* **[!UICONTROL Call-to-action button]** Puoi usare il pulsante Invito all’azione con un catalogo di prodotti per indirizzare gli utenti a un prodotto o al sito per ulteriori azioni.

   * **[!UICONTROL Call-to-action button]** Attiva l&#39;interruttore per visualizzare il pulsante di invito all&#39;azione.
   * **[!UICONTROL Require rights to display products]** Passa all’attivazione per richiedere al proprietario del contenuto di disporre dei diritti per il contenuto prima che venga visualizzato un pulsante di invito all’azione per il contenuto.

      >[!NOTE]
      >
      >Il contenuto viene visualizzato anche se i diritti non sono concessi per il contenuto, ma il pulsante Invito all’azione non viene visualizzato con il contenuto, a meno che non siano concessi i diritti per il contenuto.

   * **[!UICONTROL Call-to-action header text]** Le parole da visualizzare nell’intestazione sopra il pulsante Invito all’azione nel modale del contenuto. La dicitura predefinita è &quot;Acquista questi prodotti:&quot;.
   * **[!UICONTROL Call-to-action button text]** Le parole da visualizzare nel pulsante Invito all’azione nel modale del contenuto. Il testo predefinito è &quot;Acquista ora:&quot;.
   * **[!UICONTROL Product display options]** Scegli se visualizzare il nome della foto e del prodotto con il pulsante di invito all’azione.

      >[!NOTE]
      >
      >I pulsanti Foto e Nome prodotto evidenziano entrambi blu quando sono attivati.

   * **[!UICONTROL Product URL referral tracking]** Passa all’attivazione per tenere traccia dei riferimenti da questa app alla pagina di prodotto associata.
   * **[!UICONTROL Referral tracking key-value pairs]** Aggiungi dei parametri per specificare ulteriormente il tracciamento dei riferimenti dal contenuto dell&#39;app alla pagina di prodotto associata.

* **[!UICONTROL Product page filter]**.
   * **[!UICONTROL Filter UGC by Product ID]**. Seleziona questa opzione per creare un’app per più pagine di prodotto. Filtra l’UGC specifico per il prodotto nell’app per ogni pagina di prodotto. Puoi selezionare una o più cartelle per associare raccolte specifiche all’app.
   * **[!UICONTROL Select Product folders]**. Seleziona le cartelle di prodotto di livello principale da utilizzare per filtrare gli UGC. Utilizza CTRL/Comando + clic per selezionare più cartelle. Livefyre utilizza la cartella per determinare quali prodotti in tale cartella visualizzare nell’app su varie pagine.
   * **[!UICONTROL Show related content]**. Attiva o disattiva questa opzione per visualizzare il contenuto pubblicato nell’app, ma con tag con un ID prodotto diverso. Dopo che è stato visualizzato il contenuto specifico per il prodotto per l’app, Livefyre visualizza il contenuto per altri prodotti e contenuti non associati a un prodotto. Livefyre dà priorità al contenuto con lo stesso ID prodotto prima, al contenuto pubblicato nell’app con altri ID prodotto, quindi al contenuto pubblicato nell’app senza ID prodotto.

Puoi personalizzare Media Wall utilizzando:

* **[!UICONTROL Style]** e  **[!UICONTROL Config]** le opzioni per tutte le app in  **[!UICONTROL App Designer]**. Consulta Personalizzazione delle app per i dettagli sulle opzioni **[!UICONTROL Style]** e **[!UICONTROL Config]** standard per tutte le app in **[!UICONTROL App Designer]**.

* Strumenti di integrazione. Per ulteriori informazioni su come personalizzare una Media Wall utilizzando gli strumenti di integrazione, consulta [Integrazione Media Wall](/help/implementation/c-app-integrations/c-media-wall-integration.md) .
