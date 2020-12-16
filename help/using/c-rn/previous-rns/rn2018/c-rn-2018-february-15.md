---
description: Note sulla versione per la versione del 15 febbraio 2018.
seo-description: Note sulla versione per la versione del 15 febbraio 2018.
seo-title: 15 febbraio 2018
solution: Experience Manager
title: 15 febbraio 2018
uuid: ee46f088-9fb7-49e2-a42c-e0d4b2f24a32
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 4%

---


# 15 febbraio 2018{#february}

Note sulla versione per la versione del 15 febbraio 2018.

## Nuove funzionalità {#section_syx_mdt_wcb}

Le seguenti funzionalità sono nuove nella versione di produzione di questa versione:

* **Tag avanzati.**

   Livefyre utilizza  tecnologia di riconoscimento delle immagini Adobe Sensei per assegnare automaticamente tag alle immagini salvate nella libreria.
Con i tag avanzati è possibile risparmiare molto tempo durante la ricerca e la moderazione dei contenuti. Con i tag avanzati potete:

   * Cercare immagini salvate per ottenere contenuti precisi basati sul contenuto dell&#39;immagine, anziché solo testo
   * Raccogli contenuti in streaming in base a termini di ricerca precisi che analizzano l&#39;immagine, anziché solo testo

   Per ulteriori informazioni sui tag avanzati, vedere [Smart Tags](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md#c_smart_tags).

* **Messaggi interni al prodotto.** Ora, quando effettuate l&#39;accesso a Livefyre Studio, viene visualizzata una finestra di annunci per visualizzare gli aggiornamenti sulle nuove funzioni.
* **UGC per carosello.** Ora potete utilizzare tutte le funzioni di UGC Commerce nell&#39;app Livefyre Carousel. Puoi creare un pulsante Invito all’azione e collegare il catalogo prodotti all’app per creare un’esperienza di acquisto da Carosello.

## Problemi {#section_ehw_ndt_wcb}

In questa versione sono stati risolti i problemi riportati nelle tabelle seguenti.

## Release produzione

| **Tipo problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Problema | ModQ | È stato corretto un problema a causa del quale i post di Instagram contrassegnati come approvati o eliminati entravano nuovamente nella coda. |
| Miglioramento | Rights Management | È stato aggiunto un miglioramento per visualizzare un avviso quando si tenta di utilizzare gli account Instagram scaduti durante l&#39;esecuzione delle richieste di diritti. |
| Problema | Tendenze | È stato risolto un problema con l&#39;app Trends che consentiva comunque a volte HTTP anziché HTTPS. |

## Rilascio UAT

| **Tipo problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Miglioramento | App | Aggiunta la possibilità di eliminare le app da Livefyre. |
| Problema | Sondaggi | I sondaggi sono stati modificati per utilizzare esclusivamente HTTPS. Precedentemente, i sondaggi potevano ancora essere utilizzati con HTTP. |
| Problema | UGC | È stato risolto un problema che impediva agli UGC di un&#39;app di visualizzazione di filtrare in base all&#39;ID prodotto come previsto. |

