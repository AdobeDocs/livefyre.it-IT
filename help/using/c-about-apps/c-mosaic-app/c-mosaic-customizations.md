---
description: Modifica le opzioni di dimensione, larghezza e interazione dell’app Mosaic.
title: Personalizzazioni di Mosaic
exl-id: 0223a64c-ec33-4e01-85d7-11845c9b8476
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 0%

---

# Personalizzazioni Mosaic{#mosaic-customizations}

Modifica le opzioni di dimensione, larghezza e interazione dell’app Mosaic.

Tutte le app utilizzano le opzioni **[!UICONTROL Style]** e **[!UICONTROL Config]** in **[!UICONTROL App Designer]**. Consulta Personalizzazione delle app per i dettagli sulle opzioni standard **[!UICONTROL Style]** e **[!UICONTROL Config]** per tutte le app in **[!UICONTROL App Designer.]**

Puoi personalizzare Mosaic utilizzando le seguenti opzioni aggiuntive in App Designer:

* **[!UICONTROL Content interaction]**. Imposta lo stile con cui verrà caricato il nuovo contenuto sulla pagina:

   * **[!UICONTROL Hover Fade]** per passare all’altro lato di una scheda quando un visitatore del sito passa il mouse sul contenuto.
   * **[!UICONTROL Hover Flip]** per passare dall’altro lato di una scheda quando un visitatore del sito passa il mouse sul contenuto.
   * **[!UICONTROL Click]** per visualizzare l’altro lato di una scheda quando un visitatore del sito fa clic sul suo mouse sul contenuto.

* **[!UICONTROL Number of Tiles to Load]**. Il numero di riquadri da caricare in un Mosaic. Questo può influenzare la visualizzazione di output. Mosaic non verrà visualizzato in una griglia a meno che non si scegli il numero corretto di riquadri che corrispondono alla larghezza del contenitore. Potrebbe essere necessario regolarli affinché la griglia venga visualizzata correttamente.
* **[!UICONTROL Hide social branding when rights granted]** Attivate questa opzione per rimuovere il logo della rete di social media di origine (Twitter o Instagram) quando vengono concessi i diritti per un contenuto.

* **[!UICONTROL Call-to-action button]** Puoi usare il pulsante Invito all’azione con un catalogo di prodotti per indirizzare gli utenti a un prodotto o al sito per ulteriori azioni.

   * **[!UICONTROL Call-to-action button]** Attiva l&#39;interruttore per visualizzare il pulsante di invito all&#39;azione.

   * **[!UICONTROL Require rights to display products]** Passa all’attivazione per richiedere al proprietario del contenuto di disporre dei diritti per il contenuto prima che venga visualizzato un pulsante di invito all’azione per il contenuto.

      >[!NOTE]
      >
      >Il contenuto viene visualizzato anche se i diritti non sono concessi per il contenuto, ma il pulsante Invito all’azione non viene visualizzato con il contenuto, a meno che non siano concessi i diritti per il contenuto.

   * **[!UICONTROL Show call-to-action in tile]**. Scegli se visualizzare il pulsante di invito all’azione su un riquadro di Filmstrip invece di visualizzare il pulsante di invito all’azione solo quando il visitatore del sito fa clic su una scheda e apre il contenuto in una finestra più grande.
   * **[!UICONTROL Call-to-action indication text]** Testo da visualizzare per richiedere all’utente di fare clic sulla scheda per aprire il modale Invito all’azione.

   * **[!UICONTROL Call-to-action header text]** Le parole da visualizzare nell’intestazione sopra il pulsante Invito all’azione nel modale del contenuto. La dicitura predefinita è &quot;Acquista questi prodotti:&quot;.

   * **[!UICONTROL Call-to-action button text]** Personalizza il testo del pulsante di invito all’azione. Il testo predefinito è &quot;Acquista ora&quot;.

   * **[!UICONTROL Product display options]** Scegli se visualizzare  **[!UICONTROL Photo]** e  **[!UICONTROL Product name]** con il pulsante di invito all’azione.

   * **[!UICONTROL Product URL referral tracking]** Passa all’attivazione per tenere traccia dei riferimenti da questa app alla pagina di prodotto associata.

   * **[!UICONTROL Referral tracking key-value pairs]** Aggiungi dei parametri per specificare ulteriormente il tracciamento dei riferimenti dal contenuto dell&#39;app alla pagina di prodotto associata.

* **[!UICONTROL Product page filter]**.

   * **[!UICONTROL Filter UGC by Product ID]**. Seleziona questa opzione per creare un’app per più pagine di prodotto. Filtra l’UGC specifico per il prodotto nell’app per ogni pagina di prodotto. Puoi selezionare una o più cartelle per associare raccolte specifiche all’app.
   * **[!UICONTROL Select Product folders]**. Seleziona le cartelle di prodotto di livello principale da utilizzare per filtrare gli UGC. Utilizza CTRL/Comando + clic per selezionare più cartelle. Livefyre utilizza la cartella per determinare quali prodotti in tale cartella visualizzare nell’app su varie pagine.
   * **[!UICONTROL Show related content]**. Attiva o disattiva questa opzione per visualizzare il contenuto pubblicato nell’app, ma con tag con un ID prodotto diverso. Dopo che è stato visualizzato il contenuto specifico per il prodotto per l’app, Livefyre visualizza il contenuto per altri prodotti e contenuti non associati a un prodotto. Livefyre dà priorità al contenuto con lo stesso ID prodotto prima, al contenuto pubblicato nell’app con altri ID prodotto, quindi al contenuto pubblicato nell’app senza ID prodotto.

Per ulteriori informazioni su come personalizzare un Mosaic con Livefyre.js, consulta [Opzioni Mosaic](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) .
