---
description: Queste opzioni si applicano a qualsiasi regola di flusso da tutte le
  reti social o da metodi di pubblicazione.
seo-description: Queste opzioni si applicano a qualsiasi regola di flusso da tutte
  le reti social o da metodi di pubblicazione.
seo-title: Opzioni regola di flusso per tutte le regole di flusso
solution: Experience Manager
title: Opzioni regola di flusso per tutte le regole di flusso
uuid: 4072 ee 83-31 e 7-4 de 6-918 c -134 b 8 b 8032 e 1
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Opzioni regola di flusso per tutte le regole di flusso{#stream-rule-options-for-all-stream-rules}

Queste opzioni si applicano a qualsiasi regola di flusso da tutte le reti social o da metodi di pubblicazione.

Funzioni di ricerca per campi testo e parole chiave:

* Quando immettete le parole chiave, Livefyre usa automaticamente l'operatore **booleano OR** per singole parole. Ad esempio, per cercare post con *la parola o* *la ricetta*, inserire *una torta*, quindi inserire *la ricetta* nel **[!UICONTROL keyword]** campo.

* Potete cercare frasi esatte racchiudendo tra virgolette il testo esatto della frase. Ad esempio, per cercare la ricetta *esatta della torta*, immettete *«torta»* nel **[!UICONTROL keyword]** campo.

* È possibile combinare le ricerche booleane e esatte in una regola di flusso. Ad esempio, potete cercare *una torta*, *una ricetta*e *una "ricetta"* immettendo ciascuna frase alla volta.

**[!UICONTROL Additional Filters]**:

* **[!UICONTROL Media]**. Selezionate una delle seguenti opzioni:

   * **[!UICONTROL All Content.]** Consente qualsiasi contenuto.
   * **[!UICONTROL Media Required.]** Consente solo il contenuto con immagini e video. (Per i contenuti Istagram e Facebook, potete specificare **[!UICONTROL Photos]** o **[!UICONTROL Videos]** solo).

* **[!UICONTROL Language]**. Scegliete la lingua in cui eseguire la ricerca. Inglese è la lingua predefinita.
* **[!UICONTROL Smart Tags]**. Scegliete i tag da usare per identificare il contenuto. Livefyre utilizza la tecnologia vision computer per identificare foto e video con tag avanzati specifici per rendere la ricerca più precisa. Utilizzate il **[!UICONTROL ANY]** modificatore per filtrare il contenuto nel flusso utilizzando qualsiasi tag o **[!UICONTROL ALL]** modificatore per filtrare il contenuto nel flusso che utilizza tutti i tag. Usate il **[!UICONTROL Image contains none of these smart tags]** campo per inserire tag per foto contenenti contenuto che non si desidera includere nel flusso. Questa opzione non funziona per il contenuto testo.

* **[!UICONTROL Products]**. Aggiungete tag di prodotto per far corrispondere la regola di flusso ai prodotti dal catalogo di prodotti.
* **[!UICONTROL Premoderate]**. Selezionate una delle seguenti opzioni:

   * **[!UICONTROL On]**. Consente di precaricare tutti i contenuti delle regole in arrivo. Puoi visualizzare il contenuto premoderato dalla sezione Streams di modq. **[!UICONTROL On]** sostituisce le impostazioni in Impostazioni app.
   * **[!UICONTROL Off]**. Non prestate molta attenzione al contenuto di regole in arrivo. **[!UICONTROL Off]** sostituisce le impostazioni in Impostazioni app.
   * **[!UICONTROL Inherited (Off)]**. Utilizzate le impostazioni premoderate del sito (sotto **[!UICONTROL Site Settings]**).

* **[!UICONTROL SAFE Rules]**. Selezionate una delle seguenti opzioni:
   * **[!UICONTROL Apply SAFE Rules]**. Applica tutte le regole SAFE a questo flusso.
   * **[!UICONTROL Apply SAFE Rules for:]** Selezionate una o più opzioni per applicare Regole SAFE per questa regola di flusso.
   * **[!UICONTROL Disable SAFE Rules]**. Non applicare nessuna Regola SAFE a questo flusso.

Per le opzioni Regole di flusso specifiche per una rete social o un tipo di contenuto, vedete la seguente documentazione per la rete social o il tipo di contenuto corrispondente:

* [Pagine Facebook](../c-streams/c-facebook-page-rules.md#c_facebook_page_rules)
* [E-mail](../c-streams/c-email-rules.md#c_email_rules)
* [Instagram](../c-streams/c-instagram-rules.md#c_instagram_rules)
* [Tumblr](../c-streams/c-tumblr-rules.md#c_tumblr_rules)
* [Twitter](../c-streams/c-twitter-rules.md#c_twitter_rules)
* [YouTube](../c-streams/c-youtube-rules/c-youtube-rules.md#c_youtube_rules)
* [RSS](../c-streams/c-rss-rules-streams.md#c_rss_rules_streams)
