---
description: Scoprite le convenzioni di Livefyre e il modo in cui Livefyre organizza
  i contenuti.
seo-description: Scoprite le convenzioni di Livefyre e il modo in cui Livefyre organizza
  i contenuti.
seo-title: Architettura
solution: Experience Manager
title: Architettura
uuid: 94358 e 6 c -954 a -4 a 52-9 bb 2-d 800 b 2933130
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Architettura{#architecture}

Scoprite le convenzioni di Livefyre e il modo in cui Livefyre organizza i contenuti.

Questa sezione fornisce una panoramica di Livefyre Network Architecture.

## Panoramica su reti e siti

Livefyre organizza utenti e contenuti per rete e sito. A ogni rete possono essere associati uno o più account utente e ogni rete può includere uno o più siti Livefyre. Un sito Livefyre è un gruppo arbitrario di raccolte. Una raccolta viene mappata su un ID articolo nel CMS.

## Informazioni sulle reti {#section_hqt_4m4_xz}

I clienti con più domini possono condividere gli account utente in tutti i domini, utilizzando una sola rete Livefyre. I clienti che desiderano conservare account utente separati per domini diversi dovranno disporre di reti Livefyre separate.

Le impostazioni di configurazione possono essere applicate a siti, reti e raccolte (a cui si fa riferimento come conversazione nell'illustrazione precedente).

>[!NOTE]
>
>Alcune impostazioni sono disponibili solo a livello di rete (ad esempio, preferenze di notifica e-mail, indirizzo e-mail dall'indirizzo e logo personalizzati tramite e-mail). Se desiderate che queste impostazioni siano diverse per ciascun dominio, dovete utilizzare più reti.

## Informazioni sui siti {#section_vjw_nm4_xz}

Un sito è un gruppo arbitrario di articoli. Il raggruppamento è utile in quanto consente di assegnare diversi moderatori a diversi gruppi di contenuto. I moderatori e i proprietari possono essere configurati per moderare il contenuto e configurare le impostazioni di amministrazione a livello di rete o di sito. Se desiderate che alcuni moderatori vedano solo determinate raccolte, queste raccolte possono essere configurate come un sito Livefyre separato.

>[!NOTE]
>
>Non esiste alcun limite al numero di siti che potresti avere nella tua rete personalizzata.

## Diagramma sequenza app {#section_mw2_lm4_xz}

Sia che stiate cercando di implementare funzioni personalizzate con gli endpoint forniti con Livefyre, o che dobbiate semplicemente eseguire il debug di un problema, è utile capire in che modo funziona il flusso di richiesta/risposta dell'app Livefyre.

![](assets/appsequencediagram.png)

1. Quando il client raggiunge il sito, istanziate l'app Livefyre con l'ID sito e l'ID articolo.
1. Se desiderate autenticare l'utente (utile per la valutazione del traffico e la protezione del sito), inviate Livefyre le informazioni sul sito e il token Profilo utente.
1. Inviate Livefyre l'ID sito e l'ID articolo per inizializzare l'app.

   Livefyre restituisce il contenuto iniziale.

   Inviate il contenuto alla pagina e visualizzate l'app.

1. Per aggiornare il contenuto visualizzato sulla pagina, inviate Livefyre l'ID evento più recente dalla pagina. Se è disponibile un nuovo contenuto, verrà restituito.

   Ricaricate la pagina con nuovi contenuti e ripetete il processo a tempo indefinito.

1. Se consentite agli utenti di pubblicare nuovi contenuti, attivate un evento quando pubblicate nuovi contenuti sul sito per pubblicare il contenuto in Livefyre. Livefyre restituirà un flusso aggiornato, che potete utilizzare per aggiornare il sito.
