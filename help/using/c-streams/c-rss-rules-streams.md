---
description: Potete creare regole di streaming che estraggono il contenuto dai feed
  RSS.
seo-description: Potete creare regole di streaming che estraggono il contenuto dai
  feed RSS.
seo-title: Regole RSS
solution: Experience Manager
title: Regole RSS
uuid: 3 c 9 e 2069-bb 85-41 dc -8 b 35-6237642 a 538 a
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Regole RSS{#rss-rules}

Potete creare regole di streaming che estraggono il contenuto dai feed RSS.

I flussi RSS vengono aggiornati ogni 5 minuti, ricercando contenuto che non esiste già in Livefyre dai primi 50 elementi del feed. Livefyre ignora tutti gli elementi oltre i primi 50 elementi del feed.

Per creare regole RSS per l'inserimento di contenuto da feed RSS nell'app o nella cartella, potete filtrare:

* **[!UICONTROL URL]** del feed RSS.
* **[!UICONTROL Include recent items.]** Se è impostato su:

   * **[!UICONTROL Enabled]**Livefyre aggiunge i primi 50 elementi contenuti nel feed al flusso, indipendentemente dalla data di pubblicazione.
   * **[!UICONTROL Disabled]**, Livefyre aggiunge i primi 50 elementi contenuti nel feed al flusso con una data di pubblicazione che è la stessa della data di creazione regola di flusso o successiva.

* **[!UICONTROL Extract post information from item link (when disabled, post information is extracted from XML).]** Estraete le informazioni dal collegamento dell'elemento o dal codice XML.

**Regole RSS**

Livefyre analizza i feed RSS in base alle seguenti specifiche RSS:

* [RSS 2.0](https://en.wikipedia.org/wiki/RSS)
* [RSS multimediale](https://en.wikipedia.org/wiki/Media_RSS)
* [Atom, feed](https://validator.w3.org/feed/docs/atom.html)

Livefyre non legge i feed che non aderiscono a queste specifiche e il loro contenuto non verrà introdotto nel flusso. Utilizzare WC 3 Feed Validation Service per controllare la sintassi del feed RSS e assicurarsi che sia valido.

Per le opzioni di Regole di flusso aggiuntive per tutte le regole Flusso, consultate [Opzioni regola di flusso per tutte le regole dei flussi](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
