---
description: Potete creare regole di streaming che estraggono il contenuto da Instagram.
seo-description: Potete creare regole di streaming che estraggono il contenuto da
  Instagram.
seo-title: Regole di Instagram
title: Regole di Instagram
uuid: 98108 ddb -5710-4331-891 b -7 e 1 bbb 106059
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Regole di Instagram{#instagram-rules}

Potete creare regole di streaming che estraggono il contenuto da Instagram.

>[!NOTE]
>
>Prima di creare un flusso di Instagram, è necessario aggiungere almeno un account business Istagram alla **[!UICONTROL Social Accounts]** sezione in **[!UICONTROL Network Settings]**. Per ulteriori informazioni su come configurare un account Instagram, consultate [Informazioni su Account Instagram](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

Create regole di Instagram in base a @ menzioni o hashtag.

>[!NOTE]
>
>Tutte le regole di Instagram richiedono almeno un hashtag. L'aggiunta di parole chiave e un nome utente per la regola restituiranno il contenuto che comprende entrambe le voci.

Per creare regole di Istagram per estrarre contenuto dai feed di Instagram nell'app o nella cartella, filtra:

* **[!UICONTROL Words]**

   * Inserisci **[!UICONTROL hashtags]** da includere o escludere dal flusso Instagram. Specificando i valori per i campi **[!UICONTROL Contains]** e **[!UICONTROL Does not contain]** i campi restituiranno le immagini che contengono la prima e non contengono la seconda.

   * Ad esempio, immettendo **[!UICONTROL Contains]** le parole chiave Giants, Posey e **[!UICONTROL Does not contain]** la parola chiave Dodger, tutti i post che includono la parola Giants o Posey non includono la parola Dodger.

      >[!NOTE]
      >
      >Le regole di Instagram restituiranno i post che includono l'hashtag elencato nei commenti dell'autore, che potrebbero non essere visualizzati nel flusso.

* **[!UICONTROL Mentions]**

   * Immetti **[!UICONTROL @mentions]** per inserire il flusso o escluderlo dallo streaming.

* **[!UICONTROL Authors]**

   >[!NOTE]
   >
   >In Livefyre è necessario disporre di un account aziendale Instagram per utilizzare la ricerca Autore in una regola Flusso di istagram. Per ulteriori informazioni sulla configurazione degli account business di Instagram in Livefyre, consultate [Informazioni sull'account di Instagram](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

   * Inserisci **[!UICONTROL @usernames]** per inserire il flusso. L'account associato al **nome @ username** deve essere un account business di Instagram.

   * Immettete i **@ username** da escludere dal flusso.

* **[!UICONTROL Additional Filters]**

   * Selezionate se desiderate includere **[!UICONTROL All Content]**, **[!UICONTROL Videos Only]**o **[!UICONTROL Photos Only]** nel flusso.

Per le opzioni di Regole di flusso aggiuntive per tutte le regole Flusso, consultate [Opzioni regola di flusso per tutte le regole dei flussi](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
