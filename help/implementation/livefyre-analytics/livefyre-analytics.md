---
description: Analizzare l'attività di utenti, contenuti e moderatori per il sito.
seo-description: Analizzare l'attività di utenti, contenuti e moderatori per il sito.
seo-title: Analytics
solution: Experience Manager
title: Analytics
uuid: b022aa77-59b9-422a-8d9f-fb9d8a1b0478
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Analytics{#analytics}

Analizzare l'attività di utenti, contenuti e moderatori per il sito.

## Analytics {#topic_22D8FAE581CD440EA02B1595520F60C2}

Analizzare l'attività di utenti, contenuti e moderatori per il sito.

Livefyre Analytics consente di accedere ai dati della rete in dashboard di facile lettura per conversazioni, moderazioni e dati utente. Utilizzate queste dashboard per monitorare l'attività ed eseguire analisi rapide sui siti.

I dashboard possono essere filtrati per sito, data e attività. Utilizzate il pulldown Rete in alto a sinistra nella finestra per selezionare un sito da visualizzare. Una volta generata, fai clic sull’intestazione di una colonna per ordinare o passa il mouse sul grafico per ottenere informazioni più specifiche su qualsiasi punto dati.

Questa pagina descrive:

* Selezione di un intervallo [di](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#DateRange) date per il dashboard
* [Visualizzazione / Nascondere le attività disponibili](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ShowHideActivities)
* [Esportazione dei dati del dashboard](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ExportDashboardData)
* [Pannello Raccolte](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#CollectionsDashboard)
* [Pannello Moderazione](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ModerationDashboard)
* [Pannello Utenti](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#UsersDashboard)

>[!NOTE]
>
>Analytics supporta attualmente le attività derivanti dalle app core e dalla moderazione di Livefyre. La maggior parte delle attività incluse in queste dashboard sono disponibili anche tramite eventi [JavaScript](https://answers.livefyre.com/developers/reference/app-customizations/javascript-events/)Livefyre, che possono essere utilizzati per alimentare il vostro strumento di analisi personalizzato o di terze parti.

## Intervallo date {#concept_798C438120E643B6BE262C9997DC87C4}

Fai clic sul menu a discesa della data per selezionare un intervallo da visualizzare. Utilizzare le date rapide oppure selezionare una data di inizio e una data di fine dai calendari forniti.

![](assets/analytics-date-range.png)

Date rapide:

* **** Oggi: Visualizza i dati dalla mezzanotte della mattina del giorno corrente fino all'ultima ora completa prima di questo momento.
* **** Ieri: Visualizza i dati delle 24 ore precedenti.
* **** 7 giorni: Visualizza i dati dei 7 giorni precedenti, esclusi quelli odierni.
* **** 30 giorni: Visualizza i dati dei 30 giorni precedenti, esclusi quelli odierni.
* **** Questa settimana: Visualizza i dati dalla mezzanotte alla mattina dell'ultima domenica, fino all'ultima ora completa prima di questo momento.
* **** Questo mese: Visualizza i dati dalla mezzanotte del primo giorno del mese corrente fino all'ultima ora completa prima di questo momento.
* **** Ultima settimana: Visualizza i dati della settimana scorsa.
* **** Ultimo mese: Visualizza i dati del mese scorso.

## Visualizzazione/nascondere attività {#concept_022D9851CBCE4A2FB80D0AE52A23744D}

Le attività sono azioni che gli utenti effettuano sul sito, inclusi commenti, contrassegni, condivisione e moderazione. Utilizzate il **menu a discesa Mostra/Nascondi attività** per selezionare le attività da includere nel dashboard.

>[!NOTE]
>
>Se si selezionano nuovi eventi per il filtro, la pagina viene nuovamente visualizzata senza modificare l’URL.

![](assets/analytics-show-hide-activities.png)

Le attività disponibili variano in base al tipo di dashboard e all'esportazione e possono includere:

* **** Post: Visualizza i dati dalla mezzanotte della mattina del giorno corrente fino all'ultima ora completa prima di questo momento.
* **** Risposte: Visualizza i dati delle 24 ore precedenti.
* **** Mi piace: Visualizza i dati dei 7 giorni precedenti, esclusi quelli odierni.
* **** Non piace: Visualizza i dati dei 30 giorni precedenti, esclusi quelli odierni.
* **** Contiene file multimediali: Visualizza i dati dalla mezzanotte alla mattina dell'ultima domenica, fino all'ultima ora completa prima di questo momento.
* **** Post con caricamento foto: Visualizza i dati dalla mezzanotte del primo giorno del mese corrente fino all'ultima ora completa prima di questo momento.
* **** Collegamento post: Visualizza i dati della settimana scorsa.
* **** Il post ha @mentions: Visualizza i dati del mese scorso.
* **** Approvato: Visualizza i dati del mese scorso.
* **** Bozo'd: Visualizza i dati del mese scorso.
* **** Trashed: Visualizza i dati del mese scorso.
* **** Totale moderazione: Visualizza i dati del mese scorso.

## Esportazione dei dati del dashboard {#concept_730DB61A9F894BE6BFB34E0E2A421ED3}

Usate il menu a discesa **Esporta** per esportare i dati del dashboard come file CSV.

* Riepilogo giornaliero (solo raccolte): esporta i dati giornalieri dell'ultima settimana completa per ogni raccolta.
* Dati tabella: esporta tutti i dati delle raccolte rollup (tutte le colonne e tutte le righe del rapporto corrente).
* Dati grezzi: esporta tutti i singoli eventi utilizzati per creare il rapporto rollup corrente.

>[!NOTE]
>
>L'esportazione di questi rapporti potrebbe richiedere alcuni minuti. Tutte le marche temporali sono ora Unix.

## Raccolte {#concept_228D8E5553784DB8BABF3819A5FF0345}

Il dashboard Raccolte elenca l'attività utente per raccolta, consentendo di determinare il contenuto più (e meno) coinvolgente. Ogni raccolta elencata include un collegamento alla pagina in cui è possibile trovarlo.

![](assets/analytics-collections.png)

## Moderazione {#concept_98689B1E804B43CEA21E3F456107CCD9}

Il dashboard Moderazione elenca gli eventi per moderatore, consentendo di valutarne l'attività. Utilizzate questo rapporto per individuare i moderatori più attivi e le loro azioni di moderazione più comuni.

>[!NOTE]
>
>Le attività di moderazione automatizzata di Livefyre verranno elencate per il nome del moderatore Livefyre System.

![](assets/analytics-moderation.png)

## Utenti {#concept_D1A83E31C7B5467F9C844CBF9A740E12}

Il pannello Utenti mostra l'attività del sito in base all'utente, consentendo di analizzare in che modo i singoli utenti interagiscono con il sito. Utilizzate questa dashboard per individuare gli utenti più attivi nel sito e per valutare le attività più comuni del sito.

![](assets/analytics-users.png)

