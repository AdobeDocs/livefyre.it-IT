---
description: Puoi creare regole Stream che estraggono contenuto da Tumblr.
title: Regole Tumblr
exl-id: 5d49b266-6d1f-4ec2-8891-5e98fcab14a2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 0%

---

# Regole Tumblr{#tumblr-rules}

Puoi creare regole Stream che estraggono contenuto da Tumblr.

Crea regole Tumblr basate su un blog Tumblr e filtrate per tag. I flussi di Tumblr si aggiornano ogni 5 minuti, cercando contenuti che non esistono già in Livefyre dai primi 20 elementi del feed. Livefyre ignora tutti gli elementi oltre i primi 20 nel feed.

Per creare delle regole per spostare il contenuto da Tumblr all’app o alla cartella, puoi filtrare in base a:

* **[!UICONTROL Blog]**

   * Inserisci il **[!UICONTROL Blog Name]** per il blog Tumblr. Inserisci l&#39;URL (*staff.tumblr.com*) o il nome del blog (*staff*).

   * Includi fino a un **[!UICONTROL Tag]** per filtrare i risultati per post che includono un dato tag.

* **[!UICONTROL Include recent items.]** Se è impostato su:

   * **[!UICONTROL Enabled]**, Livefyre aggiunge al flusso i primi 20 elementi di contenuto nel feed, indipendentemente dalla data di pubblicazione.
   * **[!UICONTROL Disabled]**, Livefyre aggiunge al flusso i primi 20 elementi di contenuto nel feed con una data di pubblicazione corrispondente alla data di creazione della regola di flusso o successiva.

Per ulteriori opzioni della regola Stream per tutte le regole Stream, vedere [Opzioni della regola Stream per tutte le regole Stream](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
