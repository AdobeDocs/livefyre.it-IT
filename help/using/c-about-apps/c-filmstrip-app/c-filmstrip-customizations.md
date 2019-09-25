---
description: nulle
seo-description: nulle
seo-title: Personalizzazioni Filmstrip
solution: Experience Manager
title: Personalizzazioni Filmstrip
uuid: 99f8b697-4aa3-4813-bcac-d0e0bdee252d
translation-type: tm+mt
source-git-commit: bd989c97ae5cf06a5ac3deec215f865b0fe95d16

---


# Personalizzazioni Filmstrip{#filmstrip-customizations}

Tutte le app utilizzano **[!UICONTROL Style]** e **[!UICONTROL Config]** le opzioni in **[!UICONTROL App Designer]**. Consulta Personalizzazione delle app per informazioni dettagliate sulle opzioni standard **[!UICONTROL Style]** e **[!UICONTROL Config]** per tutte le app nel pannello **[!UICONTROL App Designer.]**

Potete personalizzare Filmstrip utilizzando le seguenti opzioni aggiuntive in App Designer:

* **[!UICONTROL Content fit]**. Scegliete **[!UICONTROL crop]** di ritagliare il contenuto per riempire la scheda o **[!UICONTROL Aspect Ratio]** per visualizzare un'intera immagine nella scheda, che riempia o meno l'intera scheda.
* **[!UICONTROL Tile Size]**. Specificate le dimensioni delle sezioni in pixel.
* **[!UICONTROL Show Notifications]**. Scegliete se visualizzare una notifica per il nuovo contenuto durante lo streaming nell'app Filmstrip.
* **[!UICONTROL Require rights]**. Abilitate questa opzione per visualizzare solo il contenuto con lo stato "Concesso" della richiesta di diritti.
* **[!UICONTROL Hide social branding when rights granted]** Attivate questa opzione per rimuovere il logo del social network di origine (Twitter o Instagram) quando vengono concessi i diritti per un contenuto.
* **[!UICONTROL Call-to-action button]** You can use the call-to-action button with a product catalog to direct users to a product or to your site for further action.

   * **[!UICONTROL Call-to-action button]** Passate l’interruttore su attivato per visualizzare il pulsante di invito all’azione.
   * **[!UICONTROL Require rights to display products]** Attivate questa opzione per richiedere al proprietario del contenuto di concedere i diritti per il contenuto prima che venga visualizzato un pulsante di invito all’azione per il contenuto.

      >[!NOTE]
      >
      >Il contenuto viene visualizzato anche se i diritti non sono concessi per il contenuto, ma il pulsante call-to-action non viene visualizzato con il contenuto a meno che non siano stati concessi i diritti per il contenuto.

   * **[!UICONTROL Show call-to-action in tile]**. Scegliete se visualizzare il pulsante di chiamata all'azione in una sezione Filmstrip invece di visualizzare il pulsante di chiamata all'azione solo quando il visitatore del sito fa clic su una scheda e apre il contenuto in una finestra più ampia.
   * **[!UICONTROL Call-to-action indication text]** Testo da visualizzare per richiedere all'utente di fare clic sulla scheda per aprire la modalità di chiamata all'azione.
   * **[!UICONTROL Call-to-action header text]** The words to display in the header above the call-to-action button in the content modal. Il testo predefinito è "Shop this products:".
   * **[!UICONTROL Call-to-action button text]** Le parole da visualizzare nel pulsante call-to-action nella modale del contenuto. Il testo predefinito è "Buy Now:".
   * **[!UICONTROL Product display options]** Scegliete se visualizzare il pulsante **[!UICONTROL Photo]** e il pulsante **[!UICONTROL Product name]** con cui effettuare la chiamata all’azione.

      >[!NOTE]
      >
      >I pulsanti Foto e Nome prodotto evidenziano blu quando sono attivati.

   * **[!UICONTROL Product URL referral tracking]** Passate all'attivazione per tenere traccia dei riferimenti da questa app alla pagina di prodotto associata.
   * **[!UICONTROL Referral tracking key-value pairs]** Aggiungi parametri per specificare ulteriormente il tracciamento del riferimento dal contenuto dell'app alla pagina del prodotto associata.

* **[!UICONTROL Embed App in multiple pages]**.

   * **[!UICONTROL Filter UGC by Product ID]**. Selezionate questa opzione per creare un'app per più pagine di prodotto. Filtra l'UGC specifico per il prodotto nell'app per ogni pagina di prodotto. Potete selezionare una o più cartelle per associare raccolte specifiche all'app.
   * **[!UICONTROL Select product folders]**. Selezionate le cartelle di prodotti di livello principale da usare per filtrare l’UGC. Per selezionare più cartelle, usate Ctrl/Comando + clic. Livefyre utilizza la cartella per determinare quali prodotti in quella cartella visualizzare nell'app su varie pagine.
   * **[!UICONTROL Show related content]**. Attivate questa opzione per visualizzare il contenuto pubblicato nell'app, ma con tag con un ID prodotto diverso. Dopo la visualizzazione del contenuto specifico del prodotto per l'app, Livefyre visualizza il contenuto per altri prodotti e contenuti non associati a un prodotto. Livefyre assegna priorità al contenuto con lo stesso ID prodotto, quindi al contenuto pubblicato nell'app con altri ID prodotto, quindi al contenuto pubblicato nell'app senza ID prodotto.

Per ulteriori informazioni su come personalizzare un [Filmstrip con Livefyre.js, consultate Opzioni](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) Filmstrip.

