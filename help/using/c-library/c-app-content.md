---
description: Gestione del contenuto nella rete Livefyre.
seo-description: Gestione del contenuto nella rete Livefyre.
seo-title: Scheda Contenuto app
solution: Experience Manager
title: Scheda Contenuto app
uuid: 65b23085-2b79-4a6f-96c9-44b421805312
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Scheda Contenuto app{#app-content-tab}

Gestione del contenuto nella rete Livefyre.

La scheda Contenuto app nella libreria consente di cercare e moderare il contenuto pubblicato nelle app. La **[!UICONTROL App Content]** scheda consente diversi filtri di ricerca con carattere jolly, per definire in modo più rapido e semplice i parametri di ricerca.

Utilizzate la scheda Contenuto app per:

* Cerca contenuto
* Visualizza cronologia contenuto
* Contenuto moderato
* Aggiungere un tag
* Feature Content
* Associate Content with Products from the Product Catalog (Associazione di contenuti con prodotti dal catalogo prodotti)

Per ulteriori informazioni su come moderare il contenuto mediante la scheda Contenuto app, vedete [](../c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md#c_moderate_content_using_app_content).

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

Utilizzate il **[!UICONTROL Quick Filters]** pulldown per limitare il contenuto restituito a **[!UICONTROL All Content]**, **[!UICONTROL All Sidenotes]**, **[!UICONTROL Approved]**, **[!UICONTROL Approved & Flagged]**, **[!UICONTROL Pending]** o **[!UICONTROL Rights Requests]** stato. Selezionate quindi un’ **[!UICONTROL Filter by]** opzione e utilizzate le caselle di controllo o i campi di input disponibili per limitare la ricerca.

Utilizzate il menu a discesa per ordinare il contenuto dell'elenco per **[!UICONTROL Newest]**, **[!UICONTROL Oldest]**, **[!UICONTROL Recently updated]**, **[!UICONTROL Most flags]** o **[!UICONTROL Most liked]**.

## Filtra per opzioni {#section_aqn_xqm_zz}

Utilizzate la **[!UICONTROL Filter by]** barra per filtrare in base alle seguenti opzioni:

* **Stato** Consente di filtrare in base allo stato corrente di moderazione del contenuto:** [!UICONTROL All Content]**, **[!UICONTROL Approved]**, **[!UICONTROL Pending]** o **[!UICONTROL Bozo]**.

* **Origine** Consente di filtrare in base all'origine del contenuto. Selezionate **[!UICONTROL Livefyre]** per elencare il contenuto generato dall'utente pubblicato direttamente nel flusso. Seleziona **[!UICONTROL Facebook]**, **[!UICONTROL Twitter]** o **[!UICONTROL RSS]** per includere il contenuto estratto nelle app da tali origini.

* **Flag** La selezione di contrassegni consente di filtrare per **[!UICONTROL User Flags]** (Spam, Off-topic, Offensive o Non d'accordo), **[!UICONTROL System Flags]** applicato da SAFE (Profanity, Spam, o Magicamente Moderato), o **[!UICONTROL Moderation Recommendations]**. ![](assets/appcontentfilter.png)

* **Data/ora** Consente di impostare il momento in cui il contenuto è stato originariamente **[!UICONTROL Created]** (o inserito nell'app tramite SocialSync o un flusso) oppure l'ultimo **[!UICONTROL Modified]** (modificato, contrassegnato o modificato dallo stato).

* **Autore** Consente di filtrare in base all’ **[!UICONTROL IP]** indirizzo dell’autore, **[!UICONTROL Display Name]** (nel pannello Utenti o sopra il contenuto pubblicato dall’autore) o **[!UICONTROL User ID]**(nel pannello Utenti).

* **Contiene** Consente di filtrare il contenuto più recente per **[!UICONTROL Keyword]** o **[!UICONTROL Content Tag]**. Selezionate la **[!UICONTROL Media]** casella di controllo per restituire solo il contenuto che contiene file multimediali. Per cercare tutto il contenuto, scorrete verso il basso tutto il contenuto dell’elenco, quindi fate clic **[!UICONTROL Search full data]**.

   **** Nota: La ricerca di più parole chiave e tag di contenuto non è supportata. Se vengono inseriti più parole chiave o tag, per la ricerca verrà utilizzata l’ultima parola.

   Durante la ricerca per Tag contenuto, i tag suggeriti verranno popolati automaticamente mentre digitate nel campo di ricerca. I risultati della ricerca restituiranno tutto il contenuto a cui è stato assegnato il tag. (Utilizzate questo campo per cercare il contenuto in primo piano, oppure fate clic sull' **[!UICONTROL Featured]** etichetta per qualsiasi contenuto disponibile in Studio.)

   **** Nota: Usate un segno meno (-) prima del nome di un tag per cercare il contenuto che non include tale tag. Ad esempio: Cercate ‘-Miley’ per cercare tutto il contenuto che non include il tag ‘Miley’.

* **App** Consente di filtrare per **[!UICONTROL Collection ID]**, **[!UICONTROL App Tag]** o ID **** principale. Il filtraggio per ID padre restituisce tutto il contenuto che rappresenta una risposta all'ID contenuto di input. (Filtrare per più tag immettendo i tag separati da virgola).

* **Diritti** Consente di filtrare in base allo stato Richieste di diritti:** [!UICONTROL Requested]**, **[!UICONTROL Granted]**, **[!UICONTROL Replied]** o **[!UICONTROL Expired]**.

## Contenuto Bozo {#section_afl_vqm_zz}

Nelle app, **[!UICONTROL Bozo]** il contenuto viene visualizzato solo all'autore del contenuto. Questo consente all'utente di credere che il contenuto sia stato approvato e di nasconderlo a tutti gli altri utenti e moderatori.

>[!NOTE]
>
>I contenuti social generati da SocialSync o Streams **[!UICONTROL cannot]** devono essere impostati su Bozo.

Potete creare contenuti Bozo per i seguenti motivi:

* Il contenuto identificato come Spam by SAFE viene automaticamente impostato sullo stato Bozo.
* Tutto il contenuto di Utenti vietati viene automaticamente impostato su Bozo.
* Il contenuto può essere contrassegnato come Bozo da Studio.
* I moderatori possono creare contenuti Bozo direttamente nel flusso.

## Visualizza cronologia contenuto {#section_ayz_tqm_zz}

Il pannello dei contenuti consente di esaminare la cronologia di tutti i contenuti elencati, inclusi la premoderazione, il filtro per gli spam, la data di pubblicazione e tutti i flag utente o le note assegnate all’elemento.

Utilizzate le schede nella parte inferiore del pannello dei contenuti per visualizzarne la cronologia.

* **[!UICONTROL More Info:]** elenca tutte le attività su questo contenuto, inclusi invio, modifica, controllo dello spam, modifica dello stato e note. In questa sezione vengono visualizzati anche l'ID contenuto Livefyre e l'indirizzo IP dell'utente.
* **[!UICONTROL Replies:]** elenca un massimo di 6 risposte. Fare clic **[!UICONTROL Show all replies]** per visualizzare tutte le risposte al post.

* **[!UICONTROL Flags & Reports:]** elenca tutti i flag utente, con l’avatar dell’utente che ha segnalato il contenuto, e tutti i report (note aggiunte dall’utente durante l’applicazione dei tag al contenuto).
* **[!UICONTROL Add a note:]** consente di aggiungere una nota visibile ad altri amministratori o moderatori.
* **[!UICONTROL Request Rights:]** apre la **[!UICONTROL New Rights Request]** finestra di dialogo da cui può essere rilasciata una richiesta di diritti.

* **[!UICONTROL Save as Asset:]**apre la **[!UICONTROL Advanced Options]** finestra di dialogo che consente di salvare l'elemento selezionato nella Libreria risorse, pubblicarlo in un'app o richiedere diritti di riutilizzo all'autore.

![](assets/PublishedMoreInfo-1024x462.png)

## Aggiungere un tag al contenuto {#section_xb4_mxr_rdb}

I contenuti con tag consentono di classificare e organizzare i contenuti per semplificarne il recupero e la personalizzazione degli stili, oppure di contrassegnare i contenuti come descritti in precedenza.

Per aggiungere tag, fai clic sull’icona più ( **[!UICONTROL +]**) sotto il contenuto. Inserite un nuovo tag oppure selezionatelo da un elenco di tag esistenti.

![](assets/PublishedAddTag-1024x338.png)

## Ricerca di immagini in tutte le risorse {#section_zxf_hsf_wcb}

Dopo aver aggiunto il contenuto alla libreria, è possibile eseguire ricerche nei contenuti tramite smart tag.

Nella libreria, in Tutte le risorse, puoi cercare immagini esistenti facendo clic su **[!UICONTROL Show Filters]** e quindi:

* Immissione del testo da cercare nel campo di ricerca
* Ordinamento in base alla pertinenza
* Immissione di testo nel **[!UICONTROL Tags]** campo per la ricerca in base ai tag avanzati. L’algoritmo di classificazione dei tag avanzati filtra il contenuto utilizzando una valutazione di attendibilità basata su smart tag, la novità del contenuto e il numero di stelle che un utente ha assegnato al contenuto.

## Contenuto in evidenza {#section_emb_kqm_zz}

Selezionate il **[!UICONTROL Featured]** tag predefinito per contrassegnare il contenuto come disponibile ed evidenziatelo come importante per gli utenti. Una volta assegnati i tag, utilizzate le opzioni di stile personalizzate per personalizzare il contenuto presente nelle app.

## Per Feature o annullare la funzionalità del contenuto {#section_ojx_3qm_zz}

* Da Studio, fate clic sul **[!UICONTROL +]** segno accanto a una parte del contenuto, selezionate il **[!UICONTROL Featured]** tag nell'elenco a discesa, quindi fate clic **[!UICONTROL Enter]** sul contenuto Feature. Il tag viene salvato e visualizzato accanto al contenuto.

* Per annullare la funzione, fate clic sul **[!UICONTROL x]** tag visualizzato sul **[!UICONTROL Featured]** tag del contenuto.

* Dall'interno di un'app Commenti, Blog dal vivo o Recensioni, passa il mouse sul contenuto che desideri presentare e fai clic **[!UICONTROL Feature]**. Per annullare la funzione, passate il mouse sul contenuto e fate clic **[!UICONTROL Unfeature]**.

>[!NOTE]
>
>A causa di vincoli di spazio, il contenuto della chat potrebbe essere disponibile solo in Studio o non disponibile, e potrebbe non essere disponibile dall'interno dell'app stessa.

## Modifica del contenuto {#section_pyw_hqm_zz}

La maggior parte delle azioni regolari sul contenuto può essere eseguita sul contenuto in evidenza, fatta eccezione per quanto segue:

* Il contenuto in evidenza non può essere contrassegnato.
* Gli utenti non possono modificare il contenuto dopo che è stato presentato, anche se possono comunque eliminarlo se lo desiderano. I moderatori possono modificare il contenuto disponibile.

