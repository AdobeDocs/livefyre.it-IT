---
description: Note sulla versione per la versione dell’8 marzo 2018.
title: 8 marzo 2018
exl-id: 46d4a425-17e0-48a2-a596-5cc7163f9edd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 4%

---

# 8 marzo 2018{#march}

Note sulla versione per la versione dell’8 marzo 2018.

## Nuove funzionalità {#section_syx_mdt_wcb}

Le seguenti funzioni sono nuove nella versione di produzione di questa versione:

* **Eliminazione delle app. **Aggiunta la possibilità di eliminare le app in Studio per consentire agli utenti di gestire meglio l’elenco delle app. Se elimini un&#39;app, questa viene rimossa dalla tabella, ma non dal sito. L’app continuerà a ricevere contenuto da un flusso se è configurata per farlo.

## Problemi {#section_ehw_ndt_wcb}

I problemi nelle tabelle seguenti sono stati risolti in questa versione.

## Versione di produzione

| **Tipo di problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Bug | Sondaggi | I sondaggi sono stati modificati per utilizzare esclusivamente HTTPS. In precedenza, i sondaggi potevano ancora essere utilizzati con HTTP. |
| Bug | Studio | È stato risolto un problema che causava la visualizzazione di annunci nella finestra modale visualizzata quando si effettuava l’accesso a Studio in modo da visualizzare troppo grandi su schermi a bassa risoluzione. |

## Versione UAT

| Tipo di problema | Componente | Note sulla versione |
|--- |--- |--- |
| Miglioramento | Filmstrip | Sono state aggiornate le seguenti funzioni di accessibilità per Filmstrip: <br><ul><li>Frecce sinistra/destra corrette da &lt;div> a &lt;button> </li><li>L&#39;elemento di anteprima dell&#39;immagine è stato modificato da un&#39;etichetta ARIA meno descrittiva di, &quot;Apri foto allegata&quot;, a un&#39;etichetta che legge il nome della piattaforma e il testo del post.</li></ul> |
| Bug | Parete multimediale | È stato risolto un problema in Media Wall a causa del quale i tag non potevano essere cliccati quando un post di Instagram veniva aggiunto da una regola di flusso. |
| Miglioramento | Parete multimediale | Miglioramento dell’accessibilità di Media Wall nei seguenti modi: <br><ul><li>L’apertura e la chiusura dei moduli tramite comandi da tastiera non consentono più di tornare a essere attivi nella parte superiore della pagina. Al contrario, l&#39;elemento rimane concentrato per l&#39;ultimo periodo prima della finestra a comparsa modale.</li><li>Il pulsante Carica altro può essere collegato e attivato utilizzando il tasto Invio della tastiera.</li></ul> |
| Bug | Rights Management | È stato corretto un errore che impediva la visualizzazione modale della richiesta di diritti dopo la concessione dei diritti per una risorsa Instagram. |
