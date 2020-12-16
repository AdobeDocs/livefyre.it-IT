---
description: Puoi creare regole di flusso che richiamano il contenuto da Instagram.
seo-description: Puoi creare regole di flusso che richiamano il contenuto da Instagram.
seo-title: Regole Instagram
title: Regole Instagram
uuid: 98108ddb-5710-4331-891b-7e1bbb106059
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---


# Regole Instagram{#instagram-rules}

Puoi creare regole di flusso che richiamano il contenuto da Instagram.

>[!NOTE]
>
>Prima di creare un flusso Instagram, è necessario aggiungere almeno un account aziendale Instagram alla sezione **[!UICONTROL Social Accounts]** in **[!UICONTROL Network Settings]**. Per ulteriori informazioni sulla configurazione di un account Instagram, vedere [Informazioni su account Instagram](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

Crea le regole di Instagram in base a @menzioni o hashtag.

>[!NOTE]
>
>Tutte le regole di Instagram richiedono almeno un hashtag. L&#39;aggiunta di parole chiave e di un nome utente per la regola restituirà il contenuto che include entrambe le voci.

Per creare regole di Instagram per estrarre contenuto dai feed di Instagram nell&#39;app o nella cartella, filtra per:

* **[!UICONTROL Words]**

   * Immettere **[!UICONTROL hashtags]** per essere incluso o escluso dal flusso di Instagram. Se si specificano valori per i campi **[!UICONTROL Contains]** e **[!UICONTROL Does not contain]**, verranno restituite immagini che contengono il primo e non il secondo.

   * Ad esempio, immettendo **[!UICONTROL Contains]** parole chiave Giants, Posey e **[!UICONTROL Does not contain]** parola chiave Dodger, verranno restituiti tutti i post che includono la parola Giants o Posey e non la parola Dodger.

      >[!NOTE]
      >
      >Instagram Rules restituisce i post che includono l’hashtag elencato nei commenti dell’autore, che potrebbero non essere visualizzati nel flusso.

* **[!UICONTROL Mentions]**

   * Immettere **[!UICONTROL @mentions]** per eseguire il pull nel flusso o escludere dal flusso.

* **[!UICONTROL Authors]**

   >[!NOTE]
   >
   >È necessario disporre di un account aziendale Instagram configurato in Livefyre per utilizzare la ricerca Author in una regola di flusso Instagram. Per ulteriori informazioni sulla configurazione di account aziendali Instagram in Livefyre, vedere [Informazioni su account Instagram](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

   * Immettere **[!UICONTROL @usernames]** per eseguire il pull nel flusso. L&#39;account associato al **@username** deve essere un account aziendale di Instagram.

   * Immettere **@usernames** per escludere dal flusso.

* **[!UICONTROL Additional Filters]**

   * Selezionare se si desidera includere **[!UICONTROL All Content]**, **[!UICONTROL Videos Only]** o **[!UICONTROL Photos Only]** nel flusso.

Per ulteriori opzioni della regola di flusso per tutte le regole di flusso, vedere [Opzioni regola di flusso per tutte le regole di flusso](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
