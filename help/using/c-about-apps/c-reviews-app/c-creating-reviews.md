---
description: Revisioni offre un’ampia gamma di personalizzazioni, che ti consentono di creare un’app di revisione che corrisponda alle tue esigenze e alle tue esigenze di branding.
title: Creazione di un'app di revisione
exl-id: 14f074d2-922c-4997-8d7d-f2c92f069e07
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 0%

---

# Creazione di un&#39;app di revisione{#creating-a-reviews-app}

Revisioni offre un’ampia gamma di personalizzazioni, che ti consentono di creare un’app di revisione che corrisponda alle tue esigenze e alle tue esigenze di branding.

Utilizza l&#39;app Reviews incorporandola su misura sul tuo sito come applicazione JS. Non è possibile creare un&#39;app di revisione in Livefyre Studio. Per creare un&#39;app di revisione sul sito, consulta [Integrazione di revisioni](/help/implementation/c-app-integrations/c-reviews-integration.md).


## Valutazioni {#section_hs5_c4h_21b}

Le valutazioni sono il valore numerico assegnato dagli utenti alla revisione. Ogni revisione deve includere una valutazione, che viene visualizzata come sistema a 5 stelle per impostazione predefinita. (Mentre le valutazioni sono visualizzate come 0,5 - 5 nell’app, Livefyre memorizza un rapporto di X/100 nel backend, in modo che 1 stella sia 20/100 e 2 stelle sia 40/100. Questo rapporto viene visualizzato quando si visualizzano le revisioni in Studio.)

La scala di valutazione da 0,5 a 5 può essere configurata fino a un rating di 100, con anche la metà delle valutazioni disponibili.

Per ulteriori informazioni, vedere il campo maxRating per l&#39;oggetto convConfig Reviews .

## Stile dell&#39;icona di valutazione {#section_cqn_c4h_21b}

Le icone di valutazione possono essere personalizzate in base al tuo marchio e stile.

Per ulteriori informazioni, consulta **[!UICONTROL Configure Star Ratings]** in Personalizzazione delle revisioni.

## Dimension di valutazione {#section_cnx_snh_21b}

Le dimensioni di valutazione sono le categorie per le quali i revisori valutano il prodotto o il servizio. Esempi di dimensioni di valutazione sono &quot;prestazioni&quot;, &quot;progettazione&quot;, &quot;costo&quot;, &quot;complessivo&quot; o qualsiasi altra categoria scelta.

L’impostazione predefinita consiste nel visualizzare una dimensione di valutazione &quot;complessiva&quot;, tuttavia è possibile definire e implementare più dimensioni di valutazione, come illustrato nell’esempio seguente.

Per ulteriori informazioni, vedere il campo ratingDimensions in Review Collection Metadata.

## Rivedi campi di testo {#section_xcm_4nh_21b}

Puoi anche includere campi di testo aggiuntivi sul prodotto o sull’esperienza da esaminare. Ad esempio, i campi di testo potrebbero includere Pro e Cons o Non perdere. Il numero, il titolo e il testo predefinito del campo sono personalizzabili. Per pubblicare la revisione, gli utenti dovranno completare tutti i campi di testo, nonché il titolo della revisione, il corpo e la valutazione. Non è possibile includere campi di testo facoltativi.

Per ulteriori informazioni, vedere il campo ratingDimensions per i metadati della raccolta di revisione.

## Riepilogo recensione {#section_ysz_lnh_21b}

Per impostazione predefinita, una sezione di riepilogo viene visualizzata nella parte superiore dell’app Reviews. Questa sezione include una visualizzazione della Valutazione media utente e della Disaggregazione di valutazione per l&#39;insieme Reviews, con solo numeri interi. Questa sezione è di sola lettura e può essere nascosta se lo desideri.

Per ulteriori informazioni, vedere il campo ratingSummaryEnabled per l&#39;oggetto convConfig Reviews .

## Filtro per spam e profanazione {#section_hcm_jnh_21b}

Il testo del Titolo e del Corpo di una recensione viene trasmesso attraverso il nostro Filtro Spam e il Filtro Profanity non appena la Revisione viene pubblicata.

## Personalizzazione del testo {#section_tjf_hnh_21b}

Le stringhe di testo, comprese descrizioni ed etichette, possono essere personalizzate per la lingua o per adattarle al marchio.

## Risposta a una recensione {#section_yng_fnh_21b}

Gli utenti possono rispondere alla propria revisione o a una revisione in ciascuna raccolta di revisioni. Solo gli utenti che hanno effettuato l’accesso possono inviare una risposta a una revisione.

L&#39;opzione per gli utenti di rispondere a una revisione è abilitata in Studio. I proprietari possono attivare/disattivare questa impostazione per il livello Rete, Sito o Raccolta. I moderatori possono abilitare questa impostazione solo per le rispettive raccolte.

## SocialSync e cura {#section_llh_2nh_21b}

Poiché Revisioni è progettato per aggiungere un valore numerico per ogni elemento di contenuto inviato, SocialSync e Curate non sono supportati con le Revisioni.

## API di revisione {#section_xrh_wmh_21b}

Le API di revisione sono disponibili per consentire di visualizzare informazioni di valutazione e valutazione media degli utenti e l’attività di revisione degli utenti su altre sezioni del sito.

[Valutazioni e recensioni](https://api.livefyre.com/docs/apis/by-category/ratings-and-reviews)

* **[!UICONTROL Bootstrap API Endpoint]** L&#39;endpoint API Bootstrap consente alla revisione di essere letto da motori di ricerca come Google in modo che il contenuto e le parole chiave possano migliorare l&#39;ottimizzazione del motore di ricerca.

* **[!UICONTROL Average User Ratings]** L&#39;API delle valutazioni medie degli utenti recupera la valutazione media degli utenti per una o più raccolte di revisioni, consentendo di creare una visualizzazione di queste informazioni su una pagina di indice o di aggiungerle a una pagina di indice di ricerca.

* **[!UICONTROL Ratings Breakdown]** L’API di suddivisione delle valutazioni recupera un raggruppamento di tutte le valutazioni per una raccolta di revisioni specifica e ti consente di creare una visualizzazione che mostra il numero di revisioni associate a ogni valutazione a stella.

* **[!UICONTROL User Reviews]** L&#39;API User Reviews recupera le revisioni più recenti per un utente specifico. Questa attività può essere utilizzata per visualizzare le revisioni di un utente sulla sua pagina del profilo pubblico.
