---
description: Puoi creare regole di flusso per estrarre contenuto dalle regole di YouTube.
title: Regole di YouTube
exl-id: 720a6fc6-d5de-4c78-a14e-51bced6e8dda
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---

# Regole YouTube {#youtube-rules}

Puoi creare regole di flusso per estrarre contenuto dalle regole di YouTube.

Crea regole YouTube in base a Utente, Canale o Playlist.

Per creare regole YouTube per estrarre contenuto da YouTube nell’app o nella cartella, puoi filtrare in base a:

* **[!UICONTROL User]**
   * Immetti la stringa di reindirizzamento per un **[!UICONTROL User]** per includere i video dell&#39;utente nel flusso.
   * Ad esempio, se l’URL del feed utente che si desidera inserire è `https://www.youtube.com/user/livefyresupport`, è sufficiente inserire `livefyresupport`.

* **[!UICONTROL Channel]**
   * Immetti la stringa di reindirizzamento per un **[!UICONTROL Channel]** per includere i video da un canale nel flusso.
   * Ad esempio, se l’URL del feed canale che desideri inserire è `https://www.youtube.com/channel/UCeNZlh03MyUkjRlLFpVQxsg`, è sufficiente inserire `UCeNZlh03MyUkjRlLFpVQxsg`.

* **[!UICONTROL Playlist]**
   * Immetti la stringa di reindirizzamento per un **[!UICONTROL Playlist]** per includere video da una sequenza di riproduzione nel flusso.
   * Ad esempio, se l&#39;URL del feed della sequenza di riproduzione che si desidera inserire è `https://www.youtube.com/playlist?list=PLFE5670C92BDAC201`, è sufficiente inserire `PLFE5670C92BDAC201`

* **[!UICONTROL Include recent items.]** Se è impostato su:
   * **[!UICONTROL Enabled]**, Livefyre aggiunge al flusso i primi 15 elementi di contenuto nel feed, indipendentemente dalla data di pubblicazione.
   * **[!UICONTROL Disabled]**, Livefyre aggiunge al flusso i primi 15 elementi di contenuto nel feed con una data di pubblicazione corrispondente alla data di creazione della regola del flusso o successiva.

Per ulteriori opzioni della regola Stream per tutte le regole Stream, vedere [Opzioni della regola Stream per tutte le regole Stream](../../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
