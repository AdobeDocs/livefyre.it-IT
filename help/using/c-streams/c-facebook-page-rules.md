---
description: Potete creare regole di flusso per estrarre il contenuto dalle pagine di Facebook.
seo-description: Potete creare regole di flusso per estrarre il contenuto dalle pagine di Facebook.
seo-title: Regole pagina Facebook
solution: Experience Manager
title: Regole pagina Facebook
uuid: 2be63476-1a92-409d-a22f-e1ec66b6dcc8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Regole pagina Facebook{#facebook-page-rules}

Potete creare regole di flusso per estrarre il contenuto dalle pagine di Facebook.

Potete utilizzare le regole della pagina Facebook per trasmettere in streaming i contenuti pubblicati pubblicamente dalle pagine Facebook. Il contenuto verrà inserito nell'app o nella cartella con la stessa frequenza di SocialSync, che cambia in base ai pattern di traffico della pagina Facebook e dei post. Sono supportati anche i collegamenti all’interno delle pagine Facebook, che verranno visualizzati nel flusso.

Per creare delle regole di pagina Facebook per estrarre il contenuto dalle pagine Facebook nell'app o nella cartella, potete filtrare in base a:

* **[!UICONTROL Facebook Page]**

   * Immettere il nome **[!UICONTROL Name]** della pagina. Immettere solo il testo finale per l'URL. **** Ad esempio: Per aggiungere contenuto da `https://facebook.com/KellysSuperFunFanPage`, digitare *KellysSuperFunFanPage* nel **[!UICONTROL Name]** campo.

   * Attivate questa opzione **[!UICONTROL Include Facebook Comments for each post]** se desiderate includere i commenti degli utenti ai post della pagina.
   * Attivate questa opzione **[!UICONTROL Only Show Author Posts]** se desiderate escludere i post da altri utenti.

Per ulteriori opzioni della regola di flusso per tutte le regole di flusso, vedere Opzioni della regola di [flusso per tutte le regole](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)di flusso.

>[!NOTE]
>
>Livefyre è limitato ai contenuti ricevuti da Facebook e pertanto non è in grado di garantire che ogni post su una pagina Facebook venga incluso nel flusso di lavoro.

>[!NOTE]
>
>Se SocialSync di Facebook e una regola di pagina Facebook sono entrambi abilitati per una pagina Facebook specifica e i commenti degli utenti sono abilitati per la Regola pagina Facebook, la Regola flusso sovrascrive SocialSync. Il contenuto verrà trasmesso in streaming nell'app in base solo alla regola Cura pagina Facebook e non utilizzando SocialSync.

I tipi di contenuto supportati da Facebook Page Curate includono:

* Proprietario pagina o amministratore

   * Stato
   * Foto
   * Video come collegamenti

* Utente Facebook standard

   * Stato
   * Foto
   * Video come collegamenti

* Terzi

   * Stato

