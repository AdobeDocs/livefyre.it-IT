---
title: Utilizzo del filtro Profanity
description: Utilizzo del filtro Profanity
exl-id: 6ea7d913-f562-42a5-a6ea-241aa4e1089a
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 0%

---

# Utilizzo del filtro Profanity{#using-the-profanity-filter}

Tutti i contenuti pubblicati in un’app Livefyre vengono controllati per verificarne la presenza. Se una parola inclusa nell’elenco dei profili si trova nel contenuto o nel nome visualizzato di un utente, tale contenuto verrà contrassegnato con &quot;Profanity&quot; (Profanità), che consente di filtrarlo per Premoderazione, Regole, ModQ o ricerche generali nel contenuto dell’app.

>[!NOTE]
>
>Il contenuto degli amministratori e dei manager di Studio non è soggetto al controllo Regola di profitto e il contenuto pubblicato da un moderatore non verrà contrassegnato.

Livefyre fornisce un elenco di profanità predefinito. È possibile scegliere di applicare questo elenco a livello di rete, fornire un proprio elenco o utilizzare un aggregato dei due. I singoli siti all&#39;interno della rete possono ereditare l&#39;elenco delle proprietà della rete o utilizzare un elenco personalizzato per essere specifico del sito.

Per fornire il proprio elenco di profili personalizzato come impostazione predefinita della rete, invialo al tuo account manager Livefyre.

## Abilitazione del filtro profili {#section_yqc_qsk_f1b}

Abilita e configura il filtro di profanity a livello di rete e di sito. Disattiva il filtro di profanità a livello di rete per disabilitare automaticamente il filtro di profanity per tutti i siti che ereditano dalla rete.

>[!NOTE]
>
>Tutto il contenuto che passa attraverso Livefyre è controllato per la blasfemia. Se viene trovato contenuto che include parole contenute nell&#39;elenco di profanità SAFE predefinito o nell&#39;elenco di Profanity personalizzato, viene contrassegnato come &quot;Profanity&quot;. Per impostare Livefyre affinché esegua automaticamente l&#39;azione su questi elementi, ruotare **[!UICONTROL Enable Profanity Checking]** su **[!UICONTROL ON]**.

## Abilitare il filtro Profanity per una rete {#section_twd_ssk_f1b}

1. Selezionare **[!UICONTROL Network]** dal menu a discesa di rete.
1. Vai a **[!UICONTROL Settings > Network Settings > Moderation]**.
1. Scorri verso il basso fino a **[!UICONTROL Profanity List]** e imposta **[!UICONTROL Enable Profanity Checking]** su **[!UICONTROL ON]**.

1. Utilizzare il campo **[!UICONTROL Update Network Profanity List]** per aggiungere parole all&#39;elenco oppure fare clic su una parola per rimuoverla dall&#39;elenco.

>[!NOTE]
>
>La modifica dell&#39;elenco delle proprietà a livello di rete non avrà alcun effetto sugli elenchi a livello di sito già esistenti. Per garantire che le modifiche dalla rete siano apportate al sito, selezionare **[!UICONTROL Restore Network List]** per il sito dopo aver apportato le modifiche.

## Attiva il filtro Profanity per un sito {#section_fld_wsk_f1b}

1. Selezionare il sito dal menu a discesa di rete.
1. Vai a **[!UICONTROL Settings > Site Settings > Moderation]**.
1. Scorri verso il basso fino a **[!UICONTROL Profanity List]** e imposta **[!UICONTROL Enable Profanity Checking]** su **[!UICONTROL ON]**.

1. Scegliere una delle opzioni seguenti:

   * Per ereditare l&#39;Elenco profitti dalla rete (non comune), impostare **[!UICONTROL Use Site Profanity List]** su **[!UICONTROL OFF]**.

   * Per modificare l&#39;elenco delle proprietà specifico del sito, impostare **[!UICONTROL Use Site Profanity List]** su **[!UICONTROL On]** per aprire il campo **[!UICONTROL Update Profanity List]** in cui è possibile modificare l&#39;elenco:

      * Per rimuovere una parola, fare clic su di essa.
      * Per aggiungere una parola, digita la parola nella casella **[!UICONTROL Add new word]** e premi **[!UICONTROL Return]**.

      * Per verificare se una parola è inclusa nell’elenco, digitare la parola nella casella **[!UICONTROL Test profanity filter]**.
   * Per reimportare l&#39;elenco delle proprietà della rete e applicarlo al sito, fare clic su **[!UICONTROL Restore Network List]**.
   * Per cancellare tutto il contenuto dall’elenco e iniziare da zero, fai clic su **[!UICONTROL Clear List]**.


## Utilizzo di contenuti contenenti proprietà {#section_epy_dtk_f1b}

Utilizza l’Elenco profitti per filtrare le ricerche di contenuto e creare regole di moderazione per ModQ.

Per cercare contenuti contenenti profanità, vai su **[!UICONTROL Library > App Content]**, **[!UICONTROL Filter by Flags]** e seleziona la casella di controllo **[!UICONTROL Profanity]**. Verranno visualizzati tutti i contenuti catturati dal filtro Profanity per il sito o la rete selezionata. Questo elenco include il contenuto inserito nell’app tramite SocialSync e Streams.

Per creare regole di moderazione, in Studio selezionare **[!UICONTROL Settings > Network Settings > Moderation]**. Una volta abilitato il filtro di profanità, viene visualizzata una nuova regola che consente di contrassegnare o moderare il contenuto contenente profanità. Per impostazione predefinita, questa regola abilita automaticamente **[!UICONTROL Premoderate]** per il contenuto di profilo, che può essere modificato in **[!UICONTROL Trash it]** o **[!UICONTROL Bozo it]**.

>[!NOTE]
>
>Se un singolo contenuto è soggetto a più tipi di regole (come le regole SAFE e Flag), viene applicato il più rigoroso. Ad esempio: Se la regola di moderazione dice di moderare un contenuto, ma una regola SAFE dice di eliminarlo, verrà eliminata.

## Visualizza e aggiorna l&#39;elenco delle proprietà per una rete {#section_qdb_btk_f1b}

1. Vai a **[!UICONTROL Settings > Network Settings > Moderation]**.
1. Scorri verso il basso fino alla sezione **[!UICONTROL Profanity List]**.
1. Imposta **[!UICONTROL Enable Profanity Checking]** su **[!UICONTROL On]** per visualizzare l’elenco abilitato per la rete (impostazione predefinita Livefyre o elenco personalizzato caricato) e modificalo. È possibile modificare l’elenco nei seguenti modi:
   * Per rimuovere una parola, fare clic su di essa.
   * Per aggiungere una parola, digita la parola nella casella **[!UICONTROL Add new word]** e premi **[!UICONTROL Return]**.
   * Per verificare se una parola è inclusa nell’elenco, digitare la parola nella casella **[!UICONTROL Test profanity filter]**.

>[!NOTE]
>
>Solo gli amministratori e i moderatori di Studio possono modificare gli elenchi di profitto.
