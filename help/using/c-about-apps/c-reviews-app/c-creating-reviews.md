---
description: Le recensioni offrono un'ampia gamma di personalizzazioni, che consentono di creare un'app di revisione in base alle esigenze e al marchio.
seo-description: Le recensioni offrono un'ampia gamma di personalizzazioni, che consentono di creare un'app di revisione in base alle esigenze e al marchio.
seo-title: Creazione di un'app di revisione
solution: Experience Manager
title: Creazione di un'app di revisione
uuid: 6caeafe7-c04e-484e-b02f-98dc6d9b3184
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Creazione di un'app di revisione{#creating-a-reviews-app}

Le recensioni offrono un'ampia gamma di personalizzazioni, che consentono di creare un'app di revisione in base alle esigenze e al marchio.

Utilizzate l'app di revisione incorporandola in modo personalizzato sul vostro sito come applicazione JS. Non è possibile creare un'app di revisione in Livefyre Studio. Per creare un'app di revisione sul sito, consulta Integrazione [di](/help/implementation/c-app-integrations/c-reviews-integration.md)revisioni.


## Valutazioni {#section_hs5_c4h_21b}

Le valutazioni sono il valore numerico assegnato dagli utenti alla revisione. Ogni revisione deve includere una valutazione, che per impostazione predefinita viene visualizzata come sistema a 5 stelle. (Mentre le valutazioni sono visualizzate come 0,5 - 5 nell'app, Livefyre memorizza un rapporto di X/100 nel backend, ad esempio 1 stella è 20/100 e 2 stelle è 40/100. Questo rapporto viene visualizzato quando si visualizzano le revisioni in Studio.)

La scala di valutazione da 0,5 a 5 può essere configurata fino a un rating di 100, con anche metà delle valutazioni disponibili.

Per ulteriori informazioni, vedere il campo maxRating dell'oggetto convConfig Reviews.

## Attribuzione stile icona valutazione {#section_cqn_c4h_21b}

Le icone di valutazione possono essere personalizzate in base al marchio e allo stile.

Per ulteriori informazioni, vedere **[!UICONTROL Configure Star Ratings]** in Personalizzazione revisioni.

## Dimensioni di valutazione {#section_cnx_snh_21b}

Le dimensioni di valutazione sono le categorie per le quali i revisori valutano il prodotto o il servizio. Esempi di dimensioni di valutazione sono "prestazioni", "progettazione", "costo", "complessivo" o qualsiasi altra categoria scelta.

L'impostazione predefinita prevede la visualizzazione di una dimensione di valutazione "complessiva", tuttavia è possibile definire e implementare più dimensioni di valutazione, come mostrato nell'esempio seguente.

Per ulteriori informazioni, consulta il campo ratingDimensions in Rivedi metadati raccolta.

## Rivedi campi di testo {#section_xcm_4nh_21b}

Potete anche includere altri campi di testo sul prodotto o sull'esperienza in fase di revisione. Ad esempio, i campi di testo possono includere Pro e Cons o Non perdere. Il numero, il titolo e il testo predefinito del campo sono personalizzabili. Per pubblicare la revisione, gli utenti dovranno completare tutti i campi di testo, nonché il titolo della revisione, il corpo e la valutazione. Non è possibile includere campi di testo facoltativi.

Per ulteriori informazioni, consulta il campo ratingDimensions (Dimensioni di valutazione) per i metadati della raccolta Review.

## Riepilogo revisione {#section_ysz_lnh_21b}

Per impostazione predefinita, una sezione di riepilogo viene visualizzata nella parte superiore dell'app di revisione. Questa sezione include una visualizzazione della valutazione media dell'utente e della suddivisione della valutazione per l'insieme Reviews, con la sola visualizzazione di numeri interi. Questa sezione è di sola lettura e può essere nascosta se lo si desidera.

Per ulteriori informazioni, vedere il campo ratingSummaryEnabled per l'oggetto convConfig Reviews.

## Spam and Profanity Filter {#section_hcm_jnh_21b}

Il testo del Titolo e del Corpo di una recensione viene trasmesso attraverso il nostro Filtro Spam e Filtro Profanity non appena viene pubblicata la revisione.

## Personalizzazione del testo {#section_tjf_hnh_21b}

Le stringhe di testo, comprese descrizioni ed etichette, possono essere personalizzate per la lingua o per adattarle al marchio.

## Risposta a una revisione {#section_yng_fnh_21b}

Gli utenti possono rispondere alla propria o a un'altra revisione in ciascuna raccolta di recensioni. Solo gli utenti che hanno eseguito l’accesso possono inviare una risposta a una revisione.

L'opzione che consente agli utenti di rispondere a una revisione è abilitata in Studio. I proprietari possono attivare/disattivare questa impostazione per il livello Rete, Sito o Raccolta. I moderatori possono attivare questa impostazione solo per le raccolte.

## SocialSync e Curate {#section_llh_2nh_21b}

Poiché Recensioni è progettato per aggiungere un valore numerico per ogni elemento di contenuto inviato, SocialSync e Curate non sono supportate con le Recensioni.

## API Review {#section_xrh_wmh_21b}

Le API di revisione sono disponibili per consentire la visualizzazione di informazioni di valutazione e valutazione media degli utenti e delle attività di revisione degli utenti su altre sezioni del sito.

[Valutazioni e recensioni](https://api.livefyre.com/docs/apis/by-category/ratings-and-reviews)

* **[!UICONTROL Bootstrap API Endpoint]** L'endpoint API di Bootstrap consente la lettura della revisione da parte di motori di ricerca come Google in modo che il contenuto e le parole chiave possano migliorare l'ottimizzazione del motore di ricerca.

* **[!UICONTROL Average User Ratings]** L'API Average User Ratings (Valutazione utente media) recupera la valutazione media degli utenti per una o più raccolte di recensioni, consentendo di creare una visualizzazione di queste informazioni in una pagina indice o di aggiungerle a una pagina di indice di ricerca.

* **[!UICONTROL Ratings Breakdown]** L'API di suddivisione valutazioni recupera una suddivisione di tutte le valutazioni per una raccolta di recensioni specifica e consente di creare una visualizzazione che mostra il numero di revisioni associate a ciascuna valutazione a stella.

* **[!UICONTROL User Reviews]** L'API User Reviews recupera le revisioni più recenti per un utente specifico. Questa attività può essere utilizzata per visualizzare le revisioni di un utente sulla pagina del profilo pubblico.
