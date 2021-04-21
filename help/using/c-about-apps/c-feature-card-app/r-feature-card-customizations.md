---
description: Modifica le opzioni di dimensione, larghezza e interazione dell’app Mappa.
title: Personalizzazioni delle schede di funzionalità
exl-id: b907885a-211d-4628-9955-5f1a5ec577cf
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# Personalizzazioni delle schede di funzionalità{#feature-card-customizations}

Modifica le opzioni di dimensione, larghezza e interazione dell’app Mappa.

<!-- 
r_feature_card_customization.dita
 -->

Le app per schede di funzioni includono solo personalizzazioni standard:** [!UICONTROL Theme]**, colore del marchio, famiglia di font e dimensione del font.

Puoi personalizzare le schede delle funzioni utilizzando:

* **[!UICONTROL Style]** e  **[!UICONTROL Config]** le opzioni per tutte le app in  **[!UICONTROL App Designer]**. Consulta Personalizzazione delle app per i dettagli sulle opzioni **[!UICONTROL Style]** e **[!UICONTROL Config]** standard per tutte le app in **[!UICONTROL App Designer]**.

* Strumenti di integrazione. Per ulteriori informazioni su come personalizzare le app utilizzando gli strumenti di integrazione, consulta Integrazioni app .
* **[!UICONTROL Call-to-action button]** Puoi usare il pulsante Invito all’azione con un catalogo di prodotti per indirizzare gli utenti a un prodotto o al sito per ulteriori azioni.

   * **[!UICONTROL Call-to-action button]** Attiva l&#39;interruttore per visualizzare il pulsante di invito all&#39;azione.
   * **[!UICONTROL Require rights to display products]** Passa all’attivazione per richiedere al proprietario del contenuto di disporre dei diritti per il contenuto prima che venga visualizzato un pulsante di invito all’azione per il contenuto.

      >[!NOTE]
      >
      >Il contenuto viene visualizzato anche se i diritti non sono concessi per il contenuto, ma il pulsante Invito all’azione non viene visualizzato con il contenuto, a meno che non siano concessi i diritti per il contenuto.

   * **[!UICONTROL Call-to-action header text]** Le parole da visualizzare nell’intestazione sopra il pulsante Invito all’azione nel modale del contenuto. La dicitura predefinita è &quot;Acquista questi prodotti:&quot;.
   * **[!UICONTROL Call-to-action button text]** Personalizza il testo del pulsante di invito all’azione. Il testo predefinito è &quot;Acquista ora&quot;.
   * **[!UICONTROL Product display options]** Scegli se visualizzare  **[!UICONTROL Photo]** e  **[!UICONTROL Product name]** con il pulsante di invito all’azione.
   * **[!UICONTROL Product URL referral tracking]** Passa all’attivazione per tenere traccia dei riferimenti da questa app alla pagina di prodotto associata.
   * **[!UICONTROL Referral tracking key-value pairs]** Aggiungi dei parametri per specificare ulteriormente il tracciamento dei riferimenti dal contenuto dell&#39;app alla pagina di prodotto associata.

* **[!UICONTROL Product page filter]**

   * **[!UICONTROL Filter UGC by Product ID]**. Seleziona questa opzione per creare un’app per più pagine di prodotto. Filtra l’UGC specifico per il prodotto nell’app per ogni pagina di prodotto. Puoi selezionare una o più cartelle per associare raccolte specifiche all’app.
   * **[!UICONTROL Select Product folders]**. Seleziona le cartelle di prodotto di livello principale da utilizzare per filtrare gli UGC. Utilizza `CTRL/Command + click` per selezionare più cartelle. Livefyre utilizza la cartella per determinare quali prodotti in tale cartella visualizzare nell’app su varie pagine.
   * **[!UICONTROL Show related content]**. Attiva o disattiva questa opzione per visualizzare il contenuto pubblicato nell’app, ma con tag con un ID prodotto diverso. Dopo che è stato visualizzato il contenuto specifico per il prodotto per l’app, Livefyre visualizza il contenuto per altri prodotti e contenuti non associati a un prodotto. Livefyre dà priorità al contenuto con lo stesso ID prodotto prima, al contenuto pubblicato nell’app con altri ID prodotto, quindi al contenuto pubblicato nell’app senza ID prodotto.
