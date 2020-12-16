---
description: Consente di moderare i contenuti da un'unica interfaccia intelligente.
seo-description: Consente di moderare i contenuti da un'unica interfaccia intelligente.
seo-title: Contenuto moderato con ModQ
title: Contenuto moderato con ModQ
uuid: c630fb85-7bd0-4da0-ac7e-080e970fb4f9
translation-type: tm+mt
source-git-commit: 52f59cd15f315aa93be198f6eb586f008c18a384
workflow-type: tm+mt
source-wordcount: '1465'
ht-degree: 0%

---


# Contenuto moderato con ModQ{#moderate-content-using-modq}

Consente di moderare i contenuti da un&#39;unica interfaccia intelligente.

ModQ crea una coda in tempo reale di tutto il contenuto del sito o della rete che corrisponde alle regole di moderazione definite, consentendo ai moderatori di concentrarsi solo sul contenuto che richiede la loro attenzione.

Una volta definite le impostazioni ModQ, alla coda verrà aggiunto nuovo contenuto che entra nel flusso o contenuto esistente contrassegnato dagli utenti. Le modifiche apportate alle regole non rimuoveranno il contenuto dal ModQ, ma aggiungeranno nuovo contenuto alla coda in base alle nuove impostazioni.

ModQ consente di:

* Consente di moderare nel contesto, visualizzare interi thread e Approvare, Cestino o Bozo singole parti di contenuto o completare i thread con un solo clic.
* Maggiore velocità ed efficienza del flusso di lavoro.
* Rispondi ai contenuti, aumentando il coinvolgimento con la community.
* Consente a più moderatori di lavorare attraverso il contenuto, senza duplicare il lavoro dell&#39;altro.

Il contenuto Livefyre è elencato in ModQ per un massimo di 6 settimane, mentre il contenuto dei flussi premoderati che non è stato risolto viene elencato in ModQ per 90 giorni.

>[!NOTE]
>
>Un singolo contenuto può essere elencato più volte se corrisponde a più regole per l’inclusione in ModQ. Ad esempio, se una parte di contenuto attiva una regola di flag utente per Offensive, in seguito attiva un&#39;altra regola per Profane, questa verrà elencata due volte in ModQ.

Il contenuto non visualizzato in ModQ include:

* Contenuto con traccia.
* Contenuto approvato da un moderatore.
* Contenuto pubblicato da un utente censurato o flag di utente applicati da un utente censurato.

## Navigazione in ModQ {#section_uv4_db2_yy}

ModQ è suddiviso in due pannelli a schede:

* **[!UICONTROL Items]** elenca tutti i contenuti Livefyre nativi e SocialSync destinati alla moderazione. Questa scheda include qualsiasi contenuto Social Search o Stream contrassegnato o modificato dopo la moderazione.
* **[!UICONTROL Streams Premoderation]** elenca tutti i contenuti che entrano nelle app dai flussi con l&#39;opzione Premoderato abilitata. Per ulteriori informazioni, consultate Creazione di flussi.

Entrambe le schede offrono molti degli stessi filtri e strumenti di moderazione.

* **[!UICONTROL Item Count]** Il numero di elementi rimanenti nella coda viene visualizzato nell&#39;angolo superiore sinistro di ModQ.
* **[!UICONTROL Filter]** Fare clic  **[!UICONTROL Filter]** per definire i parametri in base ai quali il contenuto verrà elencato nel riquadro.
* **[!UICONTROL History]** Fate clic sul  **[!UICONTROL History]** pulsante in alto a destra dello schermo per aprire un elenco di contenuti moderati di recente, che consente di rivedere il lavoro o di modificare una moderazione recente. Fate di nuovo clic sul pulsante per tornare al contenuto in coda. Verranno visualizzate solo le 100 azioni più recenti. **La** cronologia non elenca le azioni eseguite da un altro moderatore.

* **[!UICONTROL User Pane]** Fate clic sui pulsanti di espansione o riduzione in alto a destra della pagina per aprire o chiudere il riquadro Utente.

## Informazioni sul contenuto di ModQ {#section_oxm_kgz_y1b}

Ogni contenuto elencato presenta informazioni di anteprima, compreso il sito in cui è stato pubblicato e il relativo autore. Quando si seleziona un elemento, viene visualizzata l’intera parte di contenuto, compresi eventuali supporti.

>[!NOTE]
>
>Il contenuto nativo di Livefyre visualizzerà più informazioni del contenuto aggiunto all&#39;app tramite Streams o altre fonti di social media.

Quando selezionate un elemento vengono visualizzate le informazioni seguenti:

* **[!UICONTROL Time in Queue:]** elenca il tempo durante il quale il contenuto è stato aggiunto a ModQ.
* **[!UICONTROL App name:]** l&#39;app in cui viene visualizzato il contenuto. Collegamenti al sito con l&#39;app.
* **[!UICONTROL Content Body:]** miniatura del testo e del supporto, se disponibile.
* **[!UICONTROL Status:]** lo stato corrente del contenuto (In sospeso, Con cestino e così via).
* **[!UICONTROL Author information:]** nome e nome utente dell’autore.
* **[!UICONTROL Timestamp:]** la marca temporale relativa di quando è stato creato il contenuto. Esegue il collegamento a una parte del contenuto nella pagina Contenuto app di Studio.
* **[!UICONTROL Flag Type:]** Offensiva, non d&#39;accordo, spam e così via

   * Flag SICUREZZA: Spam e Bulk.
   * Flag applicato dall&#39;elenco delle funzionalità di rete e sito: Profanità.
   * Flag applicati da SAFE: Discorsi di odio, PII (Informazioni personali), Insulti e Profanità.
   * Flag utente: Spam, Off-topic, Offensive e in disaccordo.

* **[!UICONTROL Flag origin:]** l’origine del flag elencato. Può essere SAFE, un nome utente o Livefyre.
* **[!UICONTROL More info:]** elenca i dettagli del contenuto, compreso il numero di collegamenti, flag utente, risposte ed eventuali tag applicati al contenuto. Facendo clic su Sito si apre la pagina di primo livello del sito in cui si trova il contenuto. Facendo clic sul timestamp si apre una visualizzazione concatenata del contenuto nel contesto della pagina.

## Opzioni filtro in ModQ {#section_r2c_qc2_yy}

Fate clic su **[!UICONTROL Filter]** in alto a sinistra nella finestra ModQ per aprire un pannello con le opzioni di filtro disponibili per i contenuti elencati. Quando si selezionano le opzioni, ModQ si aggiorna automaticamente per elencare solo il contenuto filtrato. Fare clic su **[!UICONTROL Clear filters]** per cancellare tutte le opzioni selezionate e ricaricare l&#39;elenco completo degli elementi.

Sono disponibili diverse opzioni di filtro per le schede **[!UICONTROL Items]** e **[!UICONTROL Streams Premoderation]**.

Le seguenti opzioni sono disponibili per ModQ sia in **[!UICONTROL Items]** che in **[!UICONTROL Streams Premoderation]**:

* **[!UICONTROL App]**. Usate il campo App di ricerca per filtrare i risultati per app. È possibile selezionare più app.
* **[!UICONTROL System Flags]**. Filtrare il contenuto in base a regole quali Spam, Profanity, SAFE e Premoderazione.

   * Se si seleziona **[!UICONTROL Spam]**, verrà visualizzato tutto il contenuto contrassegnato come Spam by SAFE (Spam by SAFE).
   * Selezionando **[!UICONTROL Profanity]** verranno elencati tutti i contenuti contrassegnati con il tag Profane (Profano) dalla rete o dall&#39;elenco delle proprietà del sito.
   * Se si seleziona **[!UICONTROL SAFE]**, verranno elencati tutti i contenuti che entrano in ModQ a seguito delle regole SICURE.
   * Selezionando **[!UICONTROL Premoderation]** verranno elencati tutti i contenuti contrassegnati per la moderazione dalla rete, dal flusso o dalle impostazioni dell&#39;app.

* **[!UICONTROL User Flags]** Filtrare il contenuto in base ai flag utente. Le opzioni includono Offensiva, Spam, Off-topic e Non d&#39;accordo.
* **[!UICONTROL Rights Requests.]** Per visualizzare solo il contenuto per il quale sono stati concessi i diritti, fate clic sulla casella di controllo.
* **[!UICONTROL Entered the queue.]** Filtrare il contenuto in base all’intervallo di tempo durante il quale il contenuto è stato inviato a ModQ. L’ora in cui il contenuto è stato inviato a ModQ non è necessariamente l’ora in cui è stato pubblicato nell’app.

Le seguenti opzioni sono disponibili per ModQ in **[!UICONTROL Streams Premoderation]**:

* **[!UICONTROL Social Source]** Filtrare il contenuto in base all&#39;origine del social network. Ad esempio, le opzioni delle fonti sociali includono Twitter, Instagram, Facebook e RSS.

L&#39;opzione seguente è disponibile per ModQ in **[!UICONTROL Items]**:

**[!UICONTROL Moderation Recommendations]**. Filtrare il contenuto in base alla raccomandazione fornita dalla raccomandazione di moderazione automatica.

Le immagini seguenti mostrano l’aspetto di Moderazione Recommendations in ModQ:  ![](assets/mod_reco1.png)

La raccomandazione di moderazione viene fornita per il contenuto quando è impostata in **[!UICONTROL Network Settings > Moderation]** e **[!UICONTROL Network Settings > ModQ]**.

## Azioni utilizzabili in ModQ {#section_h4g_wrn_z1b}

Potete decidere cosa fare con ogni contenuto nel ModQ.

Selezionate una delle seguenti opzioni:

* Icona **[!UICONTROL Checkbox]** per approvare il contenuto
* Icona **[!UICONTROL Trash can]** per inviare il contenuto al cestino
* **[!UICONTROL Request Rights]** per richiedere i diritti al contenuto al proprietario del contenuto.

   >[!NOTE]
   >
   >Non potete richiedere i diritti in ModQ per il contenuto da Instagram. Devi usare la libreria o il contenuto dell&#39;app per inviare richieste di diritti per il contenuto da Instagram.

* **[!UICONTROL Feature and Approve]** per approvare il contenuto e includere anche il contenuto.
* **[!UICONTROL Product Tag and Approve]** per aggiungere al contenuto un prodotto dal catalogo prodotti e quindi approvarlo.
* **[!UICONTROL Mark as Pending]** per contrassegnare il contenuto come in sospeso.

>[!NOTE]
>
>Una volta eseguito il cestino di una parte del contenuto, la parte del contenuto e tutte le risposte al contenuto vengono rimosse da ModQ in modo permanente. Per inserire un contenuto spazzatura in un&#39;app, vedi [Aggiungi un elemento con cestino in un&#39;app](/help/using/c-features-livefyre/c-about-moderation/t-add-trashed-item-back-into-app.md#t_add_trashed_item_back_into_app).

Se il contenuto è già nello stato desiderato, scegliendo Cestino, Bozo o Approva lo stato verrà confermato e l’elemento verrà rimosso dall’elenco. Moderare un contenuto lo rimuove immediatamente dalla coda e lo disattiva nelle code di altri moderatori.

>[!NOTE]
>
>Il contenuto del flusso potrebbe non essere Bozo’d. Il tracciamento del contenuto del flusso lo rimuove definitivamente dal flusso e non può essere annullato.

Dopo che il contenuto è stato moderato, verrà rimosso dal ModQ del moderatore e l&#39;autore non potrà più modificarlo dall&#39;interno del flusso. Se un moderatore ignora un elemento o se un utente elimina un commento, questo viene visualizzato in grigio nelle code degli altri moderatori in tempo reale. Quando il contenuto è stato disattivato, il pulsante **[!UICONTROL Clear Moderated]** viene visualizzato sulla pagina, consentendo ai moderatori di rimuoverlo dagli elenchi e di mantenere la propria posizione sulla pagina indipendentemente dalle altre attività dei moderatori.

## Utilizzo della funzione Cestino in ModQ {#section_tpx_qgz_y1b}

Utilizzate la sezione delle impostazioni per selezionare le opzioni disponibili quando il contenuto è contrassegnato come Trashed.

* ****[!UICONTROL Confirm Trash]**** Abilitate questa opzione per richiedere che i moderatori confermino la propria azione quando impostate il contenuto sul cestino. Quando questa opzione è attivata, quando si seleziona **[!UICONTROL Trash]** per il contenuto viene visualizzata una finestra di dialogo in cui viene richiesto un **[!UICONTROL Reason for Moderation]** e viene offerto un campo in cui è possibile inserire un elemento **[!UICONTROL Note]**.

   (Questa impostazione è disponibile **[!UICONTROL only]** a livello di rete e si applica a tutti i siti della rete.)

* ****[!UICONTROL Hide Replies]**** Abilitate questa opzione per ignorare automaticamente le risposte quando un commento principale viene eliminato o se è stato impostato Bozo’d.

## Modifica stato utente in ModQ {#section_tmw_lg1_z1b}

Fate clic sul pulsante **[!UICONTROL User actions]** nel pannello Riepilogo utenti per disattivare, bandire o consentire l&#39;elenco degli utenti.

* **[!UICONTROL Mute:]** consente di disattivare i flag dell’utente che ha segnalato il contenuto elencato. Utilizzate questa opzione per escludere i flag dell&#39;utente dai filtri di moderazione. Il contenuto a cui viene applicato il contrassegno non verrà inserito in ModQ come risultato del flag e i relativi flag non saranno inclusi nelle regole di contrassegno.
* **[!UICONTROL Ban:]** consente di vietare l’utente elencato dal sito o dalla rete. Solo gli amministratori di studio o i manager utente possono vietare la rete a un utente.
* **[!UICONTROL Whitelist:]** consente di consentire l’elenco degli utenti elencati per il sito o la rete. Solo gli amministratori di studio o i manager utente possono consentire l&#39;elenco di un utente mediante la rete.



App che utilizzano ModQ:

* [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Commenti](/help/using/c-about-apps/c-comments/c-comments.md)
* [Recensioni](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Pulsante Carica](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

