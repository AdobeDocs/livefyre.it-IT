---
description: Note sulla versione per la versione dell’8 marzo 2018.
seo-description: Note sulla versione per la versione dell’8 marzo 2018.
seo-title: 8 marzo 2018
solution: Experience Manager
title: 8 marzo 2018
uuid: 4ed67147-0837-4d5e-8e99-532a4278bcce
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 4%

---


# 8 marzo 2018{#march}

Note sulla versione per la versione dell’8 marzo 2018.

## Nuove funzionalità {#section_syx_mdt_wcb}

Le seguenti funzionalità sono nuove nella versione di produzione di questa versione:

* **Eliminazione delle app. **Aggiunta la possibilità di eliminare le app in Studio per consentire agli utenti di gestire meglio l&#39;elenco delle app. L&#39;eliminazione di un&#39;app la rimuove dalla tabella, ma non rimuove l&#39;app dal sito. L&#39;app continuerà a ricevere contenuto da uno streaming, se è configurata per farlo.

## Problemi {#section_ehw_ndt_wcb}

In questa versione sono stati risolti i problemi riportati nelle tabelle seguenti.

## Release produzione

| **Tipo problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Bug | Sondaggi | I sondaggi sono stati modificati per utilizzare esclusivamente HTTPS. Precedentemente, i sondaggi potevano ancora essere utilizzati con HTTP. |
| Bug | Studio | È stato risolto un problema che causava la visualizzazione di annunci nella finestra modale quando si accedeva a Studio su schermi a bassa risoluzione troppo grandi. |

## Rilascio UAT

| Tipo problema | Componente | Note sulla versione |
|--- |--- |--- |
| Miglioramento | Filmstrip | Sono state aggiornate le seguenti funzioni di accessibilità per Filmstrip: <br><ul><li>Frecce sinistra/destra corrette da &lt;div> a &lt;pulsante> </li><li>L’elemento di anteprima dell’immagine è stato modificato da un’etichetta ARIA meno descrittiva di &quot;Apri foto allegata&quot; a un’etichetta che legge il nome della piattaforma e il testo del post.</li></ul> |
| Bug | Muro di supporto | È stato risolto un problema in Media Wall a causa del quale non era possibile fare clic sui tag quando un post di Instagram veniva aggiunto da una regola di flusso. |
| Miglioramento | Muro di supporto | Miglioramento dell&#39;accessibilità di Media Wall nei seguenti modi: <br><ul><li>L&#39;apertura e la chiusura dei modelli tramite comandi da tastiera non consentono più di spostare lo stato attivo nella parte superiore della pagina. Rimane invece attivo sull&#39;ultimo elemento attivo prima della finestra a comparsa modale.</li><li>Il pulsante Carica altro può essere premuto con il tasto Invio della tastiera.</li></ul> |
| Bug | Rights Management | È stato corretto un errore che impediva la visualizzazione modale della richiesta di diritti dopo la concessione dei diritti per una risorsa Instagram. |

