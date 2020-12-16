---
description: Modificate le opzioni di dimensione, larghezza e interazione dell'app Carosello.
seo-description: Modificate le opzioni di dimensione, larghezza e interazione dell'app Carosello.
seo-title: Personalizzare un carosello con Studio
solution: Experience Manager
title: Personalizzare un carosello con Studio
uuid: 24f080fc-37bf-40d4-8c1a-a502ee8ac978
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 0%

---


# Personalizzare un carosello utilizzando Studio{#customize-a-carousel-using-studio}

Modificate le opzioni di dimensione, larghezza e interazione dell&#39;app Carosello.

Tutte le app utilizzano le opzioni **[!UICONTROL Style]** e **[!UICONTROL Config]** in **[!UICONTROL App Designer]**. Consultate Personalizzazione delle app per informazioni dettagliate sulle opzioni **[!UICONTROL Style]** e **[!UICONTROL Config]** standard per tutte le app in **[!UICONTROL App Designer]**.

È possibile personalizzare un carosello utilizzando le seguenti opzioni aggiuntive in App Designer:

* **[!UICONTROL Max Number of Items]**

   Imposta il numero di elementi da visualizzare nel carosello. Il valore predefinito è 50.

* **[!UICONTROL Orientation]**

   **[!UICONTROL Responsive]**. Solo per schermi del computer

   * Se il contenuto è maggiore di 600 pixel, viene visualizzato in orizzontale
   * Se il contenuto è inferiore a 600 pixel, viene visualizzato in verticale
   * **Verticale.** Per schermi di computer o dispositivi mobili. Nei dispositivi mobili, la scheda si riduce per adattarsi alle dimensioni dello schermo.

* **[!UICONTROL Call-to-action button]** Puoi usare il pulsante Invito all’azione con un catalogo di prodotti per indirizzare gli utenti a un prodotto o al tuo sito per ulteriori azioni.

   * **[!UICONTROL Call-to-action button]** Passate l’interruttore su attivato per visualizzare il pulsante di invito all’azione.
   * **[!UICONTROL Require rights to display products]** Attivate l’opzione per richiedere al proprietario del contenuto di concedere i diritti per il contenuto prima che venga visualizzato un pulsante di invito all’azione per il contenuto.

   >[!NOTE]
   >
   >Il contenuto viene visualizzato anche se i diritti non sono concessi per il contenuto, ma il pulsante call-to-action non viene visualizzato con il contenuto a meno che non siano stati concessi i diritti per il contenuto.

   * **[!UICONTROL Show call-to-action in tile]**. Scegliete se visualizzare il pulsante di chiamata all&#39;azione su una sezione invece del pulsante di chiamata all&#39;azione solo quando il visitatore del sito fa clic su una scheda e apre il contenuto in una finestra più grande.
   * **[!UICONTROL Call-to-action indication text]** Testo da visualizzare per richiedere all&#39;utente di fare clic sulla scheda per aprire la modalità di chiamata all&#39;azione.
   * **[!UICONTROL Call-to-action header text]** Le parole da visualizzare nell’intestazione sopra il pulsante Invito all’azione nella modalità contenuto. Il testo predefinito è &quot;Shop this products:&quot;.
   * **[!UICONTROL Call-to-action button text]** Le parole da visualizzare nel pulsante Invito all’azione nella modale del contenuto. Il testo predefinito è &quot;Buy Now:&quot;.
   * **[!UICONTROL Product display options]** Scegliere se visualizzare il pulsante  **[!UICONTROL Photo]** e il pulsante  **[!UICONTROL Product name]** con l&#39;azione.

   >[!NOTE]
   >
   >I pulsanti Foto e Nome prodotto evidenziano blu quando sono attivati.

   * **[!UICONTROL Product URL referral tracking]** Passate all&#39;attivazione per tenere traccia dei riferimenti da questa app alla pagina di prodotto associata.
   * **[!UICONTROL Referral tracking key-value pairs]** Aggiungi parametri per specificare ulteriormente il tracciamento del riferimento dal contenuto dell&#39;app alla pagina del prodotto associata.



* **[!UICONTROL Embed App in multiple pages]**

   * **[!UICONTROL Filter UGC by Product ID]**. Selezionate questa opzione per creare un&#39;app per più pagine di prodotto. Filtra l&#39;UGC specifico per il prodotto nell&#39;app per ogni pagina di prodotto. Potete selezionare una o più cartelle per associare raccolte specifiche all&#39;app.
   * **[!UICONTROL Select Product folders]**. Selezionate le cartelle di prodotti di livello principale da usare per filtrare l’UGC. Per selezionare più cartelle, usate Ctrl/Comando + clic. Livefyre utilizza la cartella per determinare quali prodotti in quella cartella visualizzare nell&#39;app su varie pagine.
   * **[!UICONTROL Show related content]**. Attivate questa opzione per visualizzare il contenuto pubblicato nell&#39;app, ma con tag con un ID prodotto diverso. Dopo la visualizzazione del contenuto specifico del prodotto per l&#39;app, Livefyre visualizza il contenuto per altri prodotti e contenuti non associati a un prodotto. Livefyre assegna priorità al contenuto con lo stesso ID prodotto, quindi al contenuto pubblicato nell&#39;app con altri ID prodotto, quindi al contenuto pubblicato nell&#39;app senza ID prodotto.
