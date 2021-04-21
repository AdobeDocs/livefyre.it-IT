---
description: Gestione dei contenuti nella rete Livefyre.
title: Scheda Contenuto app
exl-id: 8b3e5281-59ba-4321-8fee-4160ab7a5d5e
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '1109'
ht-degree: 0%

---

# Scheda Contenuto app{#app-content-tab}

Gestione dei contenuti nella rete Livefyre.

La scheda Contenuto app nella libreria ti consente di cercare e moderare il contenuto pubblicato nelle app. La scheda **[!UICONTROL App Content]** abilita diversi filtri di ricerca con ricerca con caratteri jolly, per consentirti di definire i parametri di ricerca in modo più rapido e semplice.

Utilizza la scheda Contenuto app per:

* Ricerca di contenuti
* Visualizza cronologia dei contenuti
* Contenuto moderato
* Aggiungi un tag
* Contenuto della funzione
* Associa contenuto ai prodotti del catalogo prodotti

Per ulteriori informazioni su come moderare il contenuto utilizzando la scheda Contenuto app, consulta [](../c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md#c_moderate_content_using_app_content).

## Ricerca con caratteri jolly {#section_jvr_ntm_zz}

I campi di ricerca Livefyre supportano i caratteri jolly, che consentono di aggiungere un asterisco ( * ) alle parole (o frammenti di parole) per rilevare le corrispondenze parziali.

Ad esempio:

* la palla restituisce solo la palla
* palla* restituisce pallone e pallone
* *la palla restituisce la palla e il calcio
* *la palla* restituisce la sfera e l&#39;uniball e la snowballato

## Cerca contenuto {#section_fw1_mtm_zz}

Il pannello Contenuto app consente di restringere la ricerca utilizzando diverse opzioni di filtro del contenuto.

![](assets/PublishedState-1024x367.png)

Utilizza il menu a discesa **[!UICONTROL Quick Filters]** per limitare il contenuto restituito allo stato **[!UICONTROL All Content]**, **[!UICONTROL All Sidenotes]**, **[!UICONTROL Approved]**, **[!UICONTROL Approved & Flagged]**, **[!UICONTROL Pending]** o **[!UICONTROL Rights Requests]**. Quindi seleziona un’opzione **[!UICONTROL Filter by]** e utilizza le caselle di controllo o i campi di input disponibili per limitare la ricerca.

Utilizza il menu a discesa per ordinare il contenuto dell’elenco in base a **[!UICONTROL Newest]**, **[!UICONTROL Oldest]**, **[!UICONTROL Recently updated]**, **[!UICONTROL Most flags]** o **[!UICONTROL Most liked]**.

## Filtra per opzioni {#section_aqn_xqm_zz}

Utilizza la barra **[!UICONTROL Filter by]** per filtrare in base alle seguenti opzioni:

* **** StatoConsente di filtrare in base allo stato di moderazione corrente del contenuto:**  [!UICONTROL All Content]**,  **[!UICONTROL Approved]**,  **[!UICONTROL Pending]**, o  **[!UICONTROL Bozo]**.

* **** OrigineConsente di filtrare in base all’origine del contenuto. Seleziona **[!UICONTROL Livefyre]** per elencare i contenuti generati dall’utente pubblicati direttamente nel flusso. Seleziona **[!UICONTROL Facebook]**, **[!UICONTROL Twitter]** o **[!UICONTROL RSS]** per includere il contenuto estratto nelle app da tali origini.

* **** FlagLa selezione dei flag consente di filtrare per  **[!UICONTROL User Flags]** (Spam, Off-topic, Offensive o in disaccordo),  **[!UICONTROL System Flags]** applicato da SAFE (Profanity, Spam o Magically Moderated), o  **[!UICONTROL Moderation Recommendations]**.  ![](assets/appcontentfilter.png)

* **Data/** oraConsente di adattarsi in base a quando il contenuto è stato originariamente  **[!UICONTROL Created]** (o inserito nell’app tramite SocialSync o un Stream) o per ultimo  **[!UICONTROL Modified]** (modificato, contrassegnato o modificato lo stato).

* **** AutoreConsente di filtrare in base all’ **[!UICONTROL IP]** indirizzo dell’autore,  **[!UICONTROL Display Name]** (nel pannello Utenti o da sopra il contenuto pubblicato dall’autore) o  **[!UICONTROL User ID]**(nel pannello Utenti).

* **** ContainsConsente di filtrare i contenuti degli ultimi 90 giorni per  **[!UICONTROL Keyword]** o  **[!UICONTROL Content Tag]**. Seleziona la casella di controllo **[!UICONTROL Media]** per restituire solo il contenuto contenente Media. (Per cercare tutto il contenuto, scorri verso il basso tra tutti i contenuti dell’elenco, quindi fai clic su **[!UICONTROL Search full data]**.)

   **Nota:** la ricerca di più parole chiave e tag di contenuto non è supportata. Se vengono inseriti più parole chiave o tag, l’ultima parola verrà utilizzata per la ricerca.

   Durante la ricerca per Tag contenuto, i tag suggeriti verranno compilati automaticamente mentre digiti nel campo di ricerca. I risultati della ricerca restituiranno tutto il contenuto a cui è stato assegnato il tag . (Usa questo campo per cercare il contenuto in primo piano, oppure fai clic sull’etichetta **[!UICONTROL Featured]** su qualsiasi contenuto disponibile in Studio.)

   **Nota:** utilizzate un segno meno (-) prima del nome di un tag per cercare contenuto che non includa quel tag. Ad esempio: Cerca &quot;-Miley&quot; per cercare tutti i contenuti che non includono il tag &quot;Miley&quot;.

* **** AppConsente di filtrare per  **[!UICONTROL Collection ID]**,  **[!UICONTROL App Tag]** o ID  **padre**. L’applicazione di filtri per ID padre restituisce tutti i contenuti che rappresentano una risposta all’ID contenuto di input. Per filtrare in base a più tag, immetti i tag separati da una virgola.

* **** DirittiConsente di filtrare in base allo stato delle richieste di diritti:**  [!UICONTROL Requested]*,  **[!UICONTROL Granted]**,  **[!UICONTROL Replied]** o  **[!UICONTROL Expired]**.

## Contenuto Bozo {#section_afl_vqm_zz}

Nelle app, il contenuto **[!UICONTROL Bozo]** viene visualizzato solo per l’autore del contenuto. Questo consente all’utente di credere che il proprio contenuto sia stato approvato, nascondendolo dagli altri utenti e moderatori.

>[!NOTE]
>
>I contenuti social provenienti da SocialSync o Streams **[!UICONTROL cannot]** devono essere impostati su Bozo.

Puoi creare contenuti Bozo per i seguenti motivi:

* Il contenuto identificato come Spam da SAFE viene automaticamente impostato sullo stato Bozo.
* Tutti i contenuti di Utenti banditi vengono automaticamente impostati su Bozo.
* Il contenuto può essere contrassegnato come Bozo da Studio.
* I moderatori possono creare contenuti Bozo direttamente nel flusso.

## Visualizza cronologia contenuto {#section_ayz_tqm_zz}

Il pannello dei contenuti ti consente di esaminare la cronologia di tutti i contenuti elencati, inclusi la moderazione, il filtraggio dello spam, la data del post e tutti i flag o le note utente assegnati all’elemento.

Utilizza le schede nella parte inferiore del pannello dei contenuti per visualizzarne la cronologia.

* **[!UICONTROL More Info:]** elenca tutte le attività relative a questo contenuto, inclusi l’invio, la modifica, il controllo dello spam, la modifica dello stato e le note. Anche l’ID del contenuto Livefyre e l’indirizzo IP dell’utente vengono visualizzati in questa sezione.
* **[!UICONTROL Replies:]** elenca un massimo di 6 risposte. Fai clic su **[!UICONTROL Show all replies]** per visualizzare tutte le risposte al post.

* **[!UICONTROL Flags & Reports:]** elenca tutti i flag utente, con l’avatar dell’utente che ha segnalato il contenuto e tutti i report (note aggiunte dall’utente durante l’aggiunta di un flag al contenuto).
* **[!UICONTROL Add a note:]** consente di aggiungere una nota visibile ad altri amministratori o moderatori.
* **[!UICONTROL Request Rights:]** apre la  **[!UICONTROL New Rights Request]** finestra di dialogo da cui può essere emessa una richiesta di diritti.

* **[!UICONTROL Save as Asset:]**apre la finestra di dialogo **[!UICONTROL Advanced Options]**, che consente di salvare l’elemento selezionato nella Libreria risorse, di pubblicarlo in un’app o di richiedere i diritti di riutilizzo all’autore.

![](assets/PublishedMoreInfo-1024x462.png)

## Aggiungi un tag al contenuto {#section_xb4_mxr_rdb}

L’assegnazione tag ai contenuti consente di organizzare e classificare i contenuti per facilitarne il recupero e la personalizzazione degli stili, oppure di contrassegnare i contenuti come descritto.

Per aggiungere tag, fai clic sull’icona più ( **[!UICONTROL +]**) sotto il contenuto. Inserisci un nuovo tag o selezionalo da un elenco di tag esistenti.

![](assets/PublishedAddTag-1024x338.png)

## Ricerca di immagini in tutte le risorse {#section_zxf_hsf_wcb}

Dopo aver aggiunto il contenuto alla libreria, puoi eseguire ricerche nel contenuto mediante tag avanzati.

Nella sezione Library (Tutte le risorse), puoi cercare le immagini esistenti facendo clic su **[!UICONTROL Show Filters]** e quindi:

* Inserimento di testo da cercare nel campo di ricerca
* Ordinamento in base alla pertinenza
* Inserimento di testo nel campo **[!UICONTROL Tags]** per eseguire ricerche per tag avanzati. L’algoritmo di classificazione dei tag avanzati filtra il contenuto utilizzando un punteggio di affidabilità per tag avanzati, la novità del contenuto e quante stelle un utente ha dato il contenuto.

## Contenuto in primo piano {#section_emb_kqm_zz}

Seleziona il tag **[!UICONTROL Featured]** predefinito per contrassegnare il contenuto come presentato ed evidenzialo come importante per i tuoi utenti. Una volta assegnati i tag, utilizza le opzioni di stile personalizzate per personalizzare il contenuto in primo piano nelle app.

## Per Feature o annullare la funzione del contenuto {#section_ojx_3qm_zz}

* In Studio, fai clic sul segno **[!UICONTROL +]** accanto a un contenuto, seleziona il tag **[!UICONTROL Featured]** nell’elenco a discesa e fai clic su **[!UICONTROL Enter]** per creare il contenuto della funzione. Il tag viene salvato e visualizzato accanto al contenuto.

* Per annullare la funzione, fai clic su **[!UICONTROL x]** nel tag **[!UICONTROL Featured]** visualizzato sul contenuto.

* Dall’interno di un’app Commenti, Blog live o Recensioni , passa il puntatore del mouse sul contenuto che desideri visualizzare e fai clic su **[!UICONTROL Feature]**. Per annullare la funzione, passa il mouse sul contenuto e fai clic su **[!UICONTROL Unfeature]**.

>[!NOTE]
>
>A causa di vincoli di spazio, il contenuto della chat può essere disponibile solo in studio o non essere disponibile utilizzando Studio e potrebbe non essere disponibile dall&#39;interno dell&#39;app stessa.

## Modifica del contenuto in primo piano {#section_pyw_hqm_zz}

La maggior parte delle azioni regolari sui contenuti possono essere eseguite sui contenuti in primo piano, ad eccezione dei seguenti:

* Il contenuto in primo piano non può essere contrassegnato.
* Gli utenti non possono modificare il proprio contenuto dopo che è stato pubblicato, anche se possono comunque eliminarlo se lo desiderano. I moderatori possono modificare il contenuto in primo piano.
