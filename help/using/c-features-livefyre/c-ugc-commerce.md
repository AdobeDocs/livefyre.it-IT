---
description: Distribuire UGC specifici per i prodotti in punti specifici del percorso del cliente per aumentare l'intento di acquisto e la conversione utilizzando la funzione UGC Commerce.
seo-description: Distribuire UGC specifici per i prodotti in punti specifici del percorso del cliente per aumentare l'intento di acquisto e la conversione utilizzando la funzione UGC Commerce.
seo-title: Commerce UGC
solution: Experience Manager
title: Commerce UGC
uuid: 71e64901-a2b6-4957-ba88-058e4eaca537
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '877'
ht-degree: 2%

---


# UGC Commerce{#ugc-commerce}

Distribuire UGC specifici per i prodotti in punti specifici del percorso del cliente per aumentare l&#39;intento di acquisto e la conversione utilizzando la funzione UGC Commerce.

Utilizzate la funzione UGC Commerce per influenzare l&#39;intento di acquisto e la conversione sulle pagine UGC e sui dettagli del prodotto. Velocizza il time-to-market associando senza soluzione di continuità UGC con l&#39;inventario dei prodotti. Crea fidelizzazione del marchio creando community che utilizzano UGC per evidenziare storie di clienti autentiche.

AEM Livefyre offre diversi modi per importare informazioni sul catalogo prodotti, tra cui SKU, immagini in miniatura, prezzo e nome del prodotto. Gestite facilmente l&#39;associazione di prodotti con UGC utilizzando AEM richieste di diritti di Livefyre, tag a flusso automatico delle regole e flussi di lavoro di moderazione.

Oltre a influenzare l&#39;acquisto, le funzionalità dell&#39;offerta commerciale UGC di AEM Livefyre possono essere sfruttate per stimolare le conversioni in altri modi, tra cui:

* Generazione di lead B2B: inserire i pulsanti di invito all’azione in UGC per acquisire i lead
* Download da app B2C: richiedere agli utenti di scaricare un&#39;app
* Riferimenti all&#39;articolo: collegare gli utenti agli articoli relativi a pezzi di UGC

Posiziona le chiamate alle azioni dei prodotti insieme a UGC per promuovere la conversione. Puoi:

* Aggiungi UGC per prodotti specifici a migliaia di pagine di dettagli del prodotto.
* AEM le app di visualizzazione Livefyre che supportano le funzionalità di e-commerce UGC, come Media Wall e Mosaic, nelle pagine dei dettagli del prodotto.
* Utilizza codici di monitoraggio dei riferimenti configurabili con una soluzione di analisi per misurare le conversioni dai CTA dei prodotti inseriti su UGC e UGC inseriti nelle pagine dei dettagli dei prodotti.

AEM utenti di Commerce possono integrare facilmente il catalogo di prodotti esistente in Livefyre per attirare l&#39;utente nelle app di visualizzazione di Livefyre. Gli utenti Livefyre che non utilizzano AEM Commerce possono importare manualmente i loro cataloghi di prodotti in Livefyre. Per ulteriori informazioni, consultate [Caricare i prodotti in Livefyre mediante il caricamento di file](/help/using/c-features-livefyre/c-ugc-commerce.md).

App che utilizzano questa funzione:

* [Scheda](../c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app) delle funzioni. Per informazioni sull&#39;utilizzo di UGC Commerce in una scheda delle funzioni, vedere [Personalizzazioni delle schede delle funzioni](../c-about-apps/c-feature-card-app/c-feature-card-app.md#section_uds_gzm_5y).

* [](../c-about-apps/c-filmstrip-app/c-filmstrip-app.md#concept_jpc_n2j_jbb). Per informazioni sull’utilizzo di UGC Commerce in un Filmstrip, vedere [Personalizzazioni di Filmstrip](../c-about-apps/c-filmstrip-app/c-filmstrip-customizations.md#c_filmstrip_customizations).

* [Media Wall](../c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app). Per informazioni sull&#39;utilizzo di UGC Commerce in a Media Wall, vedere [Media Wall Customizations](../c-about-apps/c-media-wall-app/r-media-wall-customizations.md#r_media_wall_customizations).

* [Mosaico](../c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app). Per informazioni sull&#39;utilizzo di UGC Commerce in a Mosaic, vedere [Mosaic Customizations](../c-about-apps/c-mosaic-app/c-mosaic-customizations.md#c_mosaic_customizations).

## Panoramica: Come utilizzare il pulsante Chiamata all&#39;azione di UGC Commerce {#section_s2d_tln_n1b}

1. Crea un&#39;app con un pulsante di invito all&#39;azione. Consultate [Aggiungere un pulsante di invito all&#39;azione a un&#39;app](/help/using/c-features-livefyre/c-call-to-action-button.md#task_36190DD1C8204C7793CB7EEA379C2155).
1. Aggiungi il catalogo prodotti a Livefyre. Potete importare il contenuto in uno dei due modi seguenti:

   * [Importa i prodotti in Livefyre utilizzando AEM ](https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/livefyre.html) Commercese utilizzi AEM Commerce.
   * [Caricate i prodotti in ](/help/using/c-features-livefyre/c-ugc-commerce.md) Livefyrese non utilizzate AEM Commerce.

1. Associate i prodotti al contenuto. Potete eseguire questa operazione in uno dei quattro modi seguenti:

   * Dalla libreria. Vedere [Associare i prodotti con i contenuti mediante la libreria](../c-library/t-associate-products-with-content-using-the-library.md#t_associate_products_with_content_using_the_library)
   * Da ModQ. Vedere [Contenuto moderato con ModQ](/help/using/c-features-livefyre/c-about-moderation/c-modq.md)
   * Da Contenuto app. Vedere [Aggiunta di un pulsante di invito all&#39;azione a un&#39;app](/help/using/c-features-livefyre/c-call-to-action-button.md)
   * Da un flusso. Vedere [Opzioni regola di flusso per tutte le regole di flusso](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

## Caricamento di prodotti in Livefyre tramite caricamento di file {#section_n1s_4hz_m1b}

Caricate i prodotti da usare con il pulsante Invito all’azione per aggiungere prodotti da associare ai contenuti o per modificare ed eliminare file esistenti.

>[!NOTE]
>
>Il caricamento di un file in una cartella contenente file esistenti eliminerà tutti i file in tale cartella e li sovrascriverà con il nuovo file.

1. Passa a **[!UICONTROL Network Settings > Products.]**
1. Creare un **[!UICONTROL Product Folder]** o utilizzare un **[!UICONTROL Product Folder]** esistente.

1. Fare clic su **[!UICONTROL Product Folder]** per selezionarlo.
1. Fare clic sul pulsante **[!UICONTROL Upload Products]**.
1. Caricate un file di prodotto in uno dei seguenti formati:

   * Formato file di Google Products
   * Formato Livefyre (vedere di seguito)

   Caricate un file JSON nel formato standard. Potete scaricare un modello per visualizzare un esempio del formato standard. Esempio di una linea di prodotti in un modello. Segue la sequenza `{"key": "value", "key": "value"}, {"key": "value", "key": "value"}`:

   ```
   {"id": "1", "title": "Flex RN 2017", "isFolder": false, "description": "Flex RN 2017", "price": "$85", "sku": "sku11111", "summary": "This brand is a member of the Sustainable Apparel Coalition", "features": "Cushioning: Lightweight, flexible response", "url": "www.shopping.com/shoes-flex-rn-2017/product/9", "attributes": [{"type": "color", "value": "blue"}
   ```

   La tabella illustra le coppie chiave-valore da usare per caricare i prodotti:

## Coppie chiave/valore per il catalogo di prodotti Carica formato standard

| Chiave | Tipo | Descrizione |
|--- |--- |--- |
| id | Stringa | ID univoco del prodotto. |
| oembed | Oggetto | Allegato immagine `0embed $ref: '../partials/schemas.yaml#/oEmbed'` |
| title | Stringa | Titolo del prodotto. |
| isFolder | Booleano | Se true, il prodotto viene trattato come una cartella (ad esempio, uomini, donne ecc.). |
| parentId | Stringa | Definisce la cartella in cui si trova il prodotto. |
| description | Stringa | Descrizione del prodotto. |
| price | Stringa | Valore del prodotto in dollari. Ad esempio, &#39;23.36.&#39; |
| sku | Stringa | Unità di conservazione delle scorte (SKU) del prodotto. |
| url | Stringa | Link alla pagina del prodotto. |
| Abilitato | Booleano | Il valore True indica che il prodotto è attivo. |
| attribute | Array | Tipi e valori che definiscono il prodotto (ad esempio, colore, dimensione, ecc.). Si tratta di un array di oggetti.</br>**Proprietà:** </br>tipo  </br>Tipo: Descrizione </br>stringa: Colore, dimensione  </br>valore  </br>Tipo: Descrizione  </br>stringa: Verde, XS |
| tags | Matrice | Tag che definiscono le categorie di contenuto (ad esempio, automobili, scarpe ecc.). Questo è un array di stringhe. |

## ModQ {#section_os1_v4t_n1b}

Puoi associare il contenuto ai prodotti del catalogo prodotti in ModQ in linea con i flussi di lavoro di moderazione esistenti. Per informazioni sull&#39;utilizzo di UGC Commerce con ModQ, vedere [Moderate Content Using ModQ](/help/using/c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md).

## Flussi {#section_qtj_v4t_n1b}

Puoi associare automaticamente i prodotti al contenuto utilizzando le regole di flusso, quindi pubblicare automaticamente il contenuto in un&#39;app, salvarlo nella libreria o Moderarlo con ModQ. Per ulteriori informazioni sull&#39;utilizzo di UGC Commerce con regole di flusso, vedere [Opzioni regola di flusso per tutte le regole di flusso](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
