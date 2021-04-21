---
description: Puoi creare regole di flusso per estrarre contenuto da Instagram.
title: Regole di Instagram
exl-id: ac00a12c-94b1-4464-ad3f-991382759d71
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Regole Instagram{#instagram-rules}

Puoi creare regole di flusso per estrarre contenuto da Instagram.

>[!NOTE]
>
>Prima di creare un flusso Instagram, è necessario aggiungere almeno un account aziendale Instagram alla sezione **[!UICONTROL Social Accounts]** in **[!UICONTROL Network Settings]**. Per ulteriori informazioni su come configurare un account Instagram, consulta [Informazioni sugli account Instagram](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

Crea regole Instagram basate su @mentions o hashtag.

>[!NOTE]
>
>Tutte le regole di Instagram richiedono almeno un hashtag. L’aggiunta di parole chiave e di un nome utente per la regola restituirà contenuto che include entrambe le voci.

Per creare regole Instagram per estrarre contenuto dai feed Instagram nell’app o nella cartella, filtra in base a:

* **[!UICONTROL Words]**

   * Inserisci **[!UICONTROL hashtags]** da includere o escludere dal flusso Instagram. Se si specificano i valori per i campi **[!UICONTROL Contains]** e **[!UICONTROL Does not contain]**, verranno restituite immagini contenenti il primo e non il secondo.

   * Ad esempio, l’immissione di **[!UICONTROL Contains]** parole chiave Giants, Posey e **[!UICONTROL Does not contain]** parola chiave Dodger restituirà tutti i post che includono la parola Giants o Posey e non includerà la parola Dodger.

      >[!NOTE]
      >
      >Instagram Rules restituirà post che includono l&#39;hashtag elencato nei commenti dell&#39;autore, che potrebbero non essere visualizzati nel flusso.

* **[!UICONTROL Mentions]**

   * Immettere **[!UICONTROL @mentions]** per effettuare il pull nel flusso o escludere dal flusso.

* **[!UICONTROL Authors]**

   >[!NOTE]
   >
   >Per utilizzare la ricerca Author in una regola Instagram Stream, è necessario disporre di un account aziendale Instagram configurato in Livefyre. Per ulteriori informazioni sulla configurazione degli account aziendali Instagram in Livefyre, consulta [Informazioni sugli account Instagram](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

   * Immettere **[!UICONTROL @usernames]** per eseguire il pull nel flusso. L&#39;account associato al **@username** deve essere un account aziendale Instagram.

   * Inserisci il **@usernames** per escludere dal flusso.

* **[!UICONTROL Additional Filters]**

   * Seleziona se includere **[!UICONTROL All Content]**, **[!UICONTROL Videos Only]** o **[!UICONTROL Photos Only]** nel flusso.

Per ulteriori opzioni della regola Stream per tutte le regole Stream, vedere [Opzioni della regola Stream per tutte le regole Stream](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
