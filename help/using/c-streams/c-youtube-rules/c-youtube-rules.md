---
description: Puoi creare regole di flusso che richiamano il contenuto dalle regole di YouTube.
seo-description: Puoi creare regole di flusso che richiamano il contenuto dalle regole di YouTube.
seo-title: Regole YouTube
solution: Experience Manager
title: Regole YouTube
uuid: ec6a3780-7119-45c3-8ab2-fb0f9803d161
translation-type: tm+mt
source-git-commit: 30aa5cce5e7567208362cc35caeb7b7260c42f3b

---


# Regole YouTube {#youtube-rules}

Puoi creare regole di flusso che richiamano il contenuto dalle regole di YouTube.

Creare regole YouTube basate su Utente, Canale o Playlist.

Per creare delle regole di YouTube per estrarre il contenuto da YouTube nell'app o nella cartella, puoi filtrare in base a:

* **[!UICONTROL User]**
   * Immettete la stringa vuota per **[!UICONTROL User]** includere nel flusso i video dell’utente.
   * Ad esempio, se l’URL del feed utente che desiderate inserire è `https://www.youtube.com/user/livefyresupport`, è sufficiente immettere `livefyresupport`.

* **[!UICONTROL Channel]**
   * Immettete la stringa vuota per **[!UICONTROL Channel]** includere nel flusso i video provenienti da un canale.
   * Ad esempio, se l’URL del feed canale che desiderate inserire è `https://www.youtube.com/channel/UCeNZlh03MyUkjRlLFpVQxsg`, è sufficiente immettere `UCeNZlh03MyUkjRlLFpVQxsg`.

* **[!UICONTROL Playlist]**
   * Immettete la stringa vuota per **[!UICONTROL Playlist]** includere i video di una sequenza di riproduzione nel flusso.
   * Ad esempio, se l'URL del feed della sequenza di riproduzione che si desidera inserire è `https://www.youtube.com/playlist?list=PLFE5670C92BDAC201`, è sufficiente immettere `PLFE5670C92BDAC201`

* **[!UICONTROL Include recent items.]** Se impostato su:
   * **[!UICONTROL Enabled]**, Livefyre aggiunge al flusso i primi 15 elementi di contenuto del feed, indipendentemente dalla data di pubblicazione.
   * **[!UICONTROL Disabled]**, Livefyre aggiunge i primi 15 elementi di contenuto nel feed al flusso con una data di pubblicazione che corrisponde alla data di creazione della regola del flusso o a una data successiva.

Per ulteriori opzioni della regola di flusso per tutte le regole di flusso, vedere Opzioni della regola di [flusso per tutte le regole](../../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)di flusso.
