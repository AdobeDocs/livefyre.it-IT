---
description: Queste opzioni si applicano a qualsiasi regola di flusso da tutti i social network o metodi di pubblicazione.
seo-description: Queste opzioni si applicano a qualsiasi regola di flusso da tutti i social network o metodi di pubblicazione.
seo-title: Opzioni regola di flusso per tutte le regole di flusso
solution: Experience Manager
title: Opzioni regola di flusso per tutte le regole di flusso
uuid: 4072ee83-31e7-4de6-918c-134b8b8032e1
translation-type: tm+mt
source-git-commit: 8bdb537b38d78dba033d6671b710c2a61934d6b2
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---


# Opzioni regola di flusso per tutte le regole di flusso{#stream-rule-options-for-all-stream-rules}

Queste opzioni si applicano a qualsiasi regola di flusso da tutti i social network o metodi di pubblicazione.

Funzioni di ricerca per campi di testo e parole chiave:

* Quando si immettono le parole chiave, Livefyre utilizza automaticamente l&#39;operatore booleano **OR** per le singole parole. Ad esempio, per cercare post con la parola *torta* o *ricetta*, immettete *torta*, quindi immettete *recipe* nel campo **[!UICONTROL keyword]**.

* Potete cercare frasi esatte racchiudendo tra virgolette il testo esatto della frase. Ad esempio, per cercare la frase esatta *torta recipe*, immettere *&quot;torta recipe&quot;* nel campo **[!UICONTROL keyword]**.

* È possibile combinare le ricerche di frasi booleane e esatte in un&#39;unica regola di flusso. Ad esempio, è possibile cercare *torta*, *ricetta* e *&quot;torta recipe&quot;* inserendo ciascuna frase uno alla volta.

**[!UICONTROL Additional Filters]**:

* **[!UICONTROL Media]**. Selezionate una delle seguenti opzioni:

   * **[!UICONTROL All Content.]** Consente qualsiasi contenuto.
   * **[!UICONTROL Media Required.]** Consente solo il contenuto con immagini e video. (Per i contenuti Instagram e Facebook, potete specificare solo **[!UICONTROL Photos]** o **[!UICONTROL Videos]**).

* **[!UICONTROL Language]**. Scegliete la lingua in cui effettuare la ricerca. L&#39;inglese è la lingua predefinita.
* **[!UICONTROL Smart Tags]**. Scegliete i tag da utilizzare per identificare il contenuto. Livefyre utilizza la tecnologia per la visione computerizzata per identificare foto e video con smart tag specifici per rendere la ricerca più precisa. Utilizzate il modificatore **[!UICONTROL ANY]** per filtrare il contenuto nel flusso utilizzando qualsiasi tag o il modificatore **[!UICONTROL ALL]** per filtrare il contenuto nel flusso che utilizza tutti i tag. Utilizzate il campo **[!UICONTROL Image contains none of these smart tags]** per inserire i tag per le foto che contengono il contenuto che non desiderate inserire nel flusso. Questa opzione non funziona per il contenuto di testo.

* **[!UICONTROL Products]**. Aggiungi tag di prodotto per far corrispondere la regola di flusso ai prodotti del catalogo di prodotti.
* **[!UICONTROL Premoderate]**. Selezionate una delle seguenti opzioni:

   * **[!UICONTROL On]**. Premoderare tutto il contenuto della regola in entrata. Potete visualizzare il contenuto predefinito dalla sezione Streams di ModQ. **[!UICONTROL On]** sostituisce le impostazioni in Impostazioni app.
   * **[!UICONTROL Off]**. Non premoderare il contenuto delle regole in entrata. **[!UICONTROL Off]** sostituisce le impostazioni in Impostazioni app.
   * **[!UICONTROL Inherited (Off)]**. Utilizzate le impostazioni predefinite dal sito (in **[!UICONTROL Site Settings]**).

* **[!UICONTROL SAFE Rules]**. Selezionate una delle seguenti opzioni:
   * **[!UICONTROL Apply SAFE Rules]**. Applica tutte le regole SAFE a questo flusso.
   * **[!UICONTROL Apply SAFE Rules for:]** Selezionare una o più opzioni per applicare le regole SICUREZZA per questa regola di flusso.
   * **[!UICONTROL Disable SAFE Rules]**. Non applicare regole SICURE a questo flusso.

Per le opzioni della regola Flusso specifiche per un social network o un tipo di contenuto, consultate la seguente documentazione per il rispettivo tipo di contenuto o social network:

* [Pagine Facebook](../c-streams/c-facebook-page-rules.md#c_facebook_page_rules)
* [E-mail](../c-streams/c-email-rules.md#c_email_rules)
* [Instagram](../c-streams/c-instagram-rules.md#c_instagram_rules)
* [Tumblr](../c-streams/c-tumblr-rules.md#c_tumblr_rules)
* [Twitter](../c-streams/c-twitter-rules.md#c_twitter_rules)
* [YouTube](../c-streams/c-youtube-rules/c-youtube-rules.md#c_youtube_rules)
* [RSS](../c-streams/c-rss-rules-streams.md#c_rss_rules_streams)
