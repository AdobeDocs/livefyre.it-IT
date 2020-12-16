---
description: Puoi creare regole di flusso per il pulling del contenuto da Tumblr.
seo-description: Puoi creare regole di flusso per il pulling del contenuto da Tumblr.
seo-title: Regole Tumblr
solution: Experience Manager
title: Regole Tumblr
uuid: fe9601ab-aa5e-48c6-a5bf-5543c179cb90
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---


# Regole di tumblr{#tumblr-rules}

Puoi creare regole di flusso per il pulling del contenuto da Tumblr.

Create regole Tumblr basate su un blog di Tumblr e filtrate per tag. I flussi Tumblr si aggiornano ogni 5 minuti, cercando il contenuto che non esiste già in Livefyre dai primi 20 elementi del feed. Livefyre ignora tutti gli elementi oltre i primi 20 nel feed.

Per creare delle regole per i tag per estrarre il contenuto da Tumblr nell’app o nella cartella, potete filtrare in base a:

* **[!UICONTROL Blog]**

   * Digitate **[!UICONTROL Blog Name]** per il blog di Tumblr. Inserite l&#39;URL (*staff.tumblr.com*) o il nome del blog (*staff*).

   * Includete fino a un **[!UICONTROL Tag]** per filtrare i risultati per post che includono un tag specifico.

* **[!UICONTROL Include recent items.]** Se impostato su:

   * **[!UICONTROL Enabled]**, Livefyre aggiunge al flusso i primi 20 elementi di contenuto del feed, indipendentemente dalla data di pubblicazione.
   * **[!UICONTROL Disabled]**, Livefyre aggiunge i primi 20 elementi di contenuto nel feed al flusso con una data di pubblicazione che corrisponde alla data di creazione della regola del flusso o a una data successiva.

Per ulteriori opzioni della regola di flusso per tutte le regole di flusso, vedere [Opzioni regola di flusso per tutte le regole di flusso](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
