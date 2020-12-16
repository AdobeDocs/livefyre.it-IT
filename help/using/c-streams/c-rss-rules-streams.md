---
description: Potete creare regole di flusso per il pulling del contenuto dai feed RSS.
seo-description: Potete creare regole di flusso per il pulling del contenuto dai feed RSS.
seo-title: Regole RSS
solution: Experience Manager
title: Regole RSS
uuid: 3c9e2069-bb85-41dc-8b35-6237642a538a
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---


# Regole RSS{#rss-rules}

Potete creare regole di flusso per il pulling del contenuto dai feed RSS.

I flussi RSS si aggiornano ogni 5 minuti, cercando il contenuto che non esiste già in Livefyre dai primi 50 elementi del feed. Livefyre ignora tutti gli elementi oltre i primi 50 nel feed.

Per creare delle regole RSS per estrarre il contenuto dai feed RSS nell&#39;app o nella cartella, potete filtrare in base a:

* **[!UICONTROL URL]** del feed RSS.
* **[!UICONTROL Include recent items.]** Se impostato su:

   * **[!UICONTROL Enabled]**, Livefyre aggiunge al flusso i primi 50 elementi di contenuto del feed, indipendentemente dalla data di pubblicazione.
   * **[!UICONTROL Disabled]**, Livefyre aggiunge i primi 50 elementi di contenuto nel feed al flusso con una data di pubblicazione che corrisponde alla data di creazione della regola del flusso o a una data successiva.

* **[!UICONTROL Extract post information from item link (when disabled, post information is extracted from XML).]** Estrarre informazioni dal collegamento dell&#39;elemento o dal codice XML.

**Regole RSS**

Livefyre analizza i feed RSS in base alle seguenti specifiche RSS:

* [RSS 2.0](https://en.wikipedia.org/wiki/RSS)
* [RSS multimediale](https://en.wikipedia.org/wiki/Media_RSS)
* [Feed Atom](https://validator.w3.org/feed/docs/atom.html)

Livefyre non legge i feed che non aderiscono a queste specifiche, e il loro contenuto non verrà estratto nel flusso. Utilizzate il servizio di convalida feed WC3 per verificare la sintassi del feed RSS e verificare che sia valido.

Per ulteriori opzioni della regola di flusso per tutte le regole di flusso, vedere [Opzioni regola di flusso per tutte le regole di flusso](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
