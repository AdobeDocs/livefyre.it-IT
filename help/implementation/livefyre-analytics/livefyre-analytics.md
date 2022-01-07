---
description: Analizzare l’attività di utenti, contenuti e moderatori per il sito.
title: Analytics
exl-id: dc0545ec-2294-44ab-87c4-67eb30c3f787
source-git-commit: 9cd6617c4204b2c09787ea294227f640018928ce
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 1%

---

# Analytics{#analytics}

Analizzare l’attività di utenti, contenuti e moderatori per il sito.

## Analytics {#topic_22D8FAE581CD440EA02B1595520F60C2}

Analizzare l’attività di utenti, contenuti e moderatori per il sito.

Livefyre Analytics fornisce l’accesso ai dati di rete in dashboard di facile lettura per conversazioni, moderazione e dati utente. Usa queste dashboard per monitorare l’attività ed eseguire analisi rapide sui tuoi siti.

Le dashboard possono essere filtrate per sito, data e attività. Utilizza il menu a discesa Rete in alto a sinistra nella finestra per selezionare un sito da visualizzare. Una volta generata, fai clic su un’intestazione di colonna per ordinare oppure passa il mouse sul grafico per ottenere informazioni più specifiche su qualsiasi punto di dati.

Questa pagina descrive:

* Selezione di un intervallo di date per il dashboard
* Mostrare/nascondere le attività disponibili
* Esportazione dei dati del dashboard
* Dashboard delle raccolte
* Dashboard di moderazione
* Dashboard degli utenti

>[!NOTE]
>
>Analytics supporta attualmente le attività provenienti dalle app core di Livefyre e dalla moderazione. La maggior parte delle attività incluse in queste dashboard sono disponibili anche tramite Eventi JavaScript Livefyre, che possono essere utilizzati per alimentare il tuo strumento di analisi personalizzato o di terze parti.

## Intervallo date {#concept_798C438120E643B6BE262C9997DC87C4}

Fai clic sul menu a discesa della data per selezionare un intervallo da visualizzare. Utilizza le date rapide oppure seleziona una data di inizio e una data di fine dai calendari forniti.

![](assets/analytics-date-range.png)

Date rapide:

* **Oggi:** Visualizza i dati dalla mezzanotte della mattina del giorno corrente fino all’ultima ora completa precedente a questo momento.
* **Ieri:** Visualizza i dati delle 24 ore precedenti.
* **7 giorni:** Visualizza i dati dei 7 giorni precedenti, esclusa la data odierna.
* **30 giorni:** Visualizza i dati dei 30 giorni precedenti, escluso il giorno corrente.
* **Questa settimana:** Visualizza i dati dalla mezzanotte della domenica scorsa fino all’ultima ora completa precedente a questo momento.
* **Questo mese:** Visualizza i dati dalla mezzanotte del primo giorno del mese corrente fino all’ultima ora completa precedente a questo momento.
* **Settimana scorsa:** Visualizza i dati della settimana scorsa.
* **Mese scorso:** Visualizza i dati del mese scorso.

## Mostrare/nascondere le attività {#concept_022D9851CBCE4A2FB80D0AE52A23744D}

Le attività sono azioni intraprese dagli utenti sul tuo sito e includono commenti, creazione di segnalibri, condivisione e moderazione. Utilizza la **Mostra/Nascondi attività** a discesa per selezionare le attività da includere nel dashboard.

>[!NOTE]
>
>Quando si selezionano nuovi eventi per il filtro, la pagina viene nuovamente sottoposta a rendering senza modificare l’URL.

![](assets/analytics-show-hide-activities.png)

Le attività disponibili variano in base al tipo di dashboard e all’esportazione e possono includere:

* **Post:** Visualizza i dati dalla mezzanotte della mattina del giorno corrente fino all’ultima ora completa precedente a questo momento.
* **Risposte:** Visualizza i dati delle 24 ore precedenti.
* **Mi piace:** Visualizza i dati dei 7 giorni precedenti, esclusa la data odierna.
* **Non piace:** Visualizza i dati dei 30 giorni precedenti, escluso il giorno corrente.
* **Contiene file multimediali:** Visualizza i dati dalla mezzanotte della domenica scorsa fino all’ultima ora completa precedente a questo momento.
* **Il post ha il caricamento di foto:** Visualizza i dati dalla mezzanotte del primo giorno del mese corrente fino all’ultima ora completa precedente a questo momento.
* **Il post ha un link:** Visualizza i dati della settimana scorsa.
* **Il post ha @mentions:** Visualizza i dati del mese scorso.
* **Approvato:** Visualizza i dati del mese scorso.
* **Bozo&#39;d:** Visualizza i dati del mese scorso.
* **Eliminato:** Visualizza i dati del mese scorso.
* **Totale moderazione:** Visualizza i dati del mese scorso.

## Esportazione dei dati del dashboard {#concept_730DB61A9F894BE6BFB34E0E2A421ED3}

Utilizza la **Esporta** menu a discesa per esportare i dati del dashboard come file CSV.

* Digest giornaliero (solo raccolte): esporta i dati giornalieri dell’ultima settimana completa per ogni raccolta.
* Dati tabella: esporta tutti i dati delle raccolte raggruppate (tutte le colonne e tutte le righe nel rapporto corrente).
* Dati grezzi: esporta tutti i singoli eventi utilizzati per creare il rapporto rollup corrente.

>[!NOTE]
>
>L&#39;esportazione di questi rapporti potrebbe richiedere alcuni minuti. Tutte le marche temporali sono tempo Unix.

## Raccolte {#concept_228D8E5553784DB8BABF3819A5FF0345}

Il dashboard Raccolte elenca l’attività dell’utente per raccolta, consentendoti di determinare il contenuto più (e meno) coinvolgente. Ogni raccolta elencata include un collegamento alla pagina in cui può essere trovata.

![](assets/analytics-collections.png)

## Moderazione {#concept_98689B1E804B43CEA21E3F456107CCD9}

Il dashboard Moderazione elenca gli eventi per moderatore, consentendoti di valutarne l’attività. Utilizza questo rapporto per trovare i moderatori più attivi e le loro azioni di moderazione più comuni.

>[!NOTE]
>
>Le attività di moderazione automatizzata Livefyre saranno elencate per il nome del moderatore Livefyre System.

![](assets/analytics-moderation.png)

## Utenti {#concept_D1A83E31C7B5467F9C844CBF9A740E12}

Il dashboard Utenti mostra l’attività del sito in base all’utente, consentendoti di analizzare in che modo i singoli utenti interagiscono con il sito. Usa questo dashboard per trovare gli utenti più attivi nel sito e per valutare le attività del sito più popolari.

![](assets/analytics-users.png)
