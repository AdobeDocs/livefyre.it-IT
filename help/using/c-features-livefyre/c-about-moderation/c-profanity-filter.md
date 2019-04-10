---
description: nulle
seo-description: nulle
seo-title: Utilizzo del filtro profanity
solution: Experience Manager
title: Utilizzo del filtro profanity
uuid: b 0 b 1 fbae-c 88 c -403 c -9 b 91-df 6620675 f 39
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Utilizzo del filtro profanity{#using-the-profanity-filter}

Tutto il contenuto pubblicato in un'app Livefyre viene controllato. Se una parola inclusa nell'elenco blasfemia si trova nel contenuto o nel nome visualizzato di un utente, il contenuto verrà contrassegnato come «Profanity», consentendo di filtrarlo per Premoderazione, Regole, modq o ricerche generiche in Contenuto app.

>[!NOTE]
>
>Il contenuto degli amministratori di studio e i manager non sono soggetti alla verifica della regola profanity e il contenuto pubblicato da un moderatore non verrà segnalato.

Livefyre fornisce un elenco profanity predefinito. Potete scegliere di applicare questo elenco a livello di rete, fornire un elenco personalizzato o utilizzare un totale di entrambi. I singoli siti all'interno della rete possono ereditare l'elenco profanity di rete, oppure utilizzare un elenco personalizzato per essere specifico del sito.

Per fornire un elenco profanity personalizzato come predefinito di rete, inviatelo al vostro account manager Livefyre.

## Abilitazione del filtro profanity {#section_yqc_qsk_f1b}

Abilita e configura il filtro blasfemico sia a livello di rete che di sito. Disattivate il filtro blasfemico a livello di rete per disattivare automaticamente il filtro blasfemia per tutti i siti che ereditano dalla rete.

>[!NOTE]
>
>Tutti i contenuti passati a Livefyre sono soggetti a controllo. Se viene trovato contenuto che include parole contenute nell'elenco fittizio SAFE o nell'elenco Profanity personalizzato, viene segnalata «Profanity. »» Per impostare Livefyre per intervenire automaticamente su questi elementi, passate **[!UICONTROL Enable Profanity Checking]****[!UICONTROL ON]**a.

## Abilitare il filtro profanity per una rete {#section_twd_ssk_f1b}

1. Selezionate **[!UICONTROL Network]** dal menu a discesa di rete.
1. **[!UICONTROL Settings > Network Settings > Moderation]**Vai a.
1. Scorrete verso il basso fino alla **[!UICONTROL Profanity List]**e **[!UICONTROL Enable Profanity Checking]** impostate su **[!UICONTROL ON]**.

1. Utilizzare il **[!UICONTROL Update Network Profanity List]** campo per aggiungere parole all'elenco o fare clic su una parola per rimuoverla dall'elenco.

>[!NOTE]
>
>La modifica dell'elenco profanity a livello di rete non influirà sugli elenchi a livello di sito già inseriti. Per fare in modo che le modifiche dalla rete siano effettuate al sito, selezionate **[!UICONTROL Restore Network List]** per il sito una volta apportate le modifiche.

## Attivare il filtro profanity per un sito {#section_fld_wsk_f1b}

1. Selezionate il sito dal menu a discesa di rete.
1. **[!UICONTROL Settings > Site Settings > Moderation]**Vai a.
1. Scorrete verso il basso fino alla **[!UICONTROL Profanity List]****[!UICONTROL Enable Profanity Checking]** posizione desiderata **[!UICONTROL ON]**.

1. Scegliete una delle opzioni seguenti:

   * To inherit the Profanity List from the network (this is not common), set **[!UICONTROL Use Site Profanity List]** to **[!UICONTROL OFF]**.

   * Per modificare l'elenco Profanity specifico per il sito, impostato **[!UICONTROL Use Site Profanity List]** su **[!UICONTROL On]** Aperto **[!UICONTROL Update Profanity List]** , dove potete modificare l'elenco:

      * Per rimuovere una parola, fate clic sulla parola.
      * Per aggiungere una parola, digitate la parola nella **[!UICONTROL Add new word]** casella e toccate **[!UICONTROL Return]**.

      * Per verificare se una parola è inclusa nell'elenco, digitate la parola nella **[!UICONTROL Test profanity filter]** casella.
   * Per reimportare l'elenco Profetico di rete e applicarlo al sito, fate clic **[!UICONTROL Restore Network List]**su.
   * Per cancellare tutto il contenuto dall'elenco e iniziare da zero, fate clic **[!UICONTROL Clear List]**su.


## Utilizzo del contenuto che contiene profanity {#section_epy_dtk_f1b}

Utilizzate l'elenco Profanity per filtrare le ricerche dei contenuti e creare regole di premoderazione per modq.

Per cercare contenuti con blasfemia, vai a **[!UICONTROL Library > App Content]**e **[!UICONTROL Filter by Flags]** seleziona la **[!UICONTROL Profanity]** casella di controllo. Viene visualizzato tutto il contenuto che è stato rilevato dal filtro profanity per il sito o la rete selezionata. Questo elenco includerà il contenuto inserito nell'app tramite socialsync e flussi.

To create Premoderation rules, from Studio select **[!UICONTROL Settings > Network Settings > Moderation]**. Quando il filtro profeity è stato abilitato, viene visualizzata una nuova regola che consente di segnalare o limitare il contenuto che contiene la profasità. Per impostazione predefinita, questa regola abilita **[!UICONTROL Premoderate]** automaticamente il contenuto profano, che può essere cambiato in o **[!UICONTROL Trash it]****[!UICONTROL Bozo it]**.

>[!NOTE]
>
>Se un singolo contenuto è soggetto a più tipi di regole (come sia SAFE che flag), verranno applicati i più rigorosi. Ad esempio: Se la regola Premoderazione dice di premoderare una parte del contenuto, ma una regola SICURA dice di cestarlo, verrà suddiviso.

## Visualizzare e aggiornare l'elenco profetico per una rete {#section_qdb_btk_f1b}

1. **[!UICONTROL Settings > Network Settings > Moderation]**Vai a.
1. Scorrete verso il basso fino alla **[!UICONTROL Profanity List]** sezione.
1. Impostate su **[!UICONTROL Enable Profanity Checking]****[!UICONTROL On]** per visualizzare l'elenco abilitato per la rete (predefinito Livefyre o l'elenco personalizzato caricato) e modificarlo. Potete modificare l'elenco nei modi seguenti:
   * Per rimuovere una parola, fate clic sulla parola.
   * Per aggiungere una parola, digitate la parola nella **[!UICONTROL Add new word]** casella e toccate **[!UICONTROL Return]**.
   * Per verificare se una parola è inclusa nell'elenco, digitate la parola nella **[!UICONTROL Test profanity filter]** casella.

>[!NOTE]
>
>Solo gli amministratori di studio e i moderatori possono modificare elenchi profanistici.

