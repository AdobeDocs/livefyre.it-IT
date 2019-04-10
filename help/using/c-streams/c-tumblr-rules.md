---
description: Potete creare regole di streaming che estraggono il contenuto da Tumblr.
seo-description: Potete creare regole di streaming che estraggono il contenuto da
  Tumblr.
seo-title: Regole Tumblr
solution: Experience Manager
title: Regole Tumblr
uuid: fe 9601 ab-aa 5 e -48 c 6-a 5 bf -5543 c 179 cb 90
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Regole Tumblr{#tumblr-rules}

Potete creare regole di streaming che estraggono il contenuto da Tumblr.

Create regole Tumblr basate su un blog Tumblr e filtrate in base al tag. I flussi Tumblr vengono aggiornati ogni 5 minuti, ricercando contenuto che non esiste già in Livefyre dai primi 20 elementi del feed. Livefyre ignora tutti gli elementi oltre i primi 20 elementi del feed.

Per creare regole Tumblr per estrarre contenuto da Tumblr nell'app o nella cartella, puoi filtrare:

* **[!UICONTROL Blog]**

   * Inserite il **[!UICONTROL Blog Name]** blog per Tumblr. Inserite l'URL (*staff.tumblr.com*) o il nome del blog (*personale*).

   * Includete fino a uno **[!UICONTROL Tag]** per filtrare i risultati per post, incluso un determinato tag.

* **[!UICONTROL Include recent items.]** Se è impostato su:

   * **[!UICONTROL Enabled]**Livefyre aggiunge i primi 20 elementi contenuti nel feed al flusso, indipendentemente dalla data di pubblicazione.
   * **[!UICONTROL Disabled]**, Livefyre aggiunge i primi 20 elementi contenuti nel feed al flusso con una data di pubblicazione che è la stessa della data di creazione regola di flusso o successiva.

Per le opzioni di Regole di flusso aggiuntive per tutte le regole Flusso, consultate [Opzioni regola di flusso per tutte le regole dei flussi](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
