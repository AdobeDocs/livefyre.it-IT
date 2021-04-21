---
description: Scopri le convenzioni di Livefyre e come Livefyre organizza i contenuti.
title: Architettura
exl-id: d4fe12d1-117a-4aae-90ff-e9ebdd6c5bac
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 0%

---

# Architettura{#architecture}

Scopri le convenzioni di Livefyre e come Livefyre organizza i contenuti.

Questa sezione fornisce una panoramica dell’architettura di rete Livefyre.

## Panoramica di reti e siti

Livefyre organizza utenti e contenuti per rete e sito. A ogni rete possono essere associati uno o più account utente e ogni rete può includere uno o più siti Livefyre. Un sito Livefyre è un raggruppamento arbitrario di raccolte. Una raccolta è mappata a un ID articolo nel tuo CMS.

## Informazioni sulle reti {#section_hqt_4m4_xz}

I clienti con più domini possono condividere gli account utente in tutti i domini, utilizzando una singola rete Livefyre. I clienti che desiderano mantenere account utente separati per domini diversi dovranno disporre di reti Livefyre separate.

Le impostazioni di configurazione possono essere applicate ai siti, alle reti e alle raccolte (in riferimento alla conversazione nell’illustrazione precedente).

>[!NOTE]
>
>Alcune impostazioni sono disponibili solo a livello di rete (come le preferenze per le notifiche e-mail, l’indirizzo e-mail e i loghi personalizzati e-mail). Se desideri che queste impostazioni siano diverse per ciascun dominio, devi utilizzare più reti.

## Informazioni sui siti {#section_vjw_nm4_xz}

Un sito è un raggruppamento arbitrario di articoli. Il raggruppamento è utile in quanto consente di assegnare moderatori diversi a diversi gruppi di contenuti. I moderatori e i proprietari possono essere impostati per moderare il contenuto e configurare le impostazioni dell&#39;amministratore a livello di rete o di sito. Se desideri che alcuni moderatori visualizzino solo alcune raccolte, queste raccolte possono essere configurate come sito Livefyre separato.

>[!NOTE]
>
>Non esiste alcun limite al numero di siti che si possono avere nella rete personalizzata.

## Diagramma della sequenza delle app {#section_mw2_lm4_xz}

Che tu stia cercando di implementare una funzione personalizzata con gli endpoint forniti da Livefyre o che tu debba semplicemente eseguire il debug di un problema, aiuta a capire come funziona il flusso di richieste/risposte dell’app Livefyre.

![](assets/appsequencediagram.png)

1. Quando il cliente accede al sito, crea un’istanza dell’app Livefyre con l’ID sito e l’ID articolo.
1. Se desideri autenticare l’utente (utile per la valutazione del traffico e per la protezione del sito), invia a Livefyre le informazioni sul sito e il token del profilo utente.
1. Invia a Livefyre l’ID sito e l’ID articolo per inizializzare l’app.

   Livefyre restituisce il contenuto iniziale.

   Invia questo contenuto alla pagina e visualizza l’app.

1. Per aggiornare il contenuto visualizzato nella pagina, invia a Livefyre l’ID evento più recente dalla pagina. Se è disponibile un nuovo contenuto, questo verrà restituito.

   Ricarica la pagina con nuovi contenuti e ripeti il processo a tempo indeterminato.

1. Se consenti agli utenti di pubblicare nuovi contenuti, attiva un evento quando nuovi contenuti vengono pubblicati sul tuo sito per pubblicare i contenuti su Livefyre. Livefyre restituirà un flusso aggiornato, che puoi utilizzare per aggiornare il tuo sito.
