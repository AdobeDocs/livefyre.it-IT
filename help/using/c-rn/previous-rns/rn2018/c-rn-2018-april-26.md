---
description: Note sulla versione per la versione del 26 aprile 2018.
title: 26 aprile 2018
exl-id: af0ee64d-d60c-4b21-a628-08848313781c
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 3%

---

# 26 aprile 2018{#april}

Note sulla versione per la versione del 26 aprile 2018.

## Nuove funzionalità {#section_syx_mdt_wcb}

Le seguenti funzioni sono nuove nella versione di produzione di questa versione:

* È stata aggiunta una nuova funzione che consente ai clienti di configurare un numero specifico di colonne per una parete multimediale. Il numero di colonne scelto forza la Muro multimediale in quel numero di colonne, indipendentemente dalle dimensioni. In caso contrario, il numero di colonne di Media Wall per impostazione predefinita è &quot;auto&quot;, dove le colonne si regolano su un numero che ottimizza Media Wall per le dimensioni dello schermo.
* In Media Wall Designer è ora disponibile un&#39;opzione che consente di disattivare l&#39;animazione automatica Media Wall che si verifica quando viene caricata una pagina con Media Wall.
* Ora puoi scegliere la soglia di affidabilità per gli smart tag nei flussi. L’impostazione del punteggio di precisione (0-100) per i tag consente di controllare la precisione delle risorse recuperate.
* Sono stati aggiunti consigli di moderazione. Ora Livefyre analizza ogni post in Apps per commentare e prevede se lo scaricherà o meno in base ai dati storici e all&#39;apprendimento automatico. Queste raccomandazioni vengono visualizzate in ModQ.
   * Gli utenti possono disattivare i consigli di moderazione, che consentono agli utenti di filtrare ModQ in base al contenuto che Livefyre pensa che trascriverai.
   * È stata aggiunta la possibilità di filtrare ModQ per il tag di raccomandazione di moderazione, Cestino.

## Problemi {#section_ehw_ndt_wcb}

I problemi nelle tabelle seguenti sono stati risolti in questa versione.

## Versione di produzione

| **Tipo di problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Bug | Rights Management | È stato risolto un problema a causa del quale le richieste di diritti non funzionavano per le risorse dopo averle trovate in una ricerca social. |
| Miglioramento | Flussi | È stato aggiornato il meccanismo di streaming che consente lo streaming dei contenuti da Facebook in conformità a una modifica back-end creata da Facebook. |
| Bug | Commerce UGC | È stato risolto un problema che impediva la visualizzazione del pulsante CTA &quot;Shop&quot; in un’app Mosaic o Filmstrip o in un prodotto modale quando si passava il mouse su una scheda con un prodotto quando il pulsante CTA era abilitato. |
| Miglioramento | Commerce UGC | È stato risolto un problema per cui il flag Commerce UGC era impostato su &quot;off&quot; per impostazione predefinita, invece di &quot;on&quot;. |

## Versione UAT

| **Tipo di problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Bug | Libreria/Ricerca | È stato risolto un problema che impediva il caricamento corretto dei video. |
| Miglioramento | Studio | Aggiunta la possibilità di visualizzare le parole suggerite durante la digitazione dei nomi dei tag. |
