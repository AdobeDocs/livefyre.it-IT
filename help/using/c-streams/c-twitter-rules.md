---
description: Puoi creare regole di flusso per estrarre contenuto da Twitter.
title: Regole twitter
exl-id: 3a5081eb-048d-4dcf-80a2-366af2cb2c86
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# Regole twitter{#twitter-rules}

Puoi creare regole di flusso per estrarre contenuto da Twitter.

Crea regole Twitter basate su hashtag, parole chiave, @mentions o autore.

L’aggiunta di **[!UICONTROL Words]** e di **[!UICONTROL Username]** per la regola restituirà contenuto che include entrambe le voci.

>[!NOTE]
>
>Livefyre aderisce alle linee guida sui display di Twitter e i clienti sono responsabili del rispetto di queste linee guida. Per ulteriori informazioni, consulta la documentazione di Twitter sui [requisiti di visualizzazione](https://dev.twitter.com/terms/display-requirements).

Per creare regole Twitter per estrarre contenuto dai feed Twitter nell’app o nella cartella, puoi filtrare in base a:

* **[!UICONTROL Keywords]**
   * Inserisci **[!UICONTROL Keywords]** da includere o escludere dal flusso Twitter. Se si specificano i valori per i campi **[!UICONTROL Contains any of these words]** e **[!UICONTROL Does not contain any of these words]**, verranno restituiti i tweet contenenti il primo e non il secondo. È possibile immettere più valori per un singolo campo e restituisce risultati che contengono uno qualsiasi dei valori. Per utilizzare l’operatore booleano AND per cercare i tweet con due o più parole, utilizza due e commerciali (*&amp;&amp;*) per separare le due parole.
   * Ad esempio, l&#39;immissione di **[!UICONTROL Contains any of these words]** parole chiave Giants, Posey e **[!UICONTROL Does not contain any of these words]** parola chiave Dodger, restituirà tutti i tweet che includono la parola *Giants* o *Posey* e non includerà la parola *Dodger*.
Per cercare i tweet che includono sia le parole *Giants* che *Posey*, immetti &quot;Giants &amp; Posey&quot;. Questa funzione è supportata solo per i campi **[!UICONTROL Contains any of these words]** e **[!UICONTROL Does not contain any of these words]** nelle regole di Twitter.

* **[!UICONTROL Hashtags]**.
   * Inserisci **[!UICONTROL Hashtags]** da includere o escludere dal flusso Twitter. Specificando i valori sia per i campi **[!UICONTROL Contains any of these words]** che per **[!UICONTROL Does not contain any of these words]** verranno restituiti i tweet contenenti hashtag nel primo campo e non gli hashtag nel secondo. È possibile immettere più valori per un singolo campo. Il flusso restituisce risultati che contengono uno qualsiasi dei valori.

* **[!UICONTROL Usernames]**
   * Immettere **[!UICONTROL @mentions]** o **[!UICONTROL authors]** per effettuare il pull nel flusso o escludere dal flusso. Utilizza le caselle di controllo per definire se è necessario includere anche **[!UICONTROL Retweets]** o **[!UICONTROL replies]** degli autori selezionati.

   >[!NOTE]
   >
   >Puoi includere o escludere gli autori; non è possibile combinare questi due campi in un&#39;unica regola Twitter.

* **[!UICONTROL Minimum number of followers.]** Seleziona il numero minimo di follower che l&#39;utente deve avere per estrarre informazioni dai propri post.
* **[!UICONTROL Location]**

   * Immettere la posizione (città, codice postale, indirizzo o codice geografico nel formato latitudine/longitudine comune (+/- 90, +/- 180) ). Inizia a digitare una posizione per visualizzare un menu a discesa con i suggerimenti. Seleziona una posizione dal menu a discesa. La mappa mostra un perno di quella posizione. Regolare il dispositivo di scorrimento per selezionare un raggio da un miglio a 25 miglia per ogni posizione. Se non scegli un raggio, Livefyre sceglie automaticamente un valore predefinito di otto miglia.
   >[!NOTE]
   >
   >Per entrambi i campi, la distanza viene calcolata dal centro della posizione di input.

   * È possibile aggiungere più di una posizione e un raggio. Per eliminare una posizione, fai clic sulla X accanto al nome di una posizione nella casella.
   * Combina i campi **[!UICONTROL Is near this location]** e **[!UICONTROL Is not near this location]** per estrarre il contenuto nelle posizioni nel campo **[!UICONTROL Is near this location]** , ma non nelle vicinanze delle posizioni nel campo **[!UICONTROL Is not near this location]** .


* **[!UICONTROL Additional Filters]**
   * Utilizza filtri aggiuntivi per perfezionare ulteriormente la regola Twitter. Definisci se:
      * Includi **[!UICONTROL Replies]** nei tweet di destinazione (se il flusso diventa ad alta velocità, questa funzione verrà disabilitata automaticamente).
      * Includi tweet da **[!UICONTROL Verified Twitter accounts only.]**
      * Includi **[!UICONTROL All Content]**, **[!UICONTROL Vines Only]** o **[!UICONTROL Images Only.]**
      * Includi solo i tweet che provengono da account con il **[!UICONTROL Minimum number of followers]** selezionato (uno, 100, 500, 1000, 10.000 o 100.000).

Per ulteriori opzioni della regola Stream per tutte le regole Stream, vedere [Opzioni della regola Stream per tutte le regole Stream](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
