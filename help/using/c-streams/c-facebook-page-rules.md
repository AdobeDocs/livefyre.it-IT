---
description: Puoi creare regole di flusso per estrarre contenuto dalle pagine Facebook.
title: Regole pagina facebook
exl-id: 1dc728c6-81fa-4c6c-acba-d9a4aea71ed2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 1%

---

# Regole pagina facebook{#facebook-page-rules}

Puoi creare regole di flusso per estrarre contenuto dalle pagine Facebook.

Puoi utilizzare le Regole pagina di Facebook per lo streaming dei contenuti pubblicati pubblicamente dalle Pagine Facebook. Il contenuto verrà trascinato nell’app o nella cartella con la stessa frequenza di SocialSync, che cambia in base ai pattern di traffico della pagina e del post di Facebook. Sono supportati anche i collegamenti all’interno delle pagine Facebook e verranno visualizzati nel flusso.

Per creare regole di pagina Facebook per estrarre contenuto dalle pagine Facebook nell’app o nella cartella, puoi filtrare in base a:

* **[!UICONTROL Facebook Page]**

   * Inserisci il **[!UICONTROL Name]** per la pagina. Immetti solo il testo finale per l’URL. **Ad esempio:** per aggiungere contenuto da  `https://facebook.com/KellysSuperFunFanPage`, digita  ** KellysSuperFunFanPagine nel  **[!UICONTROL Name]** campo .

   * Passa a **[!UICONTROL Include Facebook Comments for each post]** se desideri includere commenti degli utenti nei post di Page.
   * Passa a **[!UICONTROL Only Show Author Posts]** se desideri escludere i post da altri utenti.

Per ulteriori opzioni della regola Stream per tutte le regole Stream, vedere [Opzioni della regola Stream per tutte le regole Stream](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

>[!NOTE]
>
>Livefyre è limitato ai contenuti ricevuti da Facebook e pertanto non è in grado di garantire che ogni post su una pagina Facebook venga incluso nel flusso.

>[!NOTE]
>
>Se Facebook SocialSync e una regola di pagina Facebook sono entrambi abilitati per una pagina Facebook specifica e i commenti degli utenti sono abilitati per la regola di pagina Facebook, la regola di flusso sovrascriverà SocialSync. Il contenuto verrà inviato in streaming nell’app in base solo alla regola di cura della pagina di Facebook e non utilizzando SocialSync.

I tipi di contenuto supportati da Facebook Page Curate includono:

* Proprietario o amministratore della pagina

   * Stato
   * Foto
   * Video come collegamenti

* Utente Facebook standard

   * Stato
   * Foto
   * Video come collegamenti

* Terzi

   * Stato
