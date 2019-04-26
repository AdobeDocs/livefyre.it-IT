---
description: Modifica le opzioni di dimensione, larghezza e interazione dell'app Carosello.
seo-description: Modifica le opzioni di dimensione, larghezza e interazione dell'app
  Carosello.
seo-title: Personalizzare un carosello utilizzando Studio
solution: Experience Manager
title: Personalizzare un carosello utilizzando Studio
uuid: 24 f 080 fc -37 bf -40 d 4-8 c 1 a-a 502 ee 8 ac 978
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Personalizzare un carosello utilizzando Studio{#customize-a-carousel-using-studio}

Modifica le opzioni di dimensione, larghezza e interazione dell'app Carosello.

Tutte le app utilizzano **[!UICONTROL Style]** e **[!UICONTROL Config]** opzioni in **[!UICONTROL App Designer]**. Consultate Personalizzazione delle app per informazioni dettagliate sullo standard **[!UICONTROL Style]** e **[!UICONTROL Config]** opzioni per tutte le app in **[!UICONTROL App Designer]**.

È possibile personalizzare un carosello utilizzando le seguenti opzioni aggiuntive in App Designer:

* **[!UICONTROL Max Number of Items]**

   Imposta il numero di elementi da visualizzare nel carosello. Il valore predefinito è 50.

* **[!UICONTROL Orientation]**

   **[!UICONTROL Responsive]**. Solo per gli schermi del computer

   * Se il contenuto è maggiore di 600 pixel, viene visualizzato in orizzontale
   * Se il contenuto è inferiore a 600 pixel, viene visualizzato verticalmente
   * **Verticale.** Per schermi del computer o dispositivi mobili. Nei dispositivi mobili, la scheda si riduce in base alle dimensioni dello schermo.

* **[!UICONTROL Call-to-action button]** Potete utilizzare il pulsante Call-to-action con un catalogo di prodotti per indirizzare gli utenti a un prodotto o al sito per ulteriori azioni.

   * **[!UICONTROL Call-to-action button]** Attivate l'interruttore per visualizzare il pulsante di invito all'azione.
   * **[!UICONTROL Require rights to display products]** Attivate l'attivazione per richiedere che il proprietario del contenuto conceda i diritti per il contenuto prima che venga visualizzato un pulsante di invito all'azione.
   >[!NOTE]
   >
   >Il contenuto viene visualizzato anche se i diritti non sono concessi per il contenuto, ma il pulsante di invito all'azione non viene visualizzato con il contenuto a meno che non siano concessi diritti per il contenuto.

   * **[!UICONTROL Show call-to-action in tile]**. Scegliete se visualizzare il pulsante di chiamata su una sezione invece di visualizzare il pulsante di invito all'azione solo quando il visitatore del sito fa clic su una scheda e apre il contenuto in una finestra più grande.
   * **[!UICONTROL Call-to-action indication text]** Testo da visualizzare per richiedere all'utente di fare clic sulla scheda per aprire il modale di invito all'azione.
   * **[!UICONTROL Call-to-action header text]** Le parole da visualizzare nell'intestazione sopra il pulsante Call-to-action nel modale del contenuto. Il testo predefinito è "Store questi prodotti: ".
   * **[!UICONTROL Call-to-action button text]** Le parole da visualizzare nel pulsante Call-to-action nel modale del contenuto. Il testo predefinito è "Buy Now: ".
   * **[!UICONTROL Product display options]** Scegliete se visualizzare il **[!UICONTROL Photo]** pulsante **[!UICONTROL Product name]** di invito all'azione.
   >[!NOTE]
   >
   >I pulsanti di nome foto e nome prodotto evidenziano il blu quando sono attivati.

   * **[!UICONTROL Product URL referral tracking]** Attivate l'attivazione per tracciare i riferimenti da questa app alla pagina del prodotto associata.
   * **[!UICONTROL Referral tracking key-value pairs]** Aggiungi parametri per specificare ulteriormente il tracciamento dei riferimenti dal contenuto dell'app alla pagina del prodotto associata.



* **[!UICONTROL Embed App in multiple pages]**

   * **[!UICONTROL Filter UGC by Product ID]**. Selezionate questa opzione per creare un'app per più pagine di prodotto. Filtrare UGC specifico per il prodotto per ogni pagina di prodotto. Potete selezionare una o più cartelle per associare raccolte specifiche all'app.
   * **[!UICONTROL Select Product folders]**. Selezionate le cartelle di prodotto di livello principale da usare per filtrare UGC. Usate CTRL/Comando + clic per selezionare più cartelle. Livefyre utilizza la cartella per determinare quali prodotti visualizzare nell'app in diverse pagine.
   * **[!UICONTROL Show related content]**. Attivate questa opzione per visualizzare il contenuto pubblicato nell'app, ma contrassegnato con un ID prodotto diverso. Una volta visualizzato il contenuto specifico per l'app, Livefyre visualizza il contenuto per altri prodotti e contenuti non associati a un prodotto. Livefyre priorità il contenuto con lo stesso ID prodotto, quindi il contenuto pubblicato nell'app con altri ID prodotto, quindi il contenuto pubblicato nell'app senza ID prodotto.
