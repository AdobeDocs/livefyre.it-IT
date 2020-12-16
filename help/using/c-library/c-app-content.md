---
description: Gestione del contenuto nella rete Livefyre.
seo-description: Gestione del contenuto nella rete Livefyre.
seo-title: Scheda Contenuto app
solution: Experience Manager
title: Scheda Contenuto app
uuid: 65b23085-2b79-4a6f-96c9-44b421805312
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869
workflow-type: tm+mt
source-wordcount: '1118'
ht-degree: 0%

---


# Scheda Contenuto app{#app-content-tab}

Gestione del contenuto nella rete Livefyre.

La scheda Contenuto app nella libreria consente di cercare e moderare il contenuto pubblicato nelle app. La scheda **[!UICONTROL App Content]** consente di utilizzare diversi filtri di ricerca con caratteri jolly per definire in modo più rapido e semplice i parametri di ricerca.

Utilizzate la scheda Contenuto app per:

* Cerca contenuto
* Visualizza cronologia contenuto
* Contenuto moderato
* Aggiungere un tag
* Feature Content
* Associate Content with Products from the Product Catalog (Associazione di contenuti con prodotti dal catalogo prodotti)

Per ulteriori informazioni su come moderare il contenuto mediante la scheda Contenuto app, consultate [](../c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md#c_moderate_content_using_app_content).

## Ricerca con caratteri jolly {#section_jvr_ntm_zz}

I campi di ricerca Livefyre supportano i caratteri jolly, che consentono di aggiungere un asterisco ( * ) alle parole (o frammenti di parole) per rilevare corrispondenze parziali.

Ad esempio:

* la palla restituisce solo la palla
* ball* restituisce pallone e pallone
* *la palla restituisce la palla e il calcio
* *palla* restituisce sfere e uniball e snowballed

## Cerca contenuto {#section_fw1_mtm_zz}

Il pannello Contenuto app consente di limitare la ricerca utilizzando diverse opzioni di filtro del contenuto.

![](assets/PublishedState-1024x367.png)

Utilizzate il pulldown **[!UICONTROL Quick Filters]** per restringere il contenuto restituito allo stato **[!UICONTROL All Content]**, **[!UICONTROL All Sidenotes]**, **[!UICONTROL Approved]**, **[!UICONTROL Approved & Flagged]**, **[!UICONTROL Pending]** o **[!UICONTROL Rights Requests]**. Selezionate quindi un&#39;opzione **[!UICONTROL Filter by]** e utilizzate le caselle di controllo o i campi di input disponibili per limitare la ricerca.

Utilizzate il menu a discesa per ordinare il contenuto dell&#39;elenco in base a **[!UICONTROL Newest]**, **[!UICONTROL Oldest]**, **[!UICONTROL Recently updated]**, **[!UICONTROL Most flags]** o **[!UICONTROL Most liked]**.

## Filtrare per opzioni {#section_aqn_xqm_zz}

Utilizzate la barra **[!UICONTROL Filter by]** per filtrare in base alle seguenti opzioni:

* **** Stato: consente di filtrare in base allo stato corrente di moderazione del contenuto:**  [!UICONTROL All Content]**,  **[!UICONTROL Approved]**,  **[!UICONTROL Pending]** o  **[!UICONTROL Bozo]**.

* **** Origine: consente di filtrare in base all’origine del contenuto. Selezionare **[!UICONTROL Livefyre]** per elencare il contenuto generato dall&#39;utente pubblicato direttamente nel flusso. Selezionare **[!UICONTROL Facebook]**, **[!UICONTROL Twitter]** o **[!UICONTROL RSS]** per includere il contenuto estratto nelle app da tali origini.

* **** ContrassegniLa selezione di contrassegni consente di filtrare per  **[!UICONTROL User Flags]** (Spam, Off-topic, Offensive o Non d&#39;accordo),  **[!UICONTROL System Flags]** applicato da SAFE (Profanity, Spam, o Magicamente Moderato), o  **[!UICONTROL Moderation Recommendations]**.  ![](assets/appcontentfilter.png)

* **Data/** ora: consente di adattarsi in base a quando il contenuto è stato originariamente  **[!UICONTROL Created]** (o inserito nell&#39;app tramite SocialSync o un flusso), oppure per ultimo  **[!UICONTROL Modified]** (modificato, contrassegnato o modificato dallo stato).

* **** Autore: consente di filtrare in base all’ **[!UICONTROL IP]** indirizzo dell’autore,  **[!UICONTROL Display Name]** (nel pannello Utenti o sopra il contenuto pubblicato dall’autore) o  **[!UICONTROL User ID]**(nel pannello Utenti).

* **** Contiene: consente di filtrare gli ultimi 90 giorni di contenuto per  **[!UICONTROL Keyword]** o  **[!UICONTROL Content Tag]**. Selezionate la casella di controllo **[!UICONTROL Media]** per restituire solo il contenuto che contiene file multimediali. Per cercare tutto il contenuto, scorrete verso il basso tutto il contenuto dell&#39;elenco, quindi fate clic su **[!UICONTROL Search full data]**.

   **Nota: la ricerca di** più parole chiave e tag di contenuto non è supportata. Se vengono inseriti più parole chiave o tag, per la ricerca verrà utilizzata l’ultima parola.

   Durante la ricerca per Tag contenuto, i tag suggeriti verranno popolati automaticamente mentre digitate nel campo di ricerca. I risultati della ricerca restituiranno tutto il contenuto a cui è stato assegnato il tag. (Utilizzate questo campo per cercare il contenuto in primo piano, oppure fate clic sull&#39;etichetta **[!UICONTROL Featured]** per qualsiasi contenuto disponibile in Studio.)

   **Nota:** usate un segno meno (-) prima del nome di un tag per cercare il contenuto che non include tale tag. Ad esempio: Cercate ‘-Miley’ per cercare tutto il contenuto che non include il tag ‘Miley’.

* **** App: consente di filtrare per  **[!UICONTROL Collection ID]**,  **[!UICONTROL App Tag]** o ID **** principale. Il filtraggio per ID padre restituisce tutto il contenuto che rappresenta una risposta all&#39;ID contenuto di input. (Filtrare per più tag immettendo i tag separati da una virgola).

* **** Diritti: consente di filtrare in base allo stato delle richieste di diritti:**  [!UICONTROL Requested]**,  **[!UICONTROL Granted]**,  **[!UICONTROL Replied]** o  **[!UICONTROL Expired]**.

## Contenuto Bozo {#section_afl_vqm_zz}

Nelle app, il contenuto **[!UICONTROL Bozo]** viene visualizzato solo all&#39;autore del contenuto. Questo consente all&#39;utente di credere che il contenuto sia stato approvato e di nasconderlo a tutti gli altri utenti e moderatori.

>[!NOTE]
>
>I contenuti social originati da SocialSync o Streams **[!UICONTROL cannot]** devono essere impostati su Bozo.

Potete creare contenuti Bozo per i seguenti motivi:

* Il contenuto identificato come Spam by SAFE viene automaticamente impostato sullo stato Bozo.
* Tutto il contenuto di Utenti vietati viene automaticamente impostato su Bozo.
* Il contenuto può essere contrassegnato come Bozo da Studio.
* I moderatori possono creare contenuti Bozo direttamente nel flusso.

## Visualizza cronologia contenuto {#section_ayz_tqm_zz}

Il pannello dei contenuti consente di esaminare la cronologia di tutti i contenuti elencati, inclusi la premoderazione, il filtro per gli spam, la data di pubblicazione e tutti i flag utente o le note assegnate all’elemento.

Utilizzate le schede nella parte inferiore del pannello dei contenuti per visualizzarne la cronologia.

* **[!UICONTROL More Info:]** elenca tutte le attività su questo contenuto, inclusi invio, modifica, controllo dello spam, modifica dello stato e note. In questa sezione vengono visualizzati anche l&#39;ID contenuto Livefyre e l&#39;indirizzo IP dell&#39;utente.
* **[!UICONTROL Replies:]** elenca un massimo di 6 risposte. Fare clic su **[!UICONTROL Show all replies]** per visualizzare tutte le risposte al post.

* **[!UICONTROL Flags & Reports:]** elenca tutti i flag utente, con l’avatar dell’utente che ha segnalato il contenuto, e tutti i report (note aggiunte dall’utente durante l’applicazione dei tag al contenuto).
* **[!UICONTROL Add a note:]** consente di aggiungere una nota visibile ad altri amministratori o moderatori.
* **[!UICONTROL Request Rights:]** apre la  **[!UICONTROL New Rights Request]** finestra di dialogo da cui può essere rilasciata una richiesta di diritti.

* **[!UICONTROL Save as Asset:]**apre la finestra di dialogo **[!UICONTROL Advanced Options]**, che consente di salvare l&#39;elemento selezionato nella Libreria risorse, pubblicarlo in un&#39;app o richiedere diritti di riutilizzo all&#39;autore.

![](assets/PublishedMoreInfo-1024x462.png)

## Aggiungere un tag al contenuto {#section_xb4_mxr_rdb}

I contenuti con tag consentono di classificare e organizzare i contenuti per semplificarne il recupero e la personalizzazione degli stili, oppure di contrassegnare i contenuti come descritti in precedenza.

Per aggiungere tag, fate clic sull&#39;icona più ( **[!UICONTROL +]**) sotto il contenuto. Inserite un nuovo tag oppure selezionatelo da un elenco di tag esistenti.

![](assets/PublishedAddTag-1024x338.png)

## Ricerca di immagini in tutte le risorse {#section_zxf_hsf_wcb}

Dopo aver aggiunto il contenuto alla libreria, è possibile eseguire ricerche nei contenuti tramite smart tag.

Nella libreria, in Tutte le risorse, puoi cercare immagini esistenti facendo clic su **[!UICONTROL Show Filters]** e quindi:

* Immissione del testo da cercare nel campo di ricerca
* Ordinamento in base alla pertinenza
* Immissione di testo nel campo **[!UICONTROL Tags]** per eseguire ricerche in base ai tag avanzati. L’algoritmo di classificazione dei tag avanzati filtra il contenuto utilizzando una valutazione di attendibilità basata su smart tag, la novità del contenuto e il numero di stelle che un utente ha assegnato al contenuto.

## Contenuto in evidenza {#section_emb_kqm_zz}

Selezionate il tag **[!UICONTROL Featured]** predefinito per contrassegnare il contenuto come disponibile ed evidenziatelo come importante per gli utenti. Una volta assegnati i tag, utilizzate le opzioni di stile personalizzate per personalizzare il contenuto presente nelle app.

## Per Feature or Unfeature Content {#section_ojx_3qm_zz}

* Da Studio, fare clic sul segno **[!UICONTROL +]** accanto a una parte del contenuto, selezionare il tag **[!UICONTROL Featured]** nell&#39;elenco a discesa, quindi fare clic su **[!UICONTROL Enter]** per visualizzare il contenuto della funzione. Il tag viene salvato e visualizzato accanto al contenuto.

* Per annullare la funzionalità, fare clic su **[!UICONTROL x]** nel tag **[!UICONTROL Featured]** visualizzato sul contenuto.

* Dall&#39;interno di un&#39;app Commenti, Blog dal vivo o Recensioni, posizionate il puntatore del mouse sul contenuto che desiderate visualizzare e fate clic su **[!UICONTROL Feature]**. Per annullare la funzionalità, è sufficiente passare il mouse sul contenuto e fare clic su **[!UICONTROL Unfeature]**.

>[!NOTE]
>
>A causa di vincoli di spazio, il contenuto della chat potrebbe essere disponibile solo in Studio o non disponibile, e potrebbe non essere disponibile dall&#39;interno dell&#39;app stessa.

## Modifica del contenuto in evidenza {#section_pyw_hqm_zz}

La maggior parte delle azioni regolari sul contenuto può essere eseguita sul contenuto in evidenza, fatta eccezione per quanto segue:

* Il contenuto in evidenza non può essere contrassegnato.
* Gli utenti non possono modificare il contenuto dopo che è stato presentato, anche se possono comunque eliminarlo se lo desiderano. I moderatori possono modificare il contenuto disponibile.

