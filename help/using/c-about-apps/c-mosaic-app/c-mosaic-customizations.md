---
description: Modificare le opzioni di dimensione, larghezza e interazione dell'app Mosaic.
seo-description: Modificare le opzioni di dimensione, larghezza e interazione dell'app Mosaic.
seo-title: Personalizzazioni mosaiche
solution: Experience Manager
title: Personalizzazioni mosaiche
uuid: 4 e 226 d 68-f 517-4922-bc 25-655 d 524 d 7 d 52
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Personalizzazioni mosaiche{#mosaic-customizations}

Modificare le opzioni di dimensione, larghezza e interazione dell&#39;app Mosaic.

Tutte le app utilizzano **[!UICONTROL Style]** e **[!UICONTROL Config]** opzioni in **[!UICONTROL App Designer]**. Consultate Personalizzazione delle app per informazioni dettagliate sullo standard **[!UICONTROL Style]** e **[!UICONTROL Config]** le opzioni per tutte le app nel pannello **[!UICONTROL App Designer.]**

È possibile personalizzare Mosaic utilizzando le seguenti opzioni aggiuntive in App Designer:

* **[!UICONTROL Content interaction]**. Imposta lo stile con il quale verrà caricato nuovo contenuto sulla pagina:

   * **[!UICONTROL Hover Fade]** dissolvenza fino all&#39;altro lato di una scheda quando un visitatore del sito passa il mouse sul contenuto.
   * **[!UICONTROL Hover Flip]** capovolgere l&#39;altro lato di una scheda quando un visitatore passa il mouse sul contenuto.
   * **[!UICONTROL Click]** per visualizzare l&#39;altro lato di una scheda quando un visitatore del sito fa clic sul suo mouse.

* **[!UICONTROL Number of Tiles to Load]**. Numero di porzioni da caricare in Mosaic. Questo può influire sul display di output. Mosaic non viene visualizzato in una griglia a meno che non scegliiate il numero corretto di sezioni per corrispondere alla larghezza del contenitore. Potrebbe essere necessario modificarli affinché la griglia venga visualizzata correttamente.
* **[!UICONTROL Hide social branding when rights granted]** Attivate questa opzione per rimuovere il logo per la rete social media (Twitter o Instagram) quando vengono concessi diritti per una parte del contenuto.

* **[!UICONTROL Call-to-action button]** Potete utilizzare il pulsante Call-to-action con un catalogo di prodotti per indirizzare gli utenti a un prodotto o al sito per ulteriori azioni.

   * **[!UICONTROL Call-to-action button]** Attivate l&#39;interruttore per visualizzare il pulsante Call-to-action.

   * **[!UICONTROL Require rights to display products]** Attivate l&#39;attivazione per richiedere che il proprietario del contenuto abbia concesso i diritti per il contenuto prima che venga visualizzato un pulsante Call-to-action.

      >[!NOTE]
      >
      >Il contenuto viene visualizzato anche se i diritti non sono concessi per il contenuto, ma il pulsante Call-to-action non viene visualizzato con il contenuto a meno che non siano concessi diritti per il contenuto.

   * **[!UICONTROL Show call-to-action in tile]**. Scegliete se visualizzare il pulsante di chiamata su una sezione Filmstrip invece di visualizzare il pulsante di invito all&#39;azione solo quando il visitatore del sito fa clic su una scheda e apre il contenuto in una finestra più grande.
   * **[!UICONTROL Call-to-action indication text]** Testo da visualizzare per richiedere all&#39;utente di fare clic sulla scheda per aprire il modale Call-to-action.

   * **[!UICONTROL Call-to-action header text]** Le parole da visualizzare nell&#39;intestazione sopra il pulsante Call-to-action nel modale del contenuto. Il testo predefinito è &quot;Shop these products: &quot;.

   * **[!UICONTROL Call-to-action button text]** Personalizzare il testo sul pulsante Call-to-action. Il testo predefinito è &quot;Buy Now&quot;.

   * **[!UICONTROL Product display options]** Scegliete se visualizzare il **[!UICONTROL Photo]** pulsante **[!UICONTROL Product name]** di invito all&#39;azione.

   * **[!UICONTROL Product URL referral tracking]** Attivate l&#39;attivazione per tracciare i riferimenti da questa app alla pagina del prodotto associata.

   * **[!UICONTROL Referral tracking key-value pairs]** Aggiungi parametri per specificare ulteriormente il tracciamento dei riferimenti dal contenuto dell&#39;app alla pagina del prodotto associata.

* **[!UICONTROL Product page filter]**.

   * **[!UICONTROL Filter UGC by Product ID]**. Selezionate questa opzione per creare un&#39;app per più pagine di prodotto. Filtrare UGC specifico per il prodotto per ogni pagina di prodotto. Potete selezionare una o più cartelle per associare raccolte specifiche all&#39;app.
   * **[!UICONTROL Select Product folders]**. Selezionate le cartelle di prodotto di livello principale da usare per filtrare UGC. Usate CTRL/Comando + clic per selezionare più cartelle. Livefyre utilizza la cartella per determinare quali prodotti visualizzare nell&#39;app in diverse pagine.
   * **[!UICONTROL Show related content]**. Attivate questa opzione per visualizzare il contenuto pubblicato nell&#39;app, ma contrassegnato con un ID prodotto diverso. Una volta visualizzato il contenuto specifico per l&#39;app, Livefyre visualizza il contenuto per altri prodotti e contenuti non associati a un prodotto. Livefyre priorità il contenuto con lo stesso ID prodotto, quindi il contenuto pubblicato nell&#39;app con altri ID prodotto, quindi il contenuto pubblicato nell&#39;app senza ID prodotto.

Per [ulteriori informazioni su come personalizzare un Mosaic tramite Livefyre. js, consultate Opzioni](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) mosaico.
