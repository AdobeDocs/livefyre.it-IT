---
description: Gestione del contenuto nella rete di Livefyre.
seo-description: Gestione del contenuto nella rete di Livefyre.
seo-title: Scheda Contenuto app
solution: Experience Manager
title: Scheda Contenuto app
uuid: 65 b 23085-2 b 79-4 a 6 f -96 c 9-44 b 421805312
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Scheda Contenuto app{#app-content-tab}

Gestione del contenuto nella rete di Livefyre.

La scheda Contenuto app nella libreria consente di cercare e moderare i contenuti pubblicati nelle app. **[!UICONTROL App Content]** La scheda consente di usare più filtri di ricerca con ricerca jolly per definire in modo più rapido e semplice i parametri di ricerca.

Utilizzate la scheda Contenuto app per:

* Ricerca di contenuto
* Visualizza cronologia contenuto
* Modgola contenuto
* Aggiungere un tag
* Contenuto della funzione
* Associare contenuto con prodotti dal Catalogo prodotti

Per ulteriori informazioni su come moderare il contenuto utilizzando la scheda Contenuto app, vedi [](../c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md#c_moderate_content_using_app_content).

## Ricerca con caratteri jolly {#section_jvr_ntm_zz}

I campi di ricerca di Livefyre supportano i caratteri jolly, che consentono di aggiungere un asterisco (*) alle parole (o frammenti di parole) per rilevare corrispondenze parziali.

Ad esempio:

* ball restituisce solo ball
* ball * restituisce palla e pallast
* * ball restituisce palla e football
* * ball * restituisce ball e uniball e snowball

## Ricerca di contenuto {#section_fw1_mtm_zz}

Il pannello Contenuto app consente di limitare la ricerca utilizzando diverse opzioni di filtro del contenuto.

![](assets/PublishedState-1024x367.png)

Usate **[!UICONTROL Quick Filters]** il pulldown per limitare il contenuto restituito a **[!UICONTROL All Content]****[!UICONTROL All Sidenotes]****[!UICONTROL Approved]****[!UICONTROL Approved & Flagged]**, **[!UICONTROL Pending]**o **[!UICONTROL Rights Requests]** allo stato. Quindi selezionate un **[!UICONTROL Filter by]** 'opzione e usate le caselle di controllo o i campi di immissione disponibili per limitare la ricerca.

Utilizzate il menu a discesa per ordinare il contenuto nell'elenco per **[!UICONTROL Newest]****[!UICONTROL Oldest]****[!UICONTROL Recently updated]**, o **[!UICONTROL Most flags]****[!UICONTROL Most liked]**.

## Filtrare per opzioni {#section_aqn_xqm_zz}

Utilizzate **[!UICONTROL Filter by]** la barra per filtrare le opzioni seguenti:

* **Stato** Consente di filtrare per lo stato di moderazione corrente del contenuto: ** [!UICONTROL All Content]** **[!UICONTROL Approved]**, **[!UICONTROL Pending]**o **[!UICONTROL Bozo]**.

* **Sorgente** Consente di filtrare in base all'origine del contenuto. Seleziona **[!UICONTROL Livefyre]** per elencare direttamente nel flusso il contenuto generato dall'utente. Seleziona **[!UICONTROL Facebook]**, **[!UICONTROL Twitter]**o **[!UICONTROL RSS]** per includere il contenuto inserito nelle app da quelle origini.

* **Flags** Selecting Flags (Flag di selezione) consente di filtrare per **[!UICONTROL User Flags]** (Spam, Off-topic, Offensive o Non d'accordo), **[!UICONTROL System Flags]** applicata da SAFE (Profanity, Spam o Magically Moderated) o **[!UICONTROL Moderation Recommendations]**. ![](assets/appcontentfilter.png)

* **Data/Ora** Consente di eseguire il fiter in base alla posizione originale del contenuto **[!UICONTROL Created]** (oppure estraendo l'app tramite socialsync o a un flusso) oppure allo scorso **[!UICONTROL Modified]** (modificato, contrassegnato o stato modificato).

* **Autore** Consente di filtrare in base **[!UICONTROL IP]** all'indirizzo dell'autore **[!UICONTROL Display Name]** (nel pannello Utenti o sopra il contenuto pubblicato dall'autore) oppure **[!UICONTROL User ID]**(nel pannello Utenti).

* **Contiene** Consente di filtrare **[!UICONTROL Keyword]** i **[!UICONTROL Content Tag]**90 giorni di contenuto più recenti. Selezionate la **[!UICONTROL Media]** casella di controllo per restituire solo contenuti contenenti file multimediali. Per cercare tutti i contenuti, scorrete verso il basso tutto il contenuto dell'elenco, quindi fate clic **[!UICONTROL Search full data]**su.

   **Nota:** La ricerca di parole chiave multiple e tag di contenuto non è supportata. Se vengono inserite più parole chiave o tag, verrà utilizzata l'ultima parola per la ricerca.

   Durante la ricerca in base al tag Contenuto, i tag consigliati verranno compilati automaticamente quando digitate nel campo di ricerca. I risultati della ricerca restituiranno tutti i contenuti a cui è stato assegnato il tag. (Utilizzate questo campo per cercare Contenuti contenuti, oppure fate clic sull' **[!UICONTROL Featured]** etichetta su qualsiasi contenuto presente in Studio.)

   **Nota:** Utilizzate un segno meno (-) prima di un nome di tag per cercare il contenuto che non include tale tag. Ad esempio: Cercatè-Miley'per cercare tutti i contenuti che non includono il tag «Miley».

* **App** Consente di filtrare per **[!UICONTROL Collection ID]**, **[!UICONTROL App Tag]**o ID **principale**. Il filtro per ID principale restituisce tutto il contenuto di una risposta all'ID contenuto immesso. (Filtrare per più tag immettendo tag separati da virgole.)

* **Diritti** Consente di filtrare per stato Richieste diritti: ** [!UICONTROL Requested]** **[!UICONTROL Granted]**, **[!UICONTROL Replied]**o **[!UICONTROL Expired]**.

## Contenuto Bozo {#section_afl_vqm_zz}

Nelle app, **[!UICONTROL Bozo]** il contenuto viene visualizzato solo all'autore del contenuto. Questo consente all'utente di credere che il contenuto sia stato approvato, nascondendo al contempo la possibilità di nasconderlo da tutti gli altri utenti e moderatori.

>[!NOTE]
>
>Il contenuto social appartenente a socialsync o Streams **[!UICONTROL cannot]** deve essere impostato su Bozo.

Potete utilizzare il contenuto Bozo per i motivi seguenti:

* Il contenuto identificato come Spam da SAFE viene impostato automaticamente sullo stato Bozo.
* Tutto il contenuto di Utenti vietati viene impostato automaticamente su Bozo.
* Il contenuto può essere contrassegnato da Bozo da Studio.
* I moderatori possono utilizzare il contenuto Bozo direttamente nel flusso.

## Visualizza cronologia contenuto {#section_ayz_tqm_zz}

Il pannello Contenuto consente di esaminare la cronologia di tutto il contenuto elencato, inclusi la premoderazione, il filtraggio degli spam, la data post e qualsiasi flag o nota utente assegnato all'elemento.

Usate le schede nella parte inferiore del pannello del contenuto per visualizzarne la cronologia.

* **[!UICONTROL More Info:]** elenca tutte le attività su questo contenuto, inclusi invio, modifica, controllo dello spam, modifica dello stato e note. In questa sezione viene visualizzato l'ID contenuto Livefyre e l'indirizzo IP dell'utente.
* **[!UICONTROL Replies:]** elenca un massimo di 6 risposte. Fare clic per **[!UICONTROL Show all replies]** visualizzare tutte le risposte al post.

* **[!UICONTROL Flags & Reports:]** elenca tutti i flag utente, con l'avatar dell'utente che ha segnalato il contenuto e qualsiasi Report (note aggiunte dall'utente quando si segnalano i contenuti).
* **[!UICONTROL Add a note:]** consente di aggiungere una nota, visibile ad altri amministratori o moderatori.
* **[!UICONTROL Request Rights:]** apre la **[!UICONTROL New Rights Request]** finestra di dialogo da cui è possibile emettere una richiesta diritti.

* ****[!UICONTROL Save as Asset:]apre la **[!UICONTROL Advanced Options]** finestra di dialogo che consente di salvare l'elemento selezionato nella Libreria risorse, pubblicarlo su un'app o richiedere di riutilizzare i diritti di riuso dall'autore.

![](assets/PublishedMoreInfo-1024x462.png)

## Aggiungere un tag al contenuto {#section_xb4_mxr_rdb}

L'assegnazione di tag ai contenuti consente di categorizzare e organizzare i contenuti per facilitarne il recupero o la personalizzazione oppure di contrassegnare i contenuti come contenuti.

Per aggiungere tag, fai clic sull'icona più ( **[!UICONTROL +]**) sotto il contenuto. Immettete un nuovo tag oppure selezionatelo da un elenco di tag esistenti.

![](assets/PublishedAddTag-1024x338.png)

## Ricerca di immagini in tutte le risorse {#section_zxf_hsf_wcb}

Dopo aver aggiunto il contenuto alla libreria, potete cercare i contenuti in base ai tag avanzati.

Nella libreria, in Tutte le risorse, puoi cercare le immagini esistenti facendo clic su **[!UICONTROL Show Filters]** e quindi:

* Immissione del testo per la ricerca nel campo di ricerca
* Ordinamento per rilevanza
* Inserimento del testo nel **[!UICONTROL Tags]** campo per effettuare ricerche nei tag avanzati. L'algoritmo di classificazione tag Smart filtra il contenuto utilizzando un punteggio di attendibilità tag avanzato, il nuovo contenuto e il numero di stelle che l'utente ha fornito al contenuto.

## Contenuti contenuti {#section_emb_kqm_zz}

Selezionate il tag predefinito **[!UICONTROL Featured]** per contrassegnare il contenuto come mostrato ed evidenziarlo come importante per i vostri utenti. Una volta tag, utilizzate le opzioni di stile personalizzate per personalizzare il contenuto contenuti nelle app.

## Per visualizzare o deselezionare contenuto {#section_ojx_3qm_zz}

* Da Studio, fate clic sul **[!UICONTROL +]** segno accanto a una parte del contenuto, selezionate il **[!UICONTROL Featured]** tag nell'elenco a discesa e fate clic **[!UICONTROL Enter]** per visualizzare il contenuto. Il tag viene salvato e visualizzato accanto al contenuto.

* Per non funzionare, fate clic sul **[!UICONTROL x]****[!UICONTROL Featured]** tag visualizzato sul contenuto.

* Da un commenti, un blog live o un'app recensione, passate il mouse sul contenuto che desiderate utilizzare e fate clic **[!UICONTROL Feature]**. Per annullare la funzionalità, passate il mouse sul contenuto e fate clic **[!UICONTROL Unfeature]**.

>[!NOTE]
>
>A causa di vincoli di spazio, i contenuti chat possono essere contenuti o meno utilizzando Studio e potrebbero non essere contenuti nell'app stessa.

## Modifica dei contenuti contenuti {#section_pyw_hqm_zz}

Le azioni più regolari sul contenuto possono essere eseguite sul contenuto Contenuti, fatta eccezione per i seguenti elementi:

* I contenuti contenuti non possono essere segnalati.
* Gli utenti non possono modificarne il contenuto dopo che sono stati contenuti, ma possono comunque eliminarli, se desiderano. I moderatori possono modificare contenuti contenuti.

