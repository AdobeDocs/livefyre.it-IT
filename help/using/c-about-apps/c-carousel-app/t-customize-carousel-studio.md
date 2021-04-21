---
description: Modifica le opzioni di dimensione, larghezza e interazione dell’app Carosello.
title: Personalizzare un carosello con Studio
exl-id: f6f681ac-c601-40b9-9e99-bf5495f505f8
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 0%

---

# Personalizzare un carosello utilizzando Studio{#customize-a-carousel-using-studio}

Modifica le opzioni di dimensione, larghezza e interazione dell’app Carosello.

Tutte le app utilizzano le opzioni **[!UICONTROL Style]** e **[!UICONTROL Config]** in **[!UICONTROL App Designer]**. Consulta Personalizzazione delle app per i dettagli sulle opzioni **[!UICONTROL Style]** e **[!UICONTROL Config]** standard per tutte le app in **[!UICONTROL App Designer]**.

Puoi personalizzare un carosello utilizzando le seguenti opzioni aggiuntive in App Designer:

* **[!UICONTROL Max Number of Items]**

   Imposta il numero di elementi da visualizzare nel carosello. Il valore predefinito è 50.

* **[!UICONTROL Orientation]**

   **[!UICONTROL Responsive]**. Solo per schermi al computer

   * Se il contenuto è più grande di 600 pixel, viene visualizzato in orizzontale
   * Se il contenuto è inferiore a 600 pixel, viene visualizzato verticalmente
   * **Verticale.** Per schermi di computer o dispositivi mobili. Nei dispositivi mobili, la scheda si riduce per adattarsi alle dimensioni dello schermo.

* **[!UICONTROL Call-to-action button]** Puoi usare il pulsante Invito all’azione con un catalogo di prodotti per indirizzare gli utenti a un prodotto o al sito per ulteriori azioni.

   * **[!UICONTROL Call-to-action button]** Attiva l&#39;interruttore per visualizzare il pulsante di invito all&#39;azione.
   * **[!UICONTROL Require rights to display products]** Passa all’attivazione per richiedere al proprietario del contenuto di disporre dei diritti per il contenuto prima che venga visualizzato un pulsante di invito all’azione per il contenuto.

   >[!NOTE]
   >
   >Il contenuto viene visualizzato anche se i diritti non sono concessi per il contenuto, ma il pulsante di invito all’azione non viene visualizzato con il contenuto a meno che non siano concessi i diritti per il contenuto.

   * **[!UICONTROL Show call-to-action in tile]**. Scegli se visualizzare il pulsante di invito all’azione su un riquadro invece di visualizzare il pulsante di invito all’azione solo quando il visitatore del sito fa clic su una scheda e apre il contenuto in una finestra più grande.
   * **[!UICONTROL Call-to-action indication text]** Testo da visualizzare per richiedere all’utente di fare clic sulla scheda per aprire la finestra modale di invito all’azione.
   * **[!UICONTROL Call-to-action header text]** Le parole da visualizzare nell’intestazione sopra il pulsante Invito all’azione nel modale del contenuto. Il testo predefinito è &quot;Acquista questi prodotti:&quot;.
   * **[!UICONTROL Call-to-action button text]** Le parole da visualizzare nel pulsante Invito all’azione nel modale del contenuto. Il testo predefinito è &quot;Acquista ora:&quot;.
   * **[!UICONTROL Product display options]** Scegli se visualizzare  **[!UICONTROL Photo]** e  **[!UICONTROL Product name]** con il pulsante di invito all’azione.

   >[!NOTE]
   >
   >I pulsanti Foto e Nome prodotto evidenziano entrambi blu quando sono attivati.

   * **[!UICONTROL Product URL referral tracking]** Passa all’attivazione per tenere traccia dei riferimenti da questa app alla pagina di prodotto associata.
   * **[!UICONTROL Referral tracking key-value pairs]** Aggiungi dei parametri per specificare ulteriormente il tracciamento dei riferimenti dal contenuto dell&#39;app alla pagina di prodotto associata.



* **[!UICONTROL Embed App in multiple pages]**

   * **[!UICONTROL Filter UGC by Product ID]**. Seleziona questa opzione per creare un’app per più pagine di prodotto. Filtra l’UGC specifico per il prodotto nell’app per ogni pagina di prodotto. Puoi selezionare una o più cartelle per associare raccolte specifiche all’app.
   * **[!UICONTROL Select Product folders]**. Seleziona le cartelle di prodotto di livello principale da utilizzare per filtrare gli UGC. Utilizza CTRL/Comando + clic per selezionare più cartelle. Livefyre utilizza la cartella per determinare quali prodotti in tale cartella visualizzare nell’app su varie pagine.
   * **[!UICONTROL Show related content]**. Attiva o disattiva questa opzione per visualizzare il contenuto pubblicato nell’app, ma con tag con un ID prodotto diverso. Dopo che è stato visualizzato il contenuto specifico per il prodotto per l’app, Livefyre visualizza il contenuto per altri prodotti e contenuti non associati a un prodotto. Livefyre dà priorità al contenuto con lo stesso ID prodotto prima, al contenuto pubblicato nell’app con altri ID prodotto, quindi al contenuto pubblicato nell’app senza ID prodotto.
