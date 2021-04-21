---
description: È possibile creare regole di flusso per estrarre contenuto dai feed RSS.
title: Regole RSS
exl-id: bfb3bbad-ab26-451e-b540-d6c41f54dc31
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Regole RSS{#rss-rules}

È possibile creare regole di flusso per estrarre contenuto dai feed RSS.

I flussi RSS si aggiornano ogni 5 minuti, cercando i contenuti che non esistono già in Livefyre dai primi 50 elementi del feed. Livefyre ignora tutti gli elementi oltre i primi 50 nel feed.

Per creare regole RSS per estrarre contenuto dai feed RSS nell&#39;app o nella cartella, è possibile filtrare in base a:

* **[!UICONTROL URL]** del feed RSS.
* **[!UICONTROL Include recent items.]** Se è impostato su:

   * **[!UICONTROL Enabled]**, Livefyre aggiunge al flusso i primi 50 elementi di contenuto nel feed, indipendentemente dalla data di pubblicazione.
   * **[!UICONTROL Disabled]**, Livefyre aggiunge al flusso i primi 50 elementi di contenuto nel feed con una data di pubblicazione corrispondente alla data di creazione della regola di flusso o successiva.

* **[!UICONTROL Extract post information from item link (when disabled, post information is extracted from XML).]** Estrarre informazioni dal collegamento dell&#39;elemento o dal codice XML.

**Regole RSS**

Livefyre analizza i feed RSS in base alle seguenti specifiche RSS:

* [RSS 2.0](https://en.wikipedia.org/wiki/RSS)
* [RSS contenuti multimediali](https://en.wikipedia.org/wiki/Media_RSS)
* [Feed Atom](https://validator.w3.org/feed/docs/atom.html)

Livefyre non legge i feed che non aderiscono a queste specifiche e il loro contenuto non verrà trascinato nel flusso. Utilizzare il servizio di convalida dei feed WC3 per controllare la sintassi del feed RSS e assicurarsi che sia valido.

Per ulteriori opzioni della regola Stream per tutte le regole Stream, vedere [Opzioni della regola Stream per tutte le regole Stream](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
