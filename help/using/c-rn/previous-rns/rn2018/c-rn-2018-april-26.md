---
description: Note sulla versione per la release del 26 aprile 2018.
seo-description: Note sulla versione per la release del 26 aprile 2018.
seo-title: 26 aprile 2018
solution: Experience Manager
title: 26 aprile 2018
uuid: a84ebe5c-40d5-43b5-a300-3e041ab22046
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# April 26, 2018{#april}

Note sulla versione per la release del 26 aprile 2018.

## Nuove funzionalità {#section_syx_mdt_wcb}

Le seguenti funzionalità sono nuove nella versione di produzione di questa versione:

* È stata aggiunta una nuova funzione che consente ai clienti di configurare un numero specifico di colonne per un Media Wall. Il numero di colonne scelto imporrà la Muro multimediale a tale numero di colonne, indipendentemente dalle dimensioni. In caso contrario, il numero di colonne di Media Wall per impostazione predefinita è "auto", dove le colonne si adattano a un numero che ottimizza Media Wall per le dimensioni dello schermo.
* In Media Wall Designer è ora disponibile un interruttore che consente di disattivare l'animazione automatica di Media Wall che si verifica quando viene caricata una pagina con Media Wall.
* Ora potete scegliere la soglia di confidenza per gli smart tag nei flussi. L’impostazione del punteggio di precisione (0-100) per i tag consente di controllare l’accuratezza delle risorse recuperate.
* Aggiunte raccomandazioni di moderazione. Livefyre analizza ogni post in Apps per commenti e prevede se si desidera scaricarlo o meno in base ai dati storici e all'apprendimento automatico. Queste raccomandazioni vengono visualizzate in ModQ.
   * Gli utenti possono disattivare le raccomandazioni di moderazione, che consentono agli utenti di filtrare ModQ in base al contenuto che Livefyre pensa verrà eliminato.
   * Aggiunta la possibilità di filtrare ModQ in base al tag di raccomandazione di moderazione, Cestino.

## Problemi {#section_ehw_ndt_wcb}

In questa versione sono stati risolti i problemi riportati nelle tabelle seguenti.

## Release produzione

| **Tipo problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Bug | Rights Management | È stato corretto un problema a causa del quale le richieste di diritti non funzionavano per le risorse dopo averle trovate in una ricerca social network. |
| Miglioramento | Streams | È stato aggiornato il meccanismo di streaming che consente lo streaming dei contenuti da Facebook in conformità con una modifica back-end creata da Facebook. |
| Bug | Commerce UGC | È stato risolto un problema che impediva la visualizzazione del pulsante "Shop" CTA in un'app Mosaic o Filmstrip o in un modale di prodotti quando si passa il puntatore su una scheda con un prodotto quando il pulsante CTA è attivato. |
| Miglioramento | Commerce UGC | È stato risolto un problema per il quale il flag UGC Commerce era impostato su "off" per impostazione predefinita, invece di su "on". |

## Rilascio UAT

| **Tipo problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Bug | Libreria/Ricerca | È stato risolto un problema che impediva il caricamento corretto dei video. |
| Miglioramento | Studio | Aggiunta la possibilità di visualizzare le parole suggerite durante la digitazione nei nomi dei tag. |

