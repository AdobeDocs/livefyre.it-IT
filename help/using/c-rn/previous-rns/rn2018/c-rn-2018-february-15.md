---
description: Note sulla versione del 15 febbraio 2018.
title: 15 febbraio 2018
exl-id: 7276de37-c8cd-4e85-bc92-90c272e5bf94
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 4%

---

# 15 febbraio 2018{#february}

Note sulla versione del 15 febbraio 2018.

## Nuove funzionalità {#section_syx_mdt_wcb}

Le seguenti funzioni sono nuove nella versione di produzione di questa versione:

* **Tag avanzati.**

   Livefyre utilizza la tecnologia di riconoscimento delle immagini di Adobe Sensei per assegnare automaticamente tag alle immagini salvate nella libreria.
Con Tag avanzati è possibile risparmiare molto tempo nella ricerca e nella moderazione dei contenuti. Con i tag avanzati puoi:

   * Cerca immagini salvate per ottenere contenuti precisi basati sul contenuto dell&#39;immagine, anziché solo testo
   * Raccogli i contenuti nei flussi in base a termini di ricerca precisi che analizzano l&#39;immagine, anziché solo testo

   Per ulteriori informazioni sui tag avanzati, consulta [Tag avanzati](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md#c_smart_tags).

* **Messaggi interni al prodotto.** Ora, quando accedi a Livefyre Studio, viene visualizzata una finestra di annunci per visualizzare gli aggiornamenti sulle nuove funzioni.
* **UGC per carosello.** Ora puoi utilizzare tutte le funzioni di UGC Commerce nell’app Livefyre Carousel. Puoi creare un pulsante di invito all’azione e collegare il catalogo dei prodotti all’app per creare un’esperienza acquistabile da Carosello.

## Problemi {#section_ehw_ndt_wcb}

I problemi nelle tabelle seguenti sono stati risolti in questa versione.

## Versione di produzione

| **Tipo di problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Problema | ModQ | È stato risolto un problema a causa del quale i post Instagram contrassegnati come approvati o eliminati venivano reinseriti nella coda. |
| Miglioramento | Rights Management | È stato aggiunto un miglioramento per visualizzare un avviso quando si tenta di utilizzare account Instagram scaduti durante l’esecuzione di richieste di diritti. |
| Problema | Tendenze | È stato risolto un problema con l’app Trends che a volte consentiva comunque l’accesso a HTTP anziché HTTPS. |

## Versione UAT

| **Tipo di problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Miglioramento | App | Aggiunta la possibilità di eliminare le app da Livefyre. |
| Problema | Sondaggi | I sondaggi sono stati modificati per utilizzare esclusivamente HTTPS. In precedenza, i sondaggi potevano ancora essere utilizzati con HTTP. |
| Problema | UGC | È stato risolto un problema a causa del quale gli UGC in un’app di visualizzazione non filtravano per ID prodotto come previsto. |
