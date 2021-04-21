---
description: Fornire contenuti generati dagli utenti specifici per i prodotti in punti specifici del percorso di clienti per aumentare l’intento di acquisto e la conversione utilizzando la funzione Commerce UGC.
title: Commerce UGC
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '854'
ht-degree: 2%

---


# Commerce UGC{#ugc-commerce}

Fornire contenuti generati dagli utenti specifici per i prodotti in punti specifici del percorso di clienti per aumentare l’intento di acquisto e la conversione utilizzando la funzione Commerce UGC.

Utilizza la funzione Commerce UGC per influenzare l’intento di acquisto e la conversione sulle pagine UGC e sui dettagli del prodotto. Accelerare il time-to-market associando facilmente UGC con l&#39;inventario dei prodotti. Crea brand loyalty creando community utilizzando UGC per evidenziare storie di clienti autentiche.

AEM Livefyre offre diversi modi per importare informazioni sul catalogo dei prodotti, tra cui SKU, immagini in miniatura, prezzo e nome del prodotto. Gestisci facilmente l’associazione di prodotti con UGC utilizzando le richieste di diritti di AEM Livefyre, l’assegnazione di tag alle regole in streaming automatico e i flussi di lavoro di moderazione.

Oltre a influenzare l’acquisto, le funzionalità dell’offerta commerciale UGC di Livefyre AEM possono essere sfruttate per favorire le conversioni in altri modi, tra cui:

* Generazione di lead B2B: posizionare i pulsanti di chiamata all&#39;azione sotto UGC per acquisire i lead
* Download di app B2C: richiesta agli utenti di scaricare un&#39;app
* Riferimenti all&#39;articolo: collegare gli utenti ad articoli relativi a pezzi di UGC

Posiziona le chiamate alle azioni del prodotto insieme a UGC per favorire la conversione. Puoi:

* Aggiungi UGC specifico per prodotto su scala a migliaia di pagine di dettaglio del prodotto.
* Incorpora le app di visualizzazione di AEM Livefyre che supportano le funzionalità di e-commerce UGC, come Media Wall e Mosaic nelle pagine dei dettagli del prodotto.
* Utilizza codici di tracciamento dei riferimenti configurabili con una soluzione di analisi per misurare le conversioni dai CTA dei prodotti inseriti su UGC e UGC posizionati sulle pagine dei dettagli del prodotto.

Gli utenti di AEM Commerce possono integrare facilmente il catalogo di prodotti esistente in Livefyre per incrementare il coinvolgimento degli utenti nelle app di visualizzazione di Livefyre. Gli utenti Livefyre che non utilizzano AEM Commerce possono importare manualmente i loro cataloghi di prodotti in Livefyre. Per ulteriori informazioni, consulta [Caricamento di prodotti in Livefyre tramite Caricamento di file](/help/using/c-features-livefyre/c-ugc-commerce.md) .

App che utilizzano questa funzione:

* [Scheda funzione](../c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app). Per informazioni su come utilizzare il Commerce UGC in una scheda funzioni, consulta [Personalizzazioni di schede funzioni](../c-about-apps/c-feature-card-app/c-feature-card-app.md#section_uds_gzm_5y).

* [](../c-about-apps/c-filmstrip-app/c-filmstrip-app.md#concept_jpc_n2j_jbb). Per informazioni su come utilizzare il Commerce UGC in un Filmstrip, vedere [Personalizzazioni di sequenze](../c-about-apps/c-filmstrip-app/c-filmstrip-customizations.md#c_filmstrip_customizations).

* [Media Wall](../c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app). Per informazioni su come utilizzare UGC Commerce in a Media Wall, consulta [Personalizzazioni di Media Wall](../c-about-apps/c-media-wall-app/r-media-wall-customizations.md#r_media_wall_customizations).

* [Mosaico](../c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app). Per informazioni su come utilizzare il Commerce UGC in un Mosaic, consulta [Personalizzazioni Mosaic](../c-about-apps/c-mosaic-app/c-mosaic-customizations.md#c_mosaic_customizations).

## Panoramica: Come utilizzare il pulsante di invito all’azione Commerce UGC {#section_s2d_tln_n1b}

1. Crea un&#39;app con un pulsante di invito all&#39;azione. Consulta [Aggiungere un pulsante di invito all&#39;azione a un&#39;app](/help/using/c-features-livefyre/c-call-to-action-button.md#task_36190DD1C8204C7793CB7EEA379C2155).
1. Aggiungi il tuo catalogo prodotti a Livefyre. È possibile importare il contenuto in uno dei due modi seguenti:

   * [Importa i prodotti in Livefyre utilizzando AEM ](https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/livefyre.html) Commerce se utilizzi AEM Commerce.
   * [Carica i prodotti in ](/help/using/c-features-livefyre/c-ugc-commerce.md) Livefyrese non utilizzi AEM Commerce.

1. Associa i prodotti al contenuto. Puoi eseguire questa operazione in uno dei quattro modi seguenti:

   * Dalla libreria. Consulta [Associare i prodotti con i contenuti utilizzando la libreria](../c-library/t-associate-products-with-content-using-the-library.md#t_associate_products_with_content_using_the_library)
   * Da ModQ. Consulta [Contenuto moderato con ModQ](/help/using/c-features-livefyre/c-about-moderation/c-modq.md)
   * Dal contenuto dell’app. Consulta [Aggiungere un pulsante di invito all&#39;azione a un&#39;app](/help/using/c-features-livefyre/c-call-to-action-button.md)
   * Da un flusso. Consulta [Opzioni regola flusso per tutte le regole di flusso](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

## Caricare prodotti su Livefyre utilizzando il caricamento file {#section_n1s_4hz_m1b}

Carica i prodotti da utilizzare con il pulsante di invito all’azione per aggiungere prodotti da associare al contenuto o per modificare ed eliminare i file esistenti.

>[!NOTE]
>
>Il caricamento di un file in una cartella con file esistenti eliminerà tutti i file presenti in tale cartella e li sovrascriverà con il nuovo file.

1. Passa a **[!UICONTROL Network Settings > Products.]**
1. Crea un **[!UICONTROL Product Folder]** o utilizza un **[!UICONTROL Product Folder]** esistente.

1. Fai clic su **[!UICONTROL Product Folder]** per selezionarlo.
1. Fai clic sul pulsante **[!UICONTROL Upload Products]** .
1. Carica un file di prodotto in uno dei seguenti formati:

   * Formato file di Google Products
   * Formato Livefyre (vedi sotto)

   Carica un file JSON nel formato standard. È possibile scaricare un modello per visualizzare un esempio del formato standard. Di seguito è riportato un esempio di una linea di prodotto in un modello. Segue la sequenza `{"key": "value", "key": "value"}, {"key": "value", "key": "value"}`:

   ```
   {"id": "1", "title": "Flex RN 2017", "isFolder": false, "description": "Flex RN 2017", "price": "$85", "sku": "sku11111", "summary": "This brand is a member of the Sustainable Apparel Coalition", "features": "Cushioning: Lightweight, flexible response", "url": "www.shopping.com/shoes-flex-rn-2017/product/9", "attributes": [{"type": "color", "value": "blue"}
   ```

   La tabella spiega le coppie chiave-valore necessarie per caricare i prodotti:

## Coppie chiave/valore per il caricamento del catalogo dei prodotti in formato standard

| Chiave | Tipo | Descrizione |
|--- |--- |--- |
| id | Stringa | ID univoco del prodotto. |
| incorporato | Oggetto | Allegato immagine `0embed $ref: '../partials/schemas.yaml#/oEmbed'` |
| title | Stringa | Titolo del prodotto. |
| isFolder | Booleano | Se true, il prodotto viene trattato come una cartella (ad esempio, uomini, donne, ecc.). |
| parentId | Stringa | Definisce la cartella in cui si trova il prodotto. |
| descrizione | Stringa | Descrizione del prodotto. |
| prezzo | Stringa | Valore del prodotto in dollari. Ad esempio, &#39;23.36.&#39; |
| palude | Stringa | Unità di conservazione delle scorte (SKU) del prodotto. |
| url | Stringa | Collega alla pagina del prodotto. |
| Abilitato | Booleano | Il valore True indica che il prodotto è attivo. |
| attributes | Array | Tipi e valori che definiscono il prodotto (ad esempio, colore, dimensione, ecc.). Questo è un array di oggetti.</br>**Proprietà:** </br>tipo  </br>Tipo: </br>Descrizione stringa: Colore, dimensione  </br>valore  </br>Tipo: Stringa  </br>Descrizione: Verde, XS |
| tag | Array | Tag che definiscono categorie di contenuti (ad esempio, automobili, scarpe, ecc.). Questo è un array di stringhe. |

## ModQ {#section_os1_v4t_n1b}

In ModQ puoi associare il contenuto ai prodotti del catalogo di prodotti in linea con i flussi di lavoro di moderazione esistenti. Per informazioni su come utilizzare Commerce UGC con ModQ, consulta [Contenuto moderato con ModQ](/help/using/c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md).

## Flussi {#section_qtj_v4t_n1b}

Puoi associare automaticamente i prodotti al contenuto utilizzando le regole di flusso, quindi pubblicare il contenuto automaticamente in un’app, salvarlo nella libreria o moderarlo utilizzando ModQ. Per ulteriori informazioni su come utilizzare UGC Commerce con regole di flusso, consulta [Opzioni delle regole di flusso per tutte le regole di flusso](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
