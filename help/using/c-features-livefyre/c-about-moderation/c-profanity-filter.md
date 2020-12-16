---
description: nulle
seo-description: nulle
seo-title: Utilizzo del filtro Profanity
solution: Experience Manager
title: Utilizzo del filtro Profanity
uuid: b0b1fbae-c88c-403c-9b91-df6620675f39
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 0%

---


# Utilizzo del filtro Profanity{#using-the-profanity-filter}

Tutto il contenuto pubblicato in un&#39;app Livefyre viene controllato per verificarne la correttezza. Se una parola inclusa nell&#39;elenco delle profanità si trova nel contenuto o nel nome visualizzato di un utente, il contenuto verrà contrassegnato come &quot;Profanity&quot;, consentendo di filtrarlo per la verifica preliminare, le regole, il ModQ o le ricerche generali in Contenuto app.

>[!NOTE]
>
>I contenuti degli amministratori e dei manager di Studio non sono soggetti al controllo Regola di profitto e i contenuti pubblicati da un moderatore non vengono contrassegnati.

Livefyre fornisce un elenco di profanità predefinito. È possibile scegliere di applicare questo elenco a livello di rete, fornire un proprio elenco o utilizzare un aggregato dei due. I singoli siti all&#39;interno della rete possono ereditare l&#39;elenco delle proprietà della rete o utilizzare un elenco personalizzato per essere specifici del sito.

Per fornire il proprio elenco di redditività personalizzato come impostazione predefinita della rete, inviatelo al vostro account manager Livefyre.

## Abilitazione del filtro delle proprietà {#section_yqc_qsk_f1b}

Abilitare e configurare il filtro di profanità a livello di rete e di sito. Disattivate il filtro di profondità a livello di rete per disattivare automaticamente il filtro di profanità per tutti i siti che ereditano dalla rete.

>[!NOTE]
>
>Tutto il contenuto che passa attraverso Livefyre viene controllato per verificarne la blasfemia. Se viene trovato del contenuto che include le parole contenute nell&#39;elenco di profanità SAFE predefinito o nell&#39;elenco di Profanity personalizzato, viene contrassegnato come &quot;Profanity&quot;. Per impostare Livefyre affinché adotti automaticamente azioni su questi elementi, ruotare **[!UICONTROL Enable Profanity Checking]** su **[!UICONTROL ON]**.

## Abilitare il filtro Profanity per una rete {#section_twd_ssk_f1b}

1. Selezionare **[!UICONTROL Network]** dal menu a discesa di rete.
1. Vai a **[!UICONTROL Settings > Network Settings > Moderation]**.
1. Scorrete verso il basso fino a **[!UICONTROL Profanity List]** e impostate **[!UICONTROL Enable Profanity Checking]** su **[!UICONTROL ON]**.

1. Utilizzare il campo **[!UICONTROL Update Network Profanity List]** per aggiungere parole all&#39;elenco, oppure fare clic su una parola per rimuoverla dall&#39;elenco.

>[!NOTE]
>
>La modifica dell&#39;elenco delle proprietà a livello di rete non influisce sugli elenchi già esistenti a livello di sito. Per garantire che vengano apportate modifiche dalla rete al sito, selezionare **[!UICONTROL Restore Network List]** per il sito dopo che sono state apportate le modifiche.

## Abilitare il filtro Profanity per un sito {#section_fld_wsk_f1b}

1. Selezionate il sito dal menu a discesa di rete.
1. Vai a **[!UICONTROL Settings > Site Settings > Moderation]**.
1. Scorrete verso il basso fino a **[!UICONTROL Profanity List]** e impostate **[!UICONTROL Enable Profanity Checking]** su **[!UICONTROL ON]**.

1. Scegliete una delle seguenti opzioni:

   * Per ereditare l&#39;Elenco profitti dalla rete (non comune), impostare **[!UICONTROL Use Site Profanity List]** su **[!UICONTROL OFF]**.

   * Per modificare l&#39;Elenco profitti specifico per il sito, impostare **[!UICONTROL Use Site Profanity List]** su **[!UICONTROL On]** per aprire il campo **[!UICONTROL Update Profanity List]** in cui è possibile modificare l&#39;elenco:

      * Per rimuovere una parola, fare clic su di essa.
      * Per aggiungere una parola, digitare la parola nella casella **[!UICONTROL Add new word]** e premere **[!UICONTROL Return]**.

      * Per verificare se una parola è inclusa nell&#39;elenco, digitare la parola nella casella **[!UICONTROL Test profanity filter]**.
   * Per reimportare l&#39;elenco delle proprietà di rete e applicarlo al sito, fare clic su **[!UICONTROL Restore Network List]**.
   * Per cancellare tutto il contenuto dall&#39;elenco e iniziare da zero, fare clic su **[!UICONTROL Clear List]**.


## Utilizzo di contenuti che contengono funzionalità {#section_epy_dtk_f1b}

Utilizzate l&#39;Elenco profitti per filtrare le ricerche di contenuto e creare regole di moderazione per ModQ.

Per cercare contenuti contenenti profanità, andate a **[!UICONTROL Library > App Content]**, **[!UICONTROL Filter by Flags]** e selezionate la casella di controllo **[!UICONTROL Profanity]**. Viene visualizzato tutto il contenuto catturato dal filtro di profitto per il sito o la rete selezionati. Questo elenco includerà il contenuto estratto nell&#39;app tramite SocialSync e Streams.

Per creare regole di moderazione, in Studio selezionare **[!UICONTROL Settings > Network Settings > Moderation]**. Una volta attivato il filtro di profanità, verrà visualizzata una nuova regola che consente di contrassegnare o moderare il contenuto contenente una profanità. Per impostazione predefinita, questa regola attiva automaticamente **[!UICONTROL Premoderate]** per il contenuto profano, che può essere modificato in **[!UICONTROL Trash it]** o **[!UICONTROL Bozo it]**.

>[!NOTE]
>
>Se un singolo contenuto è soggetto a più tipi di regole (come le regole SICUREZZA e Contrassegno), verrà applicato il più rigoroso. Ad esempio: Se la regola di moderazione dice di moderare un contenuto, ma una regola di sicurezza dice che lo cestino, sarà Trash.

## Visualizza e aggiorna l&#39;elenco delle proprietà per una rete {#section_qdb_btk_f1b}

1. Vai a **[!UICONTROL Settings > Network Settings > Moderation]**.
1. Scorrete verso il basso fino alla sezione **[!UICONTROL Profanity List]**.
1. Impostate **[!UICONTROL Enable Profanity Checking]** su **[!UICONTROL On]** per visualizzare l&#39;elenco abilitato per la rete (predefinito Livefyre o elenco personalizzato caricato) e modificarlo. Potete modificare l’elenco nei seguenti modi:
   * Per rimuovere una parola, fare clic su di essa.
   * Per aggiungere una parola, digitare la parola nella casella **[!UICONTROL Add new word]** e premere **[!UICONTROL Return]**.
   * Per verificare se una parola è inclusa nell&#39;elenco, digitare la parola nella casella **[!UICONTROL Test profanity filter]**.

>[!NOTE]
>
>Solo gli amministratori e i moderatori di studio possono modificare gli elenchi di redditività.

