---
description: Puoi creare regole di streaming che estraggono il contenuto dalle regole
  di YouTube.
seo-description: Puoi creare regole di streaming che estraggono il contenuto dalle
  regole di YouTube.
seo-title: Regole YouTube
solution: Experience Manager
title: Regole YouTube
uuid: ec 6 a 3780-7119-45 c 3-8 ab 2-fb 0 f 9803 d 161
translation-type: tm+mt
source-git-commit: 30aa5cce5e7567208362cc35caeb7b7260c42f3b

---


# Regole YouTube {#youtube-rules}

Puoi creare regole di streaming che estraggono il contenuto dalle regole di YouTube.

Crea regole YouTube basate su Utente, Canale o Playlist.

Per creare regole YouTube per estrarre contenuto da YouTube nell'app o nella cartella, puoi filtrare:

* **[!UICONTROL User]**
   * Immettete la stringa personalizzata per includere **[!UICONTROL User]** i video dall'utente nel flusso.
   * Ad esempio, se l'URL del feed utente che desiderate inserire è `https://www.youtube.com/user/livefyresupport`, immettete `livefyresupport`semplicemente.

* **[!UICONTROL Channel]**
   * Immettete la stringa personalizzata per includere **[!UICONTROL Channel]** i video da un canale nel flusso.
   * Ad esempio, se l'URL del feed canale che desideri inserire è `https://www.youtube.com/channel/UCeNZlh03MyUkjRlLFpVQxsg`, immetti `UCeNZlh03MyUkjRlLFpVQxsg`semplicemente.

* **[!UICONTROL Playlist]**
   * Immettete la stringa personalizzata per includere **[!UICONTROL Playlist]** i video da una sequenza brani nel flusso.
   * Ad esempio, se l'URL del feed Playlist da inserire è `https://www.youtube.com/playlist?list=PLFE5670C92BDAC201`, immetti semplicemente `PLFE5670C92BDAC201`

* **[!UICONTROL Include recent items.]** Se è impostato su:
   * **[!UICONTROL Enabled]**Livefyre aggiunge i primi 15 elementi contenuti nel feed al flusso, indipendentemente dalla data di pubblicazione.
   * **[!UICONTROL Disabled]**, Livefyre aggiunge i primi 15 elementi contenuti nel feed al flusso con una data di pubblicazione che è la stessa della data di creazione regola di flusso o successiva.

Per le opzioni di Regole di flusso aggiuntive per tutte le regole Flusso, consultate [Opzioni regola di flusso per tutte le regole dei flussi](../../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
