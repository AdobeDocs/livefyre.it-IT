---
description: Modificate le opzioni di dimensione, larghezza e interazione dell’app Mappa.
seo-description: Modificate le opzioni di dimensione, larghezza e interazione dell’app Mappa.
seo-title: Personalizzazioni scheda funzioni
solution: Experience Manager
title: Personalizzazioni scheda funzioni
uuid: dd43c076-027f-42c8-be2e-7d863d4e3976
translation-type: tm+mt
source-git-commit: a014b5cd618672934843f1adf20d6b2cc504e2d8
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 0%

---


# Personalizzazioni scheda funzioni{#feature-card-customizations}

Modificate le opzioni di dimensione, larghezza e interazione dell’app Mappa.

<!-- 
r_feature_card_customization.dita
 -->

Le app delle schede delle funzioni includono solo personalizzazioni standard:** [!UICONTROL Theme]**, colore del marchio, famiglia di font e dimensione font.

È possibile personalizzare le schede delle funzioni utilizzando:

* **[!UICONTROL Style]** e  **[!UICONTROL Config]** le opzioni per tutte le app in  **[!UICONTROL App Designer]**. Consultate Personalizzazione delle app per informazioni dettagliate sulle opzioni **[!UICONTROL Style]** e **[!UICONTROL Config]** standard per tutte le app in **[!UICONTROL App Designer]**.

* Strumenti di integrazione. Consulta Integrazioni app per ulteriori informazioni su come personalizzare le app tramite gli strumenti di integrazione.
* **[!UICONTROL Call-to-action button]** Puoi usare il pulsante Invito all’azione con un catalogo di prodotti per indirizzare gli utenti a un prodotto o al tuo sito per ulteriori azioni.

   * **[!UICONTROL Call-to-action button]** Attivate l&#39;interruttore per visualizzare il pulsante Invito all&#39;azione.
   * **[!UICONTROL Require rights to display products]** Attivate l&#39;opzione per richiedere al proprietario del contenuto di concedere i diritti per il contenuto prima che venga visualizzato un pulsante Invito all&#39;azione per il contenuto.

      >[!NOTE]
      >
      >Il contenuto viene visualizzato anche se i diritti non sono concessi per il contenuto, ma il pulsante Invito all’azione non viene visualizzato con il contenuto a meno che non siano stati concessi i diritti per il contenuto.

   * **[!UICONTROL Call-to-action header text]** Le parole da visualizzare nell’intestazione sopra il pulsante Invito all’azione nella modalità contenuto. Il testo predefinito è &quot;Shop this products:&quot;.
   * **[!UICONTROL Call-to-action button text]** Personalizzare il testo sul pulsante Invito all’azione. Il testo predefinito è &quot;Buy Now&quot;.
   * **[!UICONTROL Product display options]** Scegliere se visualizzare il pulsante  **[!UICONTROL Photo]** e il pulsante  **[!UICONTROL Product name]** con l&#39;azione.
   * **[!UICONTROL Product URL referral tracking]** Passate all&#39;attivazione per tenere traccia dei riferimenti da questa app alla pagina di prodotto associata.
   * **[!UICONTROL Referral tracking key-value pairs]** Aggiungi parametri per specificare ulteriormente il tracciamento del riferimento dal contenuto dell&#39;app alla pagina del prodotto associata.

* **[!UICONTROL Product page filter]**

   * **[!UICONTROL Filter UGC by Product ID]**. Selezionate questa opzione per creare un&#39;app per più pagine di prodotto. Filtra l&#39;UGC specifico per il prodotto nell&#39;app per ogni pagina di prodotto. Potete selezionare una o più cartelle per associare raccolte specifiche all&#39;app.
   * **[!UICONTROL Select Product folders]**. Selezionate le cartelle di prodotti di livello principale da usare per filtrare l’UGC. Utilizzate `CTRL/Command + click` per selezionare più cartelle. Livefyre utilizza la cartella per determinare quali prodotti in quella cartella visualizzare nell&#39;app su varie pagine.
   * **[!UICONTROL Show related content]**. Attivate questa opzione per visualizzare il contenuto pubblicato nell&#39;app, ma con tag con un ID prodotto diverso. Dopo la visualizzazione del contenuto specifico del prodotto per l&#39;app, Livefyre visualizza il contenuto per altri prodotti e contenuti non associati a un prodotto. Livefyre assegna priorità al contenuto con lo stesso ID prodotto, quindi al contenuto pubblicato nell&#39;app con altri ID prodotto, quindi al contenuto pubblicato nell&#39;app senza ID prodotto.

