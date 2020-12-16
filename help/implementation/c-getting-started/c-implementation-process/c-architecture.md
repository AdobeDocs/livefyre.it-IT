---
description: Scoprite le convenzioni di Livefyre e come Livefyre organizza i contenuti.
seo-description: Scoprite le convenzioni di Livefyre e come Livefyre organizza i contenuti.
seo-title: Architettura
solution: Experience Manager
title: Architettura
uuid: 94358e6c-954a-4a52-9bb2-d800b2933130
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 0%

---


# Architecture{#architecture}

Scoprite le convenzioni di Livefyre e come Livefyre organizza i contenuti.

Questa sezione fornisce una panoramica dell’architettura di rete Livefyre.

## Panoramica di reti e siti

Livefyre organizza utenti e contenuti per rete e per sito. A ogni rete possono essere associati uno o più account utente e ogni rete può includere uno o più siti Livefyre. Un sito Livefyre è un raggruppamento arbitrario di raccolte. Una raccolta viene mappata su un ID articolo nel CMS.

## Informazioni sulle reti {#section_hqt_4m4_xz}

I clienti con più domini possono condividere gli account utente tra tutti i domini, utilizzando una singola rete Livefyre. I clienti che desiderano mantenere account utente separati per domini diversi dovranno disporre di reti Livefyre separate.

Le impostazioni di configurazione possono essere applicate a siti, reti e raccolte (come descritto nella figura precedente).

>[!NOTE]
>
>Alcune impostazioni sono disponibili solo a livello di rete (come le preferenze di notifica e-mail, e-mail dall&#39;indirizzo e loghi personalizzati e-mail). Se desiderate che queste impostazioni siano diverse per ciascun dominio, dovete utilizzare più reti.

## Informazioni sui siti {#section_vjw_nm4_xz}

Un sito è un raggruppamento arbitrario di articoli. Il raggruppamento è utile in quanto consente di assegnare diversi moderatori a diversi gruppi di contenuti. Moderatori e proprietari possono essere configurati per moderare i contenuti e configurare le impostazioni di amministrazione a livello di rete o di sito. Se desiderate che alcuni moderatori vedano solo determinate raccolte, queste raccolte possono essere configurate come un sito Livefyre separato.

>[!NOTE]
>
>Non esiste alcun limite al numero di siti che si possono avere nella rete personalizzata.

## Diagramma sequenza app {#section_mw2_lm4_xz}

Sia che desideriate implementare una funzione personalizzata con gli endpoint forniti da Livefyre, o che dobbiate semplicemente eseguire il debug di un problema, è importante comprendere il funzionamento del flusso di richieste/risposte dell&#39;app Livefyre.

![](assets/appsequencediagram.png)

1. Quando il cliente accede al sito, create un&#39;istanza dell&#39;app Livefyre con l&#39;ID sito e l&#39;ID articolo.
1. Se desiderate autenticare l’utente (utile per la valutazione del traffico e per la protezione del sito), inviate a Livefyre le informazioni sul sito e il token del profilo utente.
1. Inviate a Livefyre l&#39;ID sito e l&#39;ID articolo per inizializzare l&#39;app.

   Livefyre restituisce il contenuto iniziale.

   Inviate questo contenuto alla pagina e visualizzate l&#39;app.

1. Per aggiornare il contenuto visualizzato sulla pagina, inviate a Livefyre l’ID evento più recente dalla pagina. Se sono disponibili nuovi contenuti, questi verranno restituiti.

   Ricaricate la pagina con nuovi contenuti e ripetete il processo a tempo indeterminato.

1. Se consentite agli utenti di pubblicare nuovo contenuto, attivate un evento quando il nuovo contenuto viene pubblicato sul sito per pubblicare il contenuto su Livefyre. Livefyre restituirà un flusso aggiornato che potete utilizzare per aggiornare il sito.
