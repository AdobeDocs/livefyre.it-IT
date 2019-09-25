---
description: nulle
seo-description: nulle
seo-title: Utilizzo del filtro Profanity
solution: Experience Manager
title: Utilizzo del filtro Profanity
uuid: b0b1fbae-c88c-403c-9b91-df6620675f39
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Utilizzo del filtro Profanity{#using-the-profanity-filter}

Tutto il contenuto pubblicato in un'app Livefyre viene controllato per verificarne la correttezza. Se una parola inclusa nell'elenco delle profanità si trova nel contenuto o nel nome visualizzato di un utente, il contenuto verrà contrassegnato come "Profanity", consentendo di filtrarlo per la verifica preliminare, le regole, il ModQ o le ricerche generali in Contenuto app.

>[!NOTE]
>
>I contenuti degli amministratori e dei manager di Studio non sono soggetti al controllo Regola di profitto e i contenuti pubblicati da un moderatore non vengono contrassegnati.

Livefyre fornisce un elenco di profanità predefinito. È possibile scegliere di applicare questo elenco a livello di rete, fornire un proprio elenco o utilizzare un aggregato dei due. I singoli siti all'interno della rete possono ereditare l'elenco delle proprietà della rete o utilizzare un elenco personalizzato per essere specifici del sito.

Per fornire il proprio elenco di redditività personalizzato come impostazione predefinita della rete, inviatelo al vostro account manager Livefyre.

## Abilitazione del filtraggio della redditività {#section_yqc_qsk_f1b}

Abilitare e configurare il filtro di profanità a livello di rete e di sito. Disattiva il filtro di profondità a livello di rete per disattivare automaticamente il filtro di profanità per tutti i siti che ereditano dalla rete.

>[!NOTE]
>
>Tutto il contenuto che passa attraverso Livefyre viene controllato per verificarne la blasfemia. Se viene trovato del contenuto che include le parole contenute nell'elenco di profanità SAFE predefinito o nell'elenco di Profanity personalizzato, viene contrassegnato come "Profanity". Per impostare Livefyre affinché adotti automaticamente azioni su questi elementi, passate **[!UICONTROL Enable Profanity Checking]** a **[!UICONTROL ON]**.

## Abilitare il filtro Profanity per una rete {#section_twd_ssk_f1b}

1. Selezionare **[!UICONTROL Network]** dal menu a discesa di rete.
1. Vai a **[!UICONTROL Settings > Network Settings > Moderation]**.
1. Scorrete verso il basso fino a **[!UICONTROL Profanity List]**, quindi impostate **[!UICONTROL Enable Profanity Checking]** su **[!UICONTROL ON]**.

1. Utilizzare il **[!UICONTROL Update Network Profanity List]** campo per aggiungere parole all'elenco, oppure fare clic su una parola per rimuoverlo dall'elenco.

>[!NOTE]
>
>La modifica dell'elenco delle proprietà a livello di rete non influisce sugli elenchi già esistenti a livello di sito. Per assicurarsi che le modifiche dalla rete siano apportate al sito, selezionare **[!UICONTROL Restore Network List]** il sito dopo che sono state apportate le modifiche.

## Abilitare il filtro Profanity per un sito {#section_fld_wsk_f1b}

1. Selezionate il sito dal menu a discesa di rete.
1. Vai a **[!UICONTROL Settings > Site Settings > Moderation]**.
1. Scorrete verso il basso fino a **[!UICONTROL Profanity List]** e impostate **[!UICONTROL Enable Profanity Checking]** su **[!UICONTROL ON]**.

1. Scegliete una delle seguenti opzioni:

   * Per ereditare l'Elenco profitti dalla rete (non comune), impostare **[!UICONTROL Use Site Profanity List]** su **[!UICONTROL OFF]**.

   * Per modificare l'Elenco profitti specifico per il sito, impostare **[!UICONTROL Use Site Profanity List]** per **[!UICONTROL On]** **[!UICONTROL Update Profanity List]** aprire il campo, dove è possibile modificare l'elenco:

      * Per rimuovere una parola, fare clic sulla parola.
      * Per aggiungere una parola, digitare la parola nella **[!UICONTROL Add new word]** casella e premere **[!UICONTROL Return]**.

      * Per verificare se una parola è inclusa nell'elenco, digitare la parola nella **[!UICONTROL Test profanity filter]** casella.
   * Per reimportare l'elenco delle proprietà della rete e applicarlo al sito, fare clic su **[!UICONTROL Restore Network List]**.
   * Per cancellare tutto il contenuto dall'elenco e iniziare da zero, fare clic **[!UICONTROL Clear List]**.


## Utilizzo di contenuti che contengono proprietà {#section_epy_dtk_f1b}

Utilizzate l'Elenco profitti per filtrare le ricerche di contenuto e creare regole di moderazione per ModQ.

Per cercare contenuti contenenti profanità, andate a **[!UICONTROL Library > App Content]** e **[!UICONTROL Filter by Flags]** selezionate la **[!UICONTROL Profanity]** casella di controllo. Viene visualizzato tutto il contenuto catturato dal filtro di profitto per il sito o la rete selezionati. Questo elenco includerà il contenuto estratto nell'app tramite SocialSync e Streams.

Per creare regole di moderazione, selezionare Studio **[!UICONTROL Settings > Network Settings > Moderation]**. Una volta attivato il filtro di profanità, verrà visualizzata una nuova regola che consente di contrassegnare o moderare il contenuto contenente una profanità. Per impostazione predefinita, questa regola attiva automaticamente **[!UICONTROL Premoderate]** i contenuti profondi, che possono essere modificati in **[!UICONTROL Trash it]** o **[!UICONTROL Bozo it]**.

>[!NOTE]
>
>Se un singolo contenuto è soggetto a più tipi di regole (come le regole SICUREZZA e Contrassegno), verrà applicato il più rigoroso. Ad esempio: Se la regola di moderazione dice di moderare un contenuto, ma una regola di sicurezza dice che lo cestino, sarà Trash.

## Visualizzare e aggiornare l'elenco delle proprietà per una rete {#section_qdb_btk_f1b}

1. Vai a **[!UICONTROL Settings > Network Settings > Moderation]**.
1. Scorrete verso il basso fino alla **[!UICONTROL Profanity List]** sezione.
1. Impostato **[!UICONTROL Enable Profanity Checking]** per **[!UICONTROL On]** visualizzare l’elenco abilitato per la rete (predefinito Livefyre o elenco personalizzato caricato) e modificarlo. Potete modificare l’elenco nei seguenti modi:
   * Per rimuovere una parola, fare clic sulla parola.
   * Per aggiungere una parola, digitare la parola nella **[!UICONTROL Add new word]** casella e premere **[!UICONTROL Return]**.
   * Per verificare se una parola è inclusa nell'elenco, digitare la parola nella **[!UICONTROL Test profanity filter]** casella.

>[!NOTE]
>
>Solo gli amministratori e i moderatori di studio possono modificare gli elenchi di redditività.

