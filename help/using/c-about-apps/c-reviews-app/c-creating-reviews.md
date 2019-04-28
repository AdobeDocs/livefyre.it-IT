---
description: Le revisioni offrono un'ampia gamma di personalizzazioni, consentendo di creare un'app di revisione che corrisponda alle tue esigenze e al tuo marchio.
seo-description: Le revisioni offrono un'ampia gamma di personalizzazioni, consentendo di creare un'app di revisione che corrisponda alle tue esigenze e al tuo marchio.
seo-title: Creazione di un'app Recensioni
solution: Experience Manager
title: Creazione di un'app Recensioni
uuid: 6 caeafe 7-c 04 e -484 e-b 02 f -98 dc 6 d 9 b 3184
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Creazione di un&#39;app Recensioni{#creating-a-reviews-app}

Le revisioni offrono un&#39;ampia gamma di personalizzazioni, consentendo di creare un&#39;app di revisione che corrisponda alle tue esigenze e al tuo marchio.

Utilizzate l&#39;app Recensioni per incorporarla personalizzata sul sito come applicazione JS. Non è possibile creare un&#39;app Reviews in Livefyre Studio. Per creare un&#39;app Recensioni sul sito, vedi [Integrazione revisioni](/help/implementation/c-app-integrations/c-reviews-integration.md).


## Valutazioni {#section_hs5_c4h_21b}

Le valutazioni rappresentano il valore numerico assegnato dagli utenti alla revisione. Ogni revisione deve includere una valutazione, visualizzata come sistema a 5 stelle per impostazione predefinita. (Mentre le valutazioni sono visualizzate come 0.5 - 5 nell&#39;app, Livefyre memorizza il rapporto tra X/100 nel backend, in modo che 1 stella sia 20/100 e 2 stelle sia 40/100. Questo rapporto viene visualizzato quando visualizzate le revisioni in Studio.

La scala di valutazione da 0.5 a 5 può essere configurata fino a un massimo di 100, con le nuove valutazioni disponibili.

Per ulteriori informazioni, vedi il campo maxvalutazione per l&#39;oggetto Reviews convconfig.

## Attribuzione stile icona valutazione {#section_cqn_c4h_21b}

Le icone di valutazione possono essere personalizzate in base al marchio e allo stile.

Per ulteriori informazioni, consulta **[!UICONTROL Configure Star Ratings]** la sezione Personalizzazione revisioni.

## Dimensioni di valutazione {#section_cnx_snh_21b}

Le dimensioni di valutazione corrispondono alle categorie su cui i revisori pubblicano il prodotto o il servizio. Esempi di dimensioni di valutazione sono «performance», «design», «cost», «total» o qualsiasi altra categoria scelta.

L&#39;impostazione predefinita consiste nell&#39;visualizzare una dimensione di valutazione «globale», ma è possibile definire e implementare più dimensioni di valutazione, come illustrato nell&#39;esempio di seguito.

Per ulteriori informazioni, consultate il campo ratingdimensions in Revisione metadati raccolta.

## Rivedi campi di testo {#section_xcm_4nh_21b}

Potete anche includere altri campi di testo sul prodotto o sull&#39;esperienza in corso di revisione. Ad esempio, i campi di testo possono includere Pros and Cons, oppure Don&#39;t Miss. Il testo, il titolo e il testo predefinito per il campo sono personalizzabili. Per pubblicare la revisione, gli utenti dovranno completare tutti i campi di testo, nonché il titolo, il corpo e la valutazione della revisione. Non è possibile includere campi di testo facoltativi.

Per ulteriori informazioni, consultate il campo ratingdimensions per i metadati della raccolta.

## Riepilogo recensioni {#section_ysz_lnh_21b}

Per impostazione predefinita, nella parte superiore dell&#39;app recensioni viene visualizzata una sezione di riepilogo. Questa sezione include una visualizzazione della valutazione media utente e della suddivisione valutazione per la raccolta recensioni, che mostra solo i numeri interi. Questa sezione è di sola lettura e può essere nascosta se lo desiderate.

Per ulteriori informazioni, consultate il campo ratingsunyenabled per l&#39;oggetto Reviews convconfig.

## Filtro Spam e Profasity {#section_hcm_jnh_21b}

Il testo del Titolo e del corpo di una revisione viene trasmesso attraverso il filtro Spam e filtro profetico non appena viene pubblicata la revisione.

## Personalizzazione testo {#section_tjf_hnh_21b}

Le stringhe di testo, incluse le descrizioni e le etichette dei comandi, possono essere personalizzate per la lingua o adattate al marchio.

## Risposta a una revisione {#section_yng_fnh_21b}

Gli utenti possono rispondere a loro o all&#39;opzione Revisione in ogni raccolta recensione. Solo gli utenti connessi possono pubblicare una risposta a una revisione.

L&#39;opzione per consentire agli utenti di rispondere a una revisione è abilitata in Studio. I proprietari possono attivare o disattivare questa impostazione per il livello Rete, Sito o Raccolta. I moderatori possono abilitare questa impostazione solo per le proprie raccolte.

## Socialsync e Curate {#section_llh_2nh_21b}

Poiché le revisioni sono progettate per aggiungere un valore numerico per ogni contenuto inviato, socialsync e Curate non sono supportati con le recensioni.

## API recis {#section_xrh_wmh_21b}

Le API recensioni sono disponibili per visualizzare la valutazione media degli utenti e le informazioni sulla suddivisione delle valutazioni e l&#39;attività di revisione delle revisioni su altre sezioni del sito.

[Valutazioni e recensioni](https://api.livefyre.com/docs/apis/by-category/ratings-and-reviews)

* **[!UICONTROL Bootstrap API Endpoint]** L&#39;endpoint API di Bootstrap consente la lettura della revisione tramite motori di ricerca come Google, in modo che il contenuto e le parole chiave possano migliorare l&#39;ottimizzazione dei motori di ricerca.

* **[!UICONTROL Average User Ratings]** L&#39;API Media Valutazioni recupera la valutazione media dell&#39;utente per una o più raccolte recensioni, consentendo di creare una visualizzazione di tali informazioni in una pagina indice o di aggiungere a una pagina indice di ricerca.

* **[!UICONTROL Ratings Breakdown]** L&#39;API Analisi valutazioni recupera una suddivisione di tutte le valutazioni per una raccolta recensioni specifica e consente di creare una visualizzazione che mostra il numero di revisioni associate a ogni valutazione a stella.

* **[!UICONTROL User Reviews]** L&#39;API Recensioni utente recupera le revisioni più recenti per un utente specifico. Questa attività può essere utilizzata per visualizzare le revisioni di un utente sulla pagina del profilo pubblico.
