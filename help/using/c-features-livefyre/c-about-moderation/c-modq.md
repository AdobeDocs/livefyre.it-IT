---
description: Consente di moderare i contenuti da un’unica interfaccia intelligente.
title: Contenuto moderato utilizzando ModQ
exl-id: 694b1f45-2b24-4e80-99a1-788e2cecc8a4
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '1454'
ht-degree: 0%

---

# Contenuto moderato utilizzando ModQ{#moderate-content-using-modq}

Consente di moderare i contenuti da un’unica interfaccia intelligente.

ModQ crea una coda in tempo reale di tutto il contenuto del sito o della rete che corrisponde alle regole di moderazione definite, consentendo ai moderatori di concentrarsi solo sul contenuto che richiede la loro attenzione.

Una volta definite le impostazioni ModQ, il nuovo contenuto che entra nel flusso o il contenuto esistente contrassegnato dagli utenti verranno aggiunti alla coda. Le modifiche alle regole non rimuoveranno il contenuto dal ModQ, ma aggiungeranno nuovo contenuto alla coda in base alle nuove impostazioni.

ModQ consente di:

* Modera nel contesto, visualizza interi thread e Approva, Elimina o Bozo singoli contenuti o thread completi con un solo clic.
* Maggiore velocità ed efficienza del flusso di lavoro.
* Rispondi ai contenuti, aumentando il tuo coinvolgimento con la tua community.
* Consente a più moderatori di lavorare attraverso i contenuti senza duplicare il lavoro degli altri.

Il contenuto Livefyre è elencato in ModQ per un massimo di 6 settimane, e il contenuto di flussi premoderati che non è stato affrontato viene elencato in ModQ per 90 giorni.

>[!NOTE]
>
>Un singolo contenuto può essere elencato più volte se corrisponde a più regole per l’inclusione in ModQ. Ad esempio, se un contenuto attiva una regola di flag utente per Offensive, in seguito attiva un’altra regola per Profane, verrà elencato due volte in ModQ.

Il contenuto che non viene visualizzato in ModQ include:

* Contenuto scortato.
* Contenuto approvato da un moderatore.
* Contenuto pubblicato da un utente vietato o flag di utenti applicati da un utente vietato.

## Navigazione in ModQ {#section_uv4_db2_yy}

ModQ è suddiviso in due pannelli a schede:

* **[!UICONTROL Items]** elenca tutti i contenuti nativi di Livefyre e SocialSync destinati alla moderazione. Questa scheda include qualsiasi contenuto di Social Search o Stream contrassegnato o modificato dopo la moderazione.
* **[!UICONTROL Streams Premoderation]** elenca tutti i contenuti che entrano nelle app da Streams con Premoderato abilitato. (Per ulteriori informazioni, vedere Creazione di flussi.)

Entrambe le schede offrono molti degli stessi filtri e strumenti di moderazione.

* **[!UICONTROL Item Count]** Il numero di elementi rimanenti nella coda viene visualizzato nell’angolo in alto a sinistra di ModQ.
* **[!UICONTROL Filter]** Fai clic  **[!UICONTROL Filter]** per definire i parametri in base ai quali il contenuto verrà elencato nel riquadro.
* **[!UICONTROL History]** Fai clic sul  **[!UICONTROL History]** pulsante in alto a destra dello schermo per aprire un elenco di contenuti moderati di recente, che ti consente di rivedere il tuo lavoro o modificare una recente azione di moderazione. Fai nuovamente clic sul pulsante per tornare al contenuto in coda. Verranno visualizzate solo le 100 azioni più recenti. **** La cronologia non elenca le azioni eseguite da un altro moderatore.

* **[!UICONTROL User Pane]** Fare clic sui pulsanti espandi o comprimi in alto a destra della pagina per aprire o chiudere il riquadro Utente.

## Informazioni sul contenuto di ModQ {#section_oxm_kgz_y1b}

Ogni contenuto elencato presenta informazioni di anteprima, compreso il sito in cui è stato pubblicato e il relativo autore. Quando si seleziona un elemento, viene visualizzato l’intero contenuto, compresi eventuali contenuti multimediali.

>[!NOTE]
>
>Il contenuto nativo di Livefyre visualizzerà più informazioni del contenuto aggiunto all&#39;App tramite Streams o altre fonti di social media.

Quando selezioni un elemento vengono visualizzate le seguenti informazioni:

* **[!UICONTROL Time in Queue:]** elenca il tempo di aggiunta del contenuto a ModQ.
* **[!UICONTROL App name:]** l’app in cui viene visualizzato il contenuto. Collegamenti al sito con l’app.
* **[!UICONTROL Content Body:]** miniatura di testo e contenuti multimediali, se disponibile.
* **[!UICONTROL Status:]** lo stato corrente del contenuto (In sospeso, Trashed e così via).
* **[!UICONTROL Author information:]** nome e nome utente dell’autore.
* **[!UICONTROL Timestamp:]** la marca temporale relativa di quando è stato creato il contenuto. Esegue il collegamento a una parte del contenuto della pagina Contenuto app di Studio.
* **[!UICONTROL Flag Type:]** Offensivo, non d&#39;accordo, spam e così via.

   * Flag SICURI: Spam e Bulk.
   * Flag applicato dall&#39;elenco dei profitti della rete e del sito: Profanità.
   * Flag applicati da SAFE: Discorsi d&#39;odio, PII (informazioni personali), Insulto e Profanity.
   * Flag utente: Spam, Off-topic, Offensivo e in disaccordo.

* **[!UICONTROL Flag origin:]** l’origine del flag elencato. Può essere SAFE, un nome utente o Livefyre.
* **[!UICONTROL More info:]** elenca i dettagli del contenuto, compresi il numero di Mi piace, Flag utente, Risposte ed eventuali tag applicati al contenuto. Facendo clic su Sito si apre la pagina di primo livello del sito in cui si trova il contenuto. Facendo clic sulla marca temporale si apre una visualizzazione thread del contenuto nel contesto della pagina.

## Opzioni filtro nel ModQ {#section_r2c_qc2_yy}

Fai clic su **[!UICONTROL Filter]** in alto a sinistra nella finestra ModQ per aprire un pannello con le opzioni di filtro disponibili per i contenuti elencati. Quando selezioni le opzioni, ModQ si aggiorna automaticamente per elencare solo il contenuto filtrato. Fare clic su **[!UICONTROL Clear filters]** per cancellare tutte le opzioni selezionate e ricaricare l&#39;elenco completo degli elementi.

Sono disponibili diverse opzioni di filtro per le schede **[!UICONTROL Items]** e **[!UICONTROL Streams Premoderation]** .

Le seguenti opzioni sono disponibili per ModQ sia in **[!UICONTROL Items]** che in **[!UICONTROL Streams Premoderation]**:

* **[!UICONTROL App]**. Usa il campo Ricerca app per filtrare i risultati per app. È possibile selezionare più app.
* **[!UICONTROL System Flags]**. Filtrare il contenuto in base a regole quali Spam, Profanity, SAFE e Premoderation.

   * Selezionando **[!UICONTROL Spam]** tutti i contenuti saranno etichettati come Spam by SAFE (Spam by SAFE).
   * Selezionando **[!UICONTROL Profanity]** verranno elencati tutti i contenuti con tag Profane in base all’elenco di profili di rete o sito.
   * Selezionando **[!UICONTROL SAFE]** verranno elencati tutti i contenuti che entrano in ModQ in seguito alle tue regole SAFE.
   * Selezionando **[!UICONTROL Premoderation]** verranno elencati tutti i contenuti contrassegnati per la moderazione dalle impostazioni di rete, flusso o app.

* **[!UICONTROL User Flags]** Filtrare il contenuto in base ai flag utente. Le opzioni includono Offensive, Spam, Off-topic e Non d&#39;accordo.
* **[!UICONTROL Rights Requests.]** Per visualizzare solo il contenuto con i diritti concessi, fai clic sulla casella di controllo .
* **[!UICONTROL Entered the queue.]** Filtrare il contenuto in base all’intervallo di tempo durante il quale il contenuto è stato inviato a ModQ. Il contenuto dell’ora è stato inviato a ModQ non è necessariamente il momento in cui il contenuto è stato pubblicato nella relativa app.

Le seguenti opzioni sono disponibili per ModQ in **[!UICONTROL Streams Premoderation]**:

* **[!UICONTROL Social Source]** Filtrare il contenuto in base all’origine social da cui è stato creato il contenuto. Ad esempio, le opzioni delle fonti social includono Twitter, Instagram, Facebook e RSS.

La seguente opzione è disponibile per ModQ in **[!UICONTROL Items]**:

**[!UICONTROL Moderation Recommendations]**. Filtrare il contenuto in base alla raccomandazione fornita dalla raccomandazione di moderazione automatizzata.

Le immagini seguenti mostrano l&#39;aspetto di Moderation Recommendations in ModQ:  ![](assets/mod_reco1.png)

La raccomandazione di moderazione viene fornita per i contenuti quando è impostata in **[!UICONTROL Network Settings > Moderation]** e **[!UICONTROL Network Settings > ModQ]**.

## Azioni utilizzabili in ModQ {#section_h4g_wrn_z1b}

Puoi decidere cosa fare con ogni elemento di contenuto nel ModQ.

Selezionare una delle opzioni seguenti:

* Icona **[!UICONTROL Checkbox]** per approvare il contenuto
* Icona **[!UICONTROL Trash can]** per inviare il contenuto al cestino
* **[!UICONTROL Request Rights]** per richiedere i diritti al contenuto dal proprietario del contenuto.

   >[!NOTE]
   >
   >Non è possibile richiedere i diritti in ModQ per il contenuto da Instagram. Devi utilizzare la libreria o il contenuto dell’app per inviare richieste di diritti per il contenuto da Instagram.

* **[!UICONTROL Feature and Approve]** per approvare il contenuto e includerlo anche.
* **[!UICONTROL Product Tag and Approve]** per aggiungere al contenuto un prodotto dal catalogo di prodotti e quindi approvarlo.
* **[!UICONTROL Mark as Pending]** per contrassegnare il contenuto come in sospeso.

>[!NOTE]
>
>Una volta eliminato un contenuto, il contenuto e tutte le risposte al contenuto vengono rimossi permanentemente da ModQ. Per inserire un contenuto eliminato in un&#39;app, consulta [Aggiungere un elemento eliminato in un&#39;app](/help/using/c-features-livefyre/c-about-moderation/t-add-trashed-item-back-into-app.md#t_add_trashed_item_back_into_app).

Se il contenuto è già nello stato desiderato, scegliendo Elimina, Bozo o Approva verrà confermato lo stato e verrà rimosso l’elemento dall’elenco. La moderazione di un contenuto lo rimuove immediatamente dalla coda e lo disattiva nelle code di altri moderatori.

>[!NOTE]
>
>Il contenuto del flusso non può essere Bozo’d. Il tracciamento del contenuto Stream lo rimuoverà definitivamente dal flusso e non può essere annullato.

Una volta che il contenuto è stato moderato, verrà rimosso dal ModQ del moderatore e il suo autore non può più modificarlo dall’interno del flusso. Se un moderatore elimina un elemento o un utente elimina il proprio commento, questo verrà visualizzato in grigio nelle code degli altri moderatori in tempo reale. Quando il contenuto è disabilitato, il pulsante **[!UICONTROL Clear Moderated]** viene visualizzato sulla pagina, consentendo ai moderatori di rimuoverlo dai loro elenchi e di mantenere la propria posizione sulla pagina indipendentemente da altre attività di moderatore.

## Utilizzo della funzione Cestino in ModQ {#section_tpx_qgz_y1b}

Utilizza la sezione impostazioni per selezionare le opzioni disponibili quando il contenuto è contrassegnato come Trashed.

* ****[!UICONTROL Confirm Trash]**** Abilita questa opzione per richiedere ai moderatori di confermare la propria azione quando imposti il contenuto su Cestino. Quando è abilitata, la selezione di **[!UICONTROL Trash]** per il contenuto visualizzerà una finestra di dialogo in cui viene richiesto un elemento **[!UICONTROL Reason for Moderation]** e offrirà un campo in cui è possibile inserire un elemento **[!UICONTROL Note]**.

   (Questa impostazione è disponibile **[!UICONTROL only]** a livello di rete e si applica a tutti i siti della rete.)

* ****[!UICONTROL Hide Replies]**** Abilita questa opzione per eliminare automaticamente le risposte quando un commento principale viene eliminato o Bozo’d.

## Modifica stato utente in ModQ {#section_tmw_lg1_z1b}

Fai clic sul pulsante **[!UICONTROL User actions]** nel pannello Riepilogo utente per disattivare, bandire o inserire nell’elenco Consentiti l’utente.

* **[!UICONTROL Mute:]** consente di disattivare i contrassegni dall’utente che ha contrassegnato il contenuto elencato. Utilizza questa opzione per escludere i flag dell’utente dai filtri di premoderazione. Il contenuto che contrassegnano non entrerà in ModQ a seguito del flag e i relativi flag non saranno inclusi nelle regole di flag.
* **[!UICONTROL Ban:]** consente di vietare l’utente elencato dal sito o dalla rete. Solo gli amministratori di Studio o i gestori utenti possono vietare la rete a un utente.
* **[!UICONTROL Whitelist:]** consente di inserire nell’elenco Consentiti l’utente elencato per il sito o la rete. Solo gli amministratori di Studio o i gestori utente possono collegare in rete un utente all’elenco Consentiti.



App che utilizzano ModQ:

* [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Commenti](/help/using/c-about-apps/c-comments/c-comments.md)
* [Recensioni](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Note](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Memorizza 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Pulsante Carica](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)
