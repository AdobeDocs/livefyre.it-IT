---
description: Puoi creare regole di streaming che estraggono il contenuto da Twitter.
seo-description: Puoi creare regole di streaming che estraggono il contenuto da Twitter.
seo-title: Regole Twitter
solution: Experience Manager
title: Regole Twitter
uuid: a 7 fd 2398-fd 6 b -4 c 24-92 b 2-7471176 d 7648
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Regole Twitter{#twitter-rules}

Puoi creare regole di streaming che estraggono il contenuto da Twitter.

Crea regole Twitter basate su hashtag, parole chiave, @ menzioni o autore.

Aggiungendo **[!UICONTROL Words]** e impostando una **[!UICONTROL Username]** regola verrà restituito contenuto che include entrambe le voci.

>[!NOTE]
>
>Livefyre aderisce alle linee guida sulla visualizzazione Twitter e i clienti hanno la responsabilità di rispettare anche tali linee guida. Per ulteriori informazioni, consulta la documentazione di Twitter sui requisiti [di visualizzazione](https://dev.twitter.com/terms/display-requirements).

Per creare regole Twitter per estrarre contenuti da feed Twitter nell&#39;app o nella cartella, puoi filtrare:

* **[!UICONTROL Keywords]**
   * Inserisci **[!UICONTROL Keywords]** da includere o escludere dal flusso Twitter. Specificando i valori per i campi **[!UICONTROL Contains any of these words]** e **[!UICONTROL Does not contain any of these words]** i campi restituiranno i tweet che contengono la prima e non contengono la seconda. È possibile inserire più valori per un campo singolo e restituiranno i risultati che contengono uno qualsiasi dei valori. Per utilizzare l&#39;operatore booleano E per cercare tweet con due o più parole, utilizzare due segni (*&amp; &amp;*) per separare le due parole.
   * Ad esempio, immettendo **[!UICONTROL Contains any of these words]** le parole chiave Giants, Posey e **[!UICONTROL Does not contain any of these words]** la parola chiave Dodger, verranno restituiti tutti i tweet che includono la parola *Giants* o *Posey* e non includono la parola *Dodger*.
Per cercare Tweet che includono sia le parole *Giants* che *Posey*, immettete «Giants &amp; &amp; Posey». Questa funzione è supportata solo per i campi **[!UICONTROL Contains any of these words]** e **[!UICONTROL Does not contain any of these words]** i campi delle regole Twitter.

* **[!UICONTROL Hashtags]**.
   * Inserisci **[!UICONTROL Hashtags]** da includere o escludere dal flusso Twitter. Se si specificano valori per **[!UICONTROL Contains any of these words]** e **[!UICONTROL Does not contain any of these words]** campi, restituiranno tweet contenenti hashtag nel primo campo e non contengono hashtag nel secondo campo. È possibile immettere più valori per un singolo campo. Lo streaming restituisce i risultati che contengono uno qualsiasi dei valori.

* **[!UICONTROL Usernames]**
   * Entra **[!UICONTROL @mentions]** o **[!UICONTROL authors]** fai clic per effettuare il flusso o escludere dallo streaming. Usate le caselle di controllo per specificare se **[!UICONTROL Retweets]** includere o **[!UICONTROL replies]** meno gli autori selezionati.
   >[!NOTE]
   >
   >Potete includere o escludere autori; non è possibile combinare questi due campi in una singola regola Twitter.

* **[!UICONTROL Minimum number of followers.]** Selezionate il numero minimo di follower che l&#39;utente deve avere per estrarre informazioni dai propri post.
* **[!UICONTROL Location]**

   * Inserite il percorso (città, cap, indirizzo o geocode nel formato di latitudine/longitudine comune (+/- 90, +/- 180)). Iniziate a digitare una posizione per visualizzare un menu a discesa con i suggerimenti. Selezionate una posizione dal menu a discesa. La mappa visualizza un perno della posizione. Regolate il cursore per selezionare un raggio da 25 a miglia per ogni posizione. Se non scegliete un raggio, Livefyre sceglie automaticamente un predefinito di otto miglia.
   >[!NOTE]
   >
   >Per entrambi i campi, la distanza verrà calcolata dal centro della posizione di input.

   * Potete aggiungere più posizioni e raggio. Per eliminare una posizione, fai clic sulla X accanto al nome di una posizione nella casella.
   * Combinate i **[!UICONTROL Is near this location]****[!UICONTROL Is not near this location]** campi e i campi per estrarre il contenuto all&#39;interno del **[!UICONTROL Is near this location]** campo, ma non nelle posizioni del **[!UICONTROL Is not near this location]** campo.


* **[!UICONTROL Additional Filters]**
   * Utilizzate altri filtri per perfezionare ulteriormente la regola Twitter. Specificate se:
      * Includi **[!UICONTROL Replies]** nei tweet di destinazione (se il flusso diventa alta, questa funzione verrà automaticamente disattivata.)
      * Includi tweet da **[!UICONTROL Verified Twitter accounts only.]**
      * Includere **[!UICONTROL All Content]**, **[!UICONTROL Vines Only]** o, oppure **[!UICONTROL Images Only.]**
      * Includere solo tweet originati da account con l&#39;opzione selezionato **[!UICONTROL Minimum number of followers]** (qualsiasi, 100, 500, 1000, 10,000 o 100,000).

Per le opzioni di Regole di flusso aggiuntive per tutte le regole Flusso, consultate [Opzioni regola di flusso per tutte le regole dei flussi](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
