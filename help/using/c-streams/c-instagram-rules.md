---
description: Puoi creare regole di flusso che richiamano il contenuto da Instagram.
seo-description: Puoi creare regole di flusso che richiamano il contenuto da Instagram.
seo-title: Regole Instagram
title: Regole Instagram
uuid: 98108ddb-5710-4331-891b-7e1bbb106059
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Regole Instagram{#instagram-rules}

Puoi creare regole di flusso che richiamano il contenuto da Instagram.

>[!NOTE]
>
>Prima di creare un flusso Instagram, è necessario aggiungere almeno un account aziendale Instagram alla **[!UICONTROL Social Accounts]** sezione in **[!UICONTROL Network Settings]**. Per ulteriori informazioni sulla configurazione di un account Instagram, consultate [Informazioni sugli account](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)Instagram.

Crea le regole di Instagram in base a @menzioni o hashtag.

>[!NOTE]
>
>Tutte le regole di Instagram richiedono almeno un hashtag. L'aggiunta di parole chiave e di un nome utente per la regola restituirà il contenuto che include entrambe le voci.

Per creare regole di Instagram per estrarre contenuto dai feed di Instagram nell'app o nella cartella, filtra per:

* **[!UICONTROL Words]**

   * Inserire **[!UICONTROL hashtags]** per essere incluso o escluso dal flusso di Instagram. Se si specificano valori sia per i campi **[!UICONTROL Contains]** che per quelli **[!UICONTROL Does not contain]** , verranno restituite immagini contenenti il primo e non il secondo.

   * Ad esempio, l'immissione di **[!UICONTROL Contains]** parole chiave Giants, Posey e **[!UICONTROL Does not contain]** parola chiave Dodger restituirà tutti i post che includono la parola Giants o Posey e non includeranno la parola Dodger.

      >[!NOTE]
      >
      >Instagram Rules restituisce i post che includono l’hashtag elencato nei commenti dell’autore, che potrebbero non essere visualizzati nel flusso.

* **[!UICONTROL Mentions]**

   * Immettere **[!UICONTROL @mentions]** per eseguire il pull nel flusso o escludere dal flusso.

* **[!UICONTROL Authors]**

   >[!NOTE]
   >
   >È necessario disporre di un account aziendale Instagram configurato in Livefyre per utilizzare la ricerca Author in una regola di flusso Instagram. Per ulteriori informazioni sulla configurazione di account aziendali Instagram in Livefyre, consultate [Informazioni sugli account](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)Instagram.

   * Immettere **[!UICONTROL @usernames]** per il pulling nel flusso. L'account associato al **@username** deve essere un account aziendale di Instagram.

   * Immettere **@usernames** per escludere dal flusso.

* **[!UICONTROL Additional Filters]**

   * Selezionare se si desidera includere **[!UICONTROL All Content]**, **[!UICONTROL Videos Only]** o **[!UICONTROL Photos Only]** nel flusso.

Per ulteriori opzioni della regola di flusso per tutte le regole di flusso, vedere Opzioni della regola di [flusso per tutte le regole](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)di flusso.
