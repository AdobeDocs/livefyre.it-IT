---
description: Queste opzioni si applicano a qualsiasi regola di flusso da tutti i social network o metodi di pubblicazione.
title: Opzioni della regola di flusso per tutte le regole di flusso
exl-id: eff1a3cb-395f-4eb1-be93-f0f09bba95e2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 1%

---

# Opzioni regola di flusso per tutte le regole di flusso{#stream-rule-options-for-all-stream-rules}

Queste opzioni si applicano a qualsiasi regola di flusso da tutti i social network o metodi di pubblicazione.

Funzioni di ricerca per campi di testo e parole chiave:

* Quando si immettono le parole chiave, Livefyre utilizza automaticamente l&#39;operatore booleano **OR** quando si tratta di singole parole. Ad esempio, per cercare post con la parola *cake* o *recipe*, immetti *cake*, quindi immetti *recipe* nel campo **[!UICONTROL keyword]** .

* È possibile cercare frasi esatte circondando l&#39;esatto testo della frase tra virgolette. Ad esempio, per cercare la frase esatta *ricetta torta*, immetti *&quot;ricetta torta&quot;* nel campo **[!UICONTROL keyword]**.

* È possibile combinare le ricerche booleane ed esatte delle frasi in una regola di flusso. Ad esempio, è possibile cercare *cake*, *recipe* e *&quot;cake recipe&quot;* inserendo ciascuna frase una alla volta.

**[!UICONTROL Additional Filters]**:

* **[!UICONTROL Media]**. Selezionare una delle seguenti opzioni:

   * **[!UICONTROL All Content.]** Consenti qualsiasi contenuto.
   * **[!UICONTROL Media Required.]** Consenti solo contenuti con immagini e video. (Per i contenuti Instagram e Facebook, puoi specificare solo **[!UICONTROL Photos]** o **[!UICONTROL Videos]** ).

* **[!UICONTROL Language]**. Scegli la lingua in cui eseguire la ricerca. L’inglese è la lingua predefinita.
* **[!UICONTROL Smart Tags]**. Scegli i tag da utilizzare per identificare il contenuto. Livefyre utilizza la tecnologia di visione computerizzata per identificare foto e video con tag avanzati specifici per rendere più precisa questa ricerca. Utilizza il modificatore **[!UICONTROL ANY]** per filtrare il contenuto nel flusso utilizzando un tag qualsiasi o il modificatore **[!UICONTROL ALL]** per filtrare il contenuto nel flusso che utilizza tutti i tag. Usa il campo **[!UICONTROL Image contains none of these smart tags]** per inserire tag per le foto contenenti contenuto non desiderato nel flusso. Questa opzione non funziona per il contenuto di testo.

* **[!UICONTROL Products]**. Aggiungi tag di prodotto per far corrispondere la regola di flusso con i prodotti del catalogo di prodotto.
* **[!UICONTROL Premoderate]**. Selezionare una delle seguenti opzioni:

   * **[!UICONTROL On]**. Premodera tutto il contenuto della regola in entrata. È possibile visualizzare contenuti premoderati dalla sezione Streams di ModQ. **[!UICONTROL On]** sostituisce le impostazioni in Impostazioni app.
   * **[!UICONTROL Off]**. Non moderare alcun contenuto della regola in arrivo. **[!UICONTROL Off]** sostituisce le impostazioni in Impostazioni app.
   * **[!UICONTROL Inherited (Off)]**. Utilizza le impostazioni predefinite del sito (in **[!UICONTROL Site Settings]**).

* **[!UICONTROL SAFE Rules]**. Selezionare una delle seguenti opzioni:
   * **[!UICONTROL Apply SAFE Rules]**. Applica tutte le regole SAFE a questo flusso.
   * **[!UICONTROL Apply SAFE Rules for:]** Selezionare una o più opzioni per applicare le regole SAFE per questa regola di flusso.
   * **[!UICONTROL Disable SAFE Rules]**. Non applicare regole SICURE a questo flusso.

Per le opzioni della regola Stream specifiche per un social network o un tipo di contenuto, consulta la documentazione seguente per il rispettivo social network o tipo di contenuto:

* [Pagine facebook](../c-streams/c-facebook-page-rules.md#c_facebook_page_rules)
* [E-mail](../c-streams/c-email-rules.md#c_email_rules)
* [Instagram](../c-streams/c-instagram-rules.md#c_instagram_rules)
* [Tumblr](../c-streams/c-tumblr-rules.md#c_tumblr_rules)
* [Twitter](../c-streams/c-twitter-rules.md#c_twitter_rules)
* [YouTube](../c-streams/c-youtube-rules/c-youtube-rules.md#c_youtube_rules)
* [RSS](../c-streams/c-rss-rules-streams.md#c_rss_rules_streams)
