---
description: Puoi creare regole di streaming che estraggono il contenuto da Facebook
  Pages.
seo-description: Puoi creare regole di streaming che estraggono il contenuto da Facebook
  Pages.
seo-title: Regole pagina Facebook
solution: Experience Manager
title: Regole pagina Facebook
uuid: 2 be 63476-1 a 92-409 d-a 22 f-e 1 ec 66 b 6 dcc 8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Regole pagina Facebook{#facebook-page-rules}

Puoi creare regole di streaming che estraggono il contenuto da Facebook Pages.

Potete utilizzare le regole di pagina Facebook per trasmettere il contenuto pubblicato pubblicamente da Facebook Pages. Il contenuto verrà introdotto nell'app o nella cartella alla stessa frequenza di socialsync, che si basa sui pattern di pagina Facebook e post. Sono inoltre supportati i collegamenti all'interno delle pagine Facebook, che verranno visualizzati nel flusso.

Per creare regole di pagina Facebook per il pull del contenuto dalle pagine Facebook nell'app o nella cartella, potete filtrare per:

* **[!UICONTROL Facebook Page]**

   * Immettete la **[!UICONTROL Name]** pagina. Immettere solo il testo finale per l'URL. **Ad esempio:** Per aggiungere contenuto, `https://facebook.com/KellysSuperFunFanPage`digitate *kellyssuperfunfanpage* nel **[!UICONTROL Name]** campo.

   * Attivate questa opzione se **[!UICONTROL Include Facebook Comments for each post]** desiderate includere i commenti degli utenti in Post pagina.
   * Attivate **[!UICONTROL Only Show Author Posts]** questa opzione per escludere i post da altri utenti.

Per le opzioni di Regole di flusso aggiuntive per tutte le regole Flusso, consultate [Opzioni regola di flusso per tutte le regole dei flussi](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

>[!NOTE]
>
>Livefyre è limitato al contenuto ricevuto da Facebook e pertanto non è in grado di garantire che ogni post su una pagina Facebook venga incluso nel flusso.

>[!NOTE]
>
>Se Facebook socialsync e una Regola di pagina Facebook sono entrambi abilitati per una pagina Facebook specifica e i commenti utente sono abilitati per la Regola di pagina Facebook, la regola Flusso sostituirà socialsync. Il contenuto verrà trasmesso in streaming nell'app solo in base alla Regola di cura pagina Facebook e non tramite socialsync.

I tipi di contenuto supportati da Curate pagina Facebook includono:

* Proprietario pagina o Amministratore

   * Stato
   * Foto
   * Video come collegamenti

* Utente Facebook standard

   * Stato
   * Foto
   * Video come collegamenti

* Terze parti

   * Stato

