---
description: Note sulla versione del 26 aprile 2018.
seo-description: Note sulla versione del 26 aprile 2018.
seo-title: 26 aprile 2018
solution: Experience Manager
title: 26 aprile 2018
uuid: a 84 ebe 5 c -40 d 5-43 b 5-a 300-3 e 041 ab 22046
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 26 aprile 2018{#april}

Note sulla versione del 26 aprile 2018.

## Nuove funzionalità {#section_syx_mdt_wcb}

Le seguenti funzionalità sono nuove nella versione di produzione di questa versione:

* Aggiunta di una nuova funzione che consente ai clienti di configurare un numero specifico di colonne per un Media Wall. Il numero di colonne scelto forza la suddivisione della Media Wall in quel numero di colonne, indipendentemente dalle dimensioni. In caso contrario, il numero di colonne di Media Wall predefinito è «auto» in cui le colonne vengono regolate su un numero che ottimizza Media Wall per le dimensioni dello schermo.
* In Media Wall Designer è ora disponibile un interruttore che consente di disattivare l'animazione automatica di Media Wall che si verifica quando si carica una pagina con contenuti multimediali.
* Ora potete scegliere la soglia di confidenza per i tag avanzati nei flussi. L'impostazione della valutazione di precisione (0-100) per i tag consente di controllare la precisione delle risorse che stiamo recuperando.
* Aggiunte raccomandazioni di moderazione. Livefyre analizza ogni post nel commento delle app e spiega se effettuerai il cestino o meno in base a dati storici e machine learning. Queste raccomandazioni vengono visualizzate in modq.
   * Gli utenti possono disattivare le raccomandazioni di moderazione, che consentono agli utenti di filtrare modq dal contenuto Livefyre pensate che effettuerete il cestino.
   * Aggiunta la capacità di filtrare modq dal tag di raccomandazione moderazione, Cestino.

## Problemi {#section_ehw_ndt_wcb}

I problemi delle tabelle seguenti sono stati risolti in questa versione.

## Versione produzione

| **Tipo di edizione** | **Componente** | **Nota sulla versione** |
|---|---|---|
| Bug | Rights Management | È stato risolto un problema a causa del quale le richieste di diritti non funzionavano per le risorse dopo averle individuate in una ricerca social network. |
| Miglioramento | Flussi | È stato aggiornato il meccanismo di streaming che consente il flusso del contenuto da Facebook in conformità con una modifica back-end creata da Facebook. |
| Bug | UGC Commerce | Risolto un problema per il quale il pulsante "Negozio" CTA non veniva visualizzato in un'app Mosaic o Filmstrip oppure in un modale di prodotti quando si passava il cursore su una scheda con un prodotto quando il pulsante CTA era abilitato. |
| Miglioramento | UGC Commerce | È stato risolto un problema per il quale il flag UGC Commerce veniva impostato su "off" per impostazione predefinita, anziché su "on". |

## Versione UAT

| **Tipo di edizione** | **Componente** | **Nota sulla versione** |
|---|---|---|
| Bug | Libreria/Ricerca | È stato corretto un problema a causa del quale i video non venivano caricati correttamente. |
| Miglioramento | Studio | Aggiunta la possibilità di visualizzare parole suggerite durante la digitazione nei nomi dei tag. |

