---
description: Puoi creare regole di flusso per estrarre contenuti da Twitter.
seo-description: Puoi creare regole di flusso per estrarre contenuti da Twitter.
seo-title: Regole Twitter
solution: Experience Manager
title: Regole Twitter
uuid: a7fd2398-fd6b-4c24-92b2-7471176d7648
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 0%

---


# Regole Twitter{#twitter-rules}

Puoi creare regole di flusso per estrarre contenuti da Twitter.

Crea regole per Twitter basate su hashtag, parole chiave, @menzioni o autore.

Aggiungendo **[!UICONTROL Words]** e **[!UICONTROL Username]** per la regola, verrà restituito il contenuto che include entrambe le voci.

>[!NOTE]
>
>Livefyre aderisce alle linee guida di visualizzazione di Twitter e i clienti sono responsabili del rispetto di queste linee guida. Per ulteriori informazioni, consulta la documentazione di Twitter sui [requisiti di visualizzazione](https://dev.twitter.com/terms/display-requirements).

Per creare regole Twitter per estrarre contenuto dai feed Twitter nell&#39;app o nella cartella, potete filtrare in base a:

* **[!UICONTROL Keywords]**
   * Immettere **[!UICONTROL Keywords]** per essere incluso o escluso dal flusso Twitter. Se si specificano valori per i campi **[!UICONTROL Contains any of these words]** e **[!UICONTROL Does not contain any of these words]**, verranno restituiti i tweet contenenti il primo e non il secondo. È possibile immettere più valori per un singolo campo e restituire risultati che contengono uno qualsiasi dei valori. Per utilizzare l&#39;operatore booleano AND per cercare tweet con due o più parole, utilizzare due e commerciale (*&amp;&amp;*) per separare le due parole.
   * Ad esempio, immettendo **[!UICONTROL Contains any of these words]** parole chiave Giants, Posey e **[!UICONTROL Does not contain any of these words]** parola chiave Dodger, verranno restituiti tutti i tweet che includono la parola *Giants* o *Posey* e non includeranno la parola *Dodger*.
Per cercare i tweet che includono sia le parole *Giants* che *Posey*, immettete &quot;Giants &amp; Posey&quot;. Questa funzione è supportata solo per i campi **[!UICONTROL Contains any of these words]** e **[!UICONTROL Does not contain any of these words]** nelle regole di Twitter.

* **[!UICONTROL Hashtags]**.
   * Immettere **[!UICONTROL Hashtags]** per essere incluso o escluso dal flusso Twitter. Se si specificano valori per i campi **[!UICONTROL Contains any of these words]** e **[!UICONTROL Does not contain any of these words]**, verranno restituiti i tweet contenenti hashtag nel primo campo e non gli hashtag nel secondo. È possibile immettere più valori per un singolo campo. Il flusso restituisce risultati che contengono uno qualsiasi dei valori.

* **[!UICONTROL Usernames]**
   * Immettere **[!UICONTROL @mentions]** o **[!UICONTROL authors]** per eseguire il pull nel flusso o escludere dal flusso. Utilizzare le caselle di controllo per definire se includere anche **[!UICONTROL Retweets]** o **[!UICONTROL replies]** degli autori selezionati.

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
   * Combinate i campi **[!UICONTROL Is near this location]** e **[!UICONTROL Is not near this location]** per estrarre contenuto all&#39;interno delle posizioni nel campo **[!UICONTROL Is near this location]**, ma non vicino alle posizioni nel campo **[!UICONTROL Is not near this location]**.


* **[!UICONTROL Additional Filters]**
   * Utilizzate Filtri aggiuntivi per perfezionare ulteriormente la regola Twitter. Specificate se:
      * Includi **[!UICONTROL Replies]** nei tweet di destinazione (se il flusso diventa ad alta velocità, questa funzione verrà disattivata automaticamente).
      * Includi tweet da **[!UICONTROL Verified Twitter accounts only.]**
      * Includere **[!UICONTROL All Content]**, **[!UICONTROL Vines Only]** o **[!UICONTROL Images Only.]**
      * Include solo i tweet che provengono da account con il **[!UICONTROL Minimum number of followers]** selezionato (uno, 100, 500, 1000, 10.000 o 100.000).

Per ulteriori opzioni della regola di flusso per tutte le regole di flusso, vedere [Opzioni regola di flusso per tutte le regole di flusso](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
