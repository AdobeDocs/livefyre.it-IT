---
description: Puoi creare regole di flusso per estrarre contenuti da Twitter.
seo-description: Puoi creare regole di flusso per estrarre contenuti da Twitter.
seo-title: Regole Twitter
solution: Experience Manager
title: Regole Twitter
uuid: a7fd2398-fd6b-4c24-92b2-7471176d7648
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Regole Twitter{#twitter-rules}

Puoi creare regole di flusso per estrarre contenuti da Twitter.

Crea regole per Twitter basate su hashtag, parole chiave, @menzioni o autore.

L'aggiunta **[!UICONTROL Words]** e una **[!UICONTROL Username]** regola restituiranno il contenuto che include entrambe le voci.

>[!NOTE]
>
>Livefyre aderisce alle linee guida di visualizzazione di Twitter e i clienti sono responsabili del rispetto di queste linee guida. Per ulteriori informazioni, consultate la documentazione di Twitter sui requisiti di [visualizzazione](https://dev.twitter.com/terms/display-requirements).

Per creare regole Twitter per estrarre contenuto dai feed Twitter nell'app o nella cartella, potete filtrare in base a:

* **[!UICONTROL Keywords]**
   * Immettete **[!UICONTROL Keywords]** per essere incluso o escluso dal flusso Twitter. Se si specificano valori sia per i campi **[!UICONTROL Contains any of these words]** che per **[!UICONTROL Does not contain any of these words]** i campi, verranno restituiti i tweet contenenti il primo e che non contengono il secondo. È possibile immettere più valori per un singolo campo e restituire risultati che contengono uno qualsiasi dei valori. Per utilizzare l'operatore booleano AND per cercare tweet con due o più parole, utilizzare due e-mail (*&amp;&amp;*) per separare le due parole.
   * Ad esempio, l'immissione di **[!UICONTROL Contains any of these words]** parole chiave Giants, Posey e **[!UICONTROL Does not contain any of these words]** parola chiave Dodger restituirà tutti i tweet che includono la parola *Giants* o *Posey* e non includono la parola *Dodger*.
Per cercare i tweet che includono sia le parole *Giants* che *Posey*, immettete "Giants &amp; Posey". Questa funzione è supportata solo per i campi **[!UICONTROL Contains any of these words]** e nelle **[!UICONTROL Does not contain any of these words]** regole di Twitter.

* **[!UICONTROL Hashtags]**.
   * Immettete **[!UICONTROL Hashtags]** per essere incluso o escluso dal flusso Twitter. Se si specificano valori sia per i campi **[!UICONTROL Contains any of these words]** **[!UICONTROL Does not contain any of these words]** che per quelli corrispondenti, verranno restituiti i tweet contenenti hashtag nel primo campo e non gli hashtag nel secondo. È possibile immettere più valori per un singolo campo. Il flusso restituisce risultati che contengono uno qualsiasi dei valori.

* **[!UICONTROL Usernames]**
   * Immettere **[!UICONTROL @mentions]** o **[!UICONTROL authors]** per eseguire il pull nel flusso o escludere dal flusso. Utilizzare le caselle di controllo per definire se includere anche **[!UICONTROL Retweets]** o **[!UICONTROL replies]** da autori selezionati.
   >[!NOTE]
   >
   >Potete includere o escludere autori; non potete combinare questi due campi in una singola regola Twitter.

* **[!UICONTROL Minimum number of followers.]** Selezionate il numero minimo di follower che l’utente deve avere per estrarre informazioni dai post.
* **[!UICONTROL Location]**

   * Immettete la posizione (città, codice postale, indirizzo o codice geografico nel formato latitudine/longitudine comune (+/- 90, +/- 180). Iniziate a digitare una posizione per visualizzare un menu a discesa con i suggerimenti. Selezionate una posizione dall’elenco a discesa. La mappa mostra un perno della posizione. Regolare il cursore per selezionare un raggio compreso tra 1 e 25 miglia per ogni posizione. Se non scegliete un raggio, Livefyre sceglie automaticamente un valore predefinito di 8 miglia.
   >[!NOTE]
   >
   >Per entrambi i campi, la distanza viene calcolata dal centro della posizione di input.

   * È possibile aggiungere più posizioni e un raggio. Per eliminare una posizione, fate clic sulla X accanto al nome di una posizione nella casella.
   * Combinate i campi **[!UICONTROL Is near this location]** e **[!UICONTROL Is not near this location]** per estrarre il contenuto all'interno delle posizioni nel **[!UICONTROL Is near this location]** campo, ma non vicino alle posizioni nel **[!UICONTROL Is not near this location]** campo.


* **[!UICONTROL Additional Filters]**
   * Utilizzate Filtri aggiuntivi per perfezionare ulteriormente la regola Twitter. Specificate se:
      * Includi **[!UICONTROL Replies]** nei tweet di destinazione (se il flusso diventa ad alta velocità, questa funzione viene disattivata automaticamente).
      * Includi tweet da **[!UICONTROL Verified Twitter accounts only.]**
      * Include **[!UICONTROL All Content]**, oppure **[!UICONTROL Vines Only]**, **[!UICONTROL Images Only.]**
      * Include solo i tweet che provengono da account con gli account selezionati **[!UICONTROL Minimum number of followers]** (uno, 100, 500, 1000, 10.000 o 100.000).

Per ulteriori opzioni della regola di flusso per tutte le regole di flusso, vedere Opzioni della regola di [flusso per tutte le regole](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)di flusso.
