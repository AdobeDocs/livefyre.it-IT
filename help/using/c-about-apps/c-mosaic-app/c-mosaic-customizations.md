---
description: Modificate le opzioni di dimensione, larghezza e interazione dell'app Mosaic.
seo-description: Modificate le opzioni di dimensione, larghezza e interazione dell'app Mosaic.
seo-title: Personalizzazioni Mosaico
solution: Experience Manager
title: Personalizzazioni Mosaico
uuid: 4e226d68-f517-4922-bc25-655d524d7d52
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 0%

---


# Personalizzazioni Mosaico{#mosaic-customizations}

Modificate le opzioni di dimensione, larghezza e interazione dell&#39;app Mosaic.

Tutte le app utilizzano le opzioni **[!UICONTROL Style]** e **[!UICONTROL Config]** in **[!UICONTROL App Designer]**. Consultate Personalizzazione delle app per informazioni dettagliate sulle opzioni **[!UICONTROL Style]** e **[!UICONTROL Config]** standard per tutte le app in **[!UICONTROL App Designer.]**

Puoi personalizzare Mosaico utilizzando le seguenti opzioni aggiuntive in App Designer:

* **[!UICONTROL Content interaction]**. Imposta lo stile con cui verrà caricato il nuovo contenuto sulla pagina:

   * **[!UICONTROL Hover Fade]** per applicare la dissolvenza all&#39;altro lato di una scheda quando un visitatore del sito passa il mouse sul contenuto.
   * **[!UICONTROL Hover Flip]** per passare all&#39;altro lato di una scheda quando un visitatore del sito passa il mouse sul contenuto.
   * **[!UICONTROL Click]** per visualizzare l&#39;altro lato di una scheda quando un visitatore del sito fa clic con il mouse sul contenuto.

* **[!UICONTROL Number of Tiles to Load]**. Il numero di sezioni da caricare in un Mosaico. Questo può influenzare la visualizzazione di output. Mosaico non verrà visualizzato in una griglia a meno che non si scelga il numero corretto di sezioni per corrispondere alla larghezza del contenitore. Potrebbe essere necessario regolarli affinché la griglia venga visualizzata correttamente.
* **[!UICONTROL Hide social branding when rights granted]** Attivate questa opzione per rimuovere il logo del social network di origine (Twitter o Instagram) quando vengono concessi i diritti per un contenuto.

* **[!UICONTROL Call-to-action button]** Puoi usare il pulsante Invito all’azione con un catalogo di prodotti per indirizzare gli utenti a un prodotto o al tuo sito per ulteriori azioni.

   * **[!UICONTROL Call-to-action button]** Attivate l&#39;interruttore per visualizzare il pulsante Invito all&#39;azione.

   * **[!UICONTROL Require rights to display products]** Attivate l&#39;opzione per richiedere al proprietario del contenuto di concedere i diritti per il contenuto prima che venga visualizzato un pulsante Invito all&#39;azione per il contenuto.

      >[!NOTE]
      >
      >Il contenuto viene visualizzato anche se i diritti non sono concessi per il contenuto, ma il pulsante Invito all’azione non viene visualizzato con il contenuto a meno che non siano stati concessi i diritti per il contenuto.

   * **[!UICONTROL Show call-to-action in tile]**. Scegliete se visualizzare il pulsante di chiamata all&#39;azione in una sezione Filmstrip invece di visualizzare il pulsante di chiamata all&#39;azione solo quando il visitatore del sito fa clic su una scheda e apre il contenuto in una finestra più ampia.
   * **[!UICONTROL Call-to-action indication text]** Testo da visualizzare per richiedere all&#39;utente di fare clic sulla scheda per aprire la modalità Invito all&#39;azione.

   * **[!UICONTROL Call-to-action header text]** Le parole da visualizzare nell’intestazione sopra il pulsante Invito all’azione nella modalità contenuto. Il testo predefinito è &quot;Shop this products:&quot;.

   * **[!UICONTROL Call-to-action button text]** Personalizzare il testo sul pulsante Invito all’azione. Il testo predefinito è &quot;Buy Now&quot;.

   * **[!UICONTROL Product display options]** Scegliere se visualizzare il pulsante  **[!UICONTROL Photo]** e il pulsante  **[!UICONTROL Product name]** con l&#39;azione.

   * **[!UICONTROL Product URL referral tracking]** Passate all&#39;attivazione per tenere traccia dei riferimenti da questa app alla pagina di prodotto associata.

   * **[!UICONTROL Referral tracking key-value pairs]** Aggiungi parametri per specificare ulteriormente il tracciamento del riferimento dal contenuto dell&#39;app alla pagina del prodotto associata.

* **[!UICONTROL Product page filter]**.

   * **[!UICONTROL Filter UGC by Product ID]**. Selezionate questa opzione per creare un&#39;app per più pagine di prodotto. Filtra l&#39;UGC specifico per il prodotto nell&#39;app per ogni pagina di prodotto. Potete selezionare una o più cartelle per associare raccolte specifiche all&#39;app.
   * **[!UICONTROL Select Product folders]**. Selezionate le cartelle di prodotti di livello principale da usare per filtrare l’UGC. Per selezionare più cartelle, usate Ctrl/Comando + clic. Livefyre utilizza la cartella per determinare quali prodotti in quella cartella visualizzare nell&#39;app su varie pagine.
   * **[!UICONTROL Show related content]**. Attivate questa opzione per visualizzare il contenuto pubblicato nell&#39;app, ma con tag con un ID prodotto diverso. Dopo la visualizzazione del contenuto specifico del prodotto per l&#39;app, Livefyre visualizza il contenuto per altri prodotti e contenuti non associati a un prodotto. Livefyre assegna priorità al contenuto con lo stesso ID prodotto, quindi al contenuto pubblicato nell&#39;app con altri ID prodotto, quindi al contenuto pubblicato nell&#39;app senza ID prodotto.

Per ulteriori informazioni su come personalizzare un mosaico con Livefyre.js, consultate [Opzioni per i mosaici](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).
