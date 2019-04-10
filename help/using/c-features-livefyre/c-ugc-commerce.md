---
description: Distribuisci UGC specifici per i singoli prodotti in punti specifici
  del percorso del cliente per aumentare l'intento di acquisto e la conversione tramite
  la funzione UGC Commerce.
seo-description: Distribuisci UGC specifici per i singoli prodotti in punti specifici
  del percorso del cliente per aumentare l'intento di acquisto e la conversione tramite
  la funzione UGC Commerce.
seo-title: UGC Commerce
solution: Experience Manager
title: UGC Commerce
uuid: 71 e 64901-a 2 b 6-4957-ba 88-058 e 4 eaca 537
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# UGC Commerce{#ugc-commerce}

Distribuisci UGC specifici per i singoli prodotti in punti specifici del percorso del cliente per aumentare l'intento di acquisto e la conversione tramite la funzione UGC Commerce.

Utilizzate la funzione Commerce UGC per influenzare l'intento di acquisto e la conversione su pagine di dettaglio UGC e sui prodotti. Time time sul mercato, associando facilmente UGC alle scorte dei prodotti. Crea fidelizzazione creando community tramite UGC per evidenziare testimonianze dei clienti autentici.

AEM Livefyre offre diversi metodi per importare informazioni sui cataloghi dei prodotti, inclusi SKU, immagini in miniatura, prezzo e nome del prodotto. Gestite facilmente l'associazione di prodotti con UGC utilizzando le richieste dei diritti di AEM Livefyre, i tag di regole per flussi automatici e i flussi di lavoro di moderazione.

Oltre ad influenzare l'acquisto, le funzionalità nell'offerta commerce UGC di AEM Livefyre possono essere sfruttate per stimolare le conversioni in altri modi, tra cui:

* Generazione di lead B 2 B: Inserire pulsanti Call-to-action in UGC per acquisire i lead
* Download delle app B 2 C: richiedere agli utenti di scaricare un'app
* Referenti articolo: collegare gli utenti a articoli correlati a parti di UGC

Inserite call-to-actions di prodotto con UGC per promuovere la conversione. È possibile:

* Aggiungete UGC specifici per il prodotto a migliaia di pagine di dettaglio del prodotto.
* Incorporate le app di visualizzazione di AEM Livefyre che supportano le funzionalità del commercio UGC quali Media Wall e Mosaic sulle pagine dei dettagli dei prodotti.
* Utilizzate codici di tracciamento del referente configurabili con una soluzione di analisi per misurare le conversioni da CTC prodotto inseriti su UGC e UGC inseriti nelle pagine dei dettagli del prodotto.

Gli utenti di AEM Commerce possono integrare facilmente il proprio catalogo di prodotti in Livefyre per stimolare il coinvolgimento degli utenti nelle app di visualizzazione di Livefyre. Gli utenti Livefyre che non utilizzano AEM Commerce possono importare manualmente i cataloghi di prodotti in Livefyre. Per ulteriori informazioni, consultate [Caricare prodotti in Livefyre mediante caricamento](/help/using/c-features-livefyre/c-ugc-commerce.md)file.

App che utilizzano questa funzione:

* [Scheda Funzioni](../c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app). Per informazioni su come utilizzare UGC Commerce in una scheda Feature, consultate [Personalizzazione delle schede delle funzioni](../c-about-apps/c-feature-card-app/c-feature-card-app.md#section_uds_gzm_5y).

* [](../c-about-apps/c-filmstrip-app/c-filmstrip-app.md#concept_jpc_n2j_jbb). Per informazioni su come utilizzare UGC Commerce in un Filmstrip, consultate [Personalizzazione filmstrip](../c-about-apps/c-filmstrip-app/c-filmstrip-customizations.md#c_filmstrip_customizations).

* [Media Wall](../c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app). Per informazioni sull'utilizzo di UGC Commerce in un Media Wall, consultate [Personalizzazione di contenuti multimediali](../c-about-apps/c-media-wall-app/r-media-wall-customizations.md#r_media_wall_customizations).

* [Mosaic](../c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app). Per informazioni su come utilizzare UGC Commerce in Mosaic, consultate [Personalizzazioni mosaico](../c-about-apps/c-mosaic-app/c-mosaic-customizations.md#c_mosaic_customizations).

## Panoramica: Come utilizzare il pulsante di invito all'azione UGC Commerce {#section_s2d_tln_n1b}

1. Creare un'app con un pulsante di invito all'azione. Consultate [Aggiungere un pulsante Call-to-action a un'app](/help/using/c-features-livefyre/c-call-to-action-button.md#task_36190DD1C8204C7793CB7EEA379C2155).
1. Aggiungete il catalogo di prodotti a Livefyre. Potete importare il contenuto in uno dei due modi seguenti:

   * [Importa prodotti in Livefyre utilizzando AEM Commerce](https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/livefyre.html) se usi AEM Commerce.
   * [Carica prodotti in Livefyre](/help/using/c-features-livefyre/c-ugc-commerce.md) se non usi AEM Commerce.

1. Associare i prodotti ai contenuti. Puoi eseguire questa operazione in quattro modi:

   * Dalla libreria. Consultate [Associazione di prodotti con contenuto tramite la libreria](../c-library/t-associate-products-with-content-using-the-library.md#t_associate_products_with_content_using_the_library)
   * Da modq. Vedere [Moderazione contenuto tramite modq](/help/using/c-features-livefyre/c-about-moderation/c-modq.md)
   * Da Contenuto app. Consultate [Aggiungere un pulsante Call-to-action a un'app](/help/using/c-features-livefyre/c-call-to-action-button.md)
   * Da un flusso. Consultate [Opzioni regola di flusso per tutte le regole dei flussi](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

## Carica prodotti in Livefyre mediante caricamento file {#section_n1s_4hz_m1b}

Caricare i prodotti da utilizzare con il pulsante di invito all'azione per aggiungere prodotti da associare al contenuto o per modificare ed eliminare file esistenti.

>[!NOTE]
>
>Quando si carica un file in una cartella con file esistenti, vengono eliminati tutti i file presenti nella cartella e vengono sovrascritti con il nuovo file.

1. Passa a **[!UICONTROL Network Settings > Products.]**
1. Creare un **[!UICONTROL Product Folder]** file o utilizzarne uno esistente **[!UICONTROL Product Folder]**.

1. Fate clic sulla **[!UICONTROL Product Folder]** casella per selezionarla.
1. Fate clic sul **[!UICONTROL Upload Products]** pulsante.
1. Caricate un file di prodotto in uno dei seguenti formati:

   * Formato file Google Products
   * Formato Livefyre (vedi di seguito)
   Carica un file JSON nel formato standard. Potete scaricare un modello per visualizzare un esempio del formato standard. Esempio di linea di prodotto in un modello. Segue la sequenza `{"key": "value", "key": "value"}, {"key": "value", "key": "value"}`:

   ```
   {"id": "1", "title": "Flex RN 2017", "isFolder": false, "description": "Flex RN 2017", "price": "$85", "sku": "sku11111", "summary": "This brand is a member of the Sustainable Apparel Coalition", "features": "Cushioning: Lightweight, flexible response", "url": "www.shopping.com/shoes-flex-rn-2017/product/9", "attributes": [{"type": "color", "value": "blue"}
   ```

   La tabella descrive le coppie chiave-valore necessarie per caricare i prodotti:

## Coppie chiave/valore per il formato standard del catalogo prodotti

| Chiave | Tipo | Descrizione |
|--- |--- |--- |
| id | Stringa | ID univoco del prodotto. |
| oembed | Oggetto | Allegato immagine `0embed $ref: '../partials/schemas.yaml#/oEmbed'` |
| title | Stringa | Titolo prodotto. |
| Isfolder | Booleano | Se true, il prodotto viene trattato come una cartella (ad esempio, menu, donne, ecc.). |
| Parentid | Stringa | Definisce la cartella in cui si trova il prodotto. |
| description | Stringa | Descrizione del prodotto. |
| prezzo | Stringa | Valore del prodotto in dollari. Ad esempio,'23.36. |
| sku | Stringa | Unità di mantenimento Stock (SKU) del prodotto. |
| url | Stringa | Collega alla pagina del prodotto. |
| enabled | Booleano | Il valore True significa che il prodotto è attivo. |
| attributi | Matrice | Tipi e valori che definiscono il prodotto (ad esempio, colore, dimensione ecc.). Si tratta di un array di oggetti.</br>**Proprietà:**</br>type </br>Type: Stringdescription</br>: Tipo di colore, </br></br>Tipo di dimensione: </br>Descrizione stringa: Verde, XS |
| tag | Matrice | Tag che definiscono categorie di contenuto (ad esempio, automobili, scarpe ecc.). Si tratta di un array di stringhe. |

## Modq {#section_os1_v4t_n1b}

Potete associare contenuto ai prodotti dal catalogo di prodotti in modq in linea con i flussi di lavoro di moderazione esistenti. Per informazioni sull'utilizzo di UGC Commerce con modq, consultate [Moderazione contenuto mediante modq](/help/using/c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md).

## Flussi {#section_qtj_v4t_n1b}

Potete associare automaticamente i prodotti al contenuto utilizzando regole di streaming, quindi pubblicare automaticamente il contenuto in un'app, salvarlo nella libreria o moderarlo tramite modq. Per ulteriori informazioni sull'utilizzo di UGC Commerce con regole di streaming, consultate [Opzioni regola di flusso per tutte le regole dei flussi](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
