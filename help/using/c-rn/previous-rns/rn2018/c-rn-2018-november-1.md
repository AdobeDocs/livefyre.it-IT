---
description: Note sulla versione per la versione del 1° novembre 2018.
title: 1 novembre 2018
exl-id: b12b6a56-f14f-4447-9fde-25cb3acf6665
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 3%

---

# 1° novembre 2018{#november}

Note sulla versione per la versione del 1° novembre 2018.

## Nuove funzionalità {#section_syx_mdt_wcb}

Nella versione di produzione di questa versione sono state rilasciate le seguenti nuove funzioni:

* Tag video avanzati

   Sfrutta la tecnologia avanzata di visione dei computer, basata su Adobe Sensei, per assegnare automaticamente tag ai contenuti video quando li salvi nella libreria. I tag avanzati consentono di gestire gli UGC in modo più efficace, ma anche di creare regole di cura super precise (flussi) che raccolgono i contenuti in base a ciò che si trova nel video, non solo al testo, risparmiando un notevole sforzo nella moderazione dei contenuti indesiderati.

   Dettagli delle funzioni:

   * I tag avanzati vengono aggiunti automaticamente ai video ottenuti da ricerche social, flussi e file video caricati nella libreria. Visualizzare i tag nei dettagli della risorsa per un singolo video
   * Assegna tag ai video in formato .MP4, .MOV e AVI
   * Assegna tag ai video fino a 60 secondi o 50 MB
   * Ai video sono applicabili due categorie di tag avanzati: caratteristiche (animali, oggetti, luoghi, ecc.) e azioni (corse, passeggiate, canti, ecc.)

   Per ulteriori informazioni, consulta [Tag avanzati](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md#c_smart_tags)

* Limitazione della velocità di Instagram

   Instagram ha modificato il numero di richieste che qualsiasi azienda che utilizzi l’API Instagram, incluso Livefyre, può effettuare da 5.000 richieste all’ora per token a 200 richieste all’ora per token. Questo è noto come *limite di velocità*. Per ulteriori informazioni, consulta [Limitazione velocità Instagram](/help/using/c-streams/c-instagram-rate-limiting.md).

* File audio nella libreria

   È ora possibile eseguire le seguenti funzioni sui file audio dal pannello libreria:

   * Cerca
   * Anteprima
   * Importa
   * Filtrare per file audio
   * Trascina e rilascia i file nella finestra di progettazione

## Problemi {#section_ehw_ndt_wcb}

Non sono stati risolti nuovi problemi nella versione di produzione di questa versione. Vedi la sezione [sopra](#c_rn/section_syx_mdt_wcb).

## Rilascio UAT {#section_EE91B0C9313E45C5B4CBD59CFBCCFCFE}

I problemi nelle tabelle seguenti sono stati risolti nella versione UAT di questa versione.

| **Tipo di problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Miglioramento | GDPR | Tutti i dati attribuiti ai clienti precedenti in Analytics verranno eliminati. |
| Bug | Libreria | È stato risolto un problema che impediva la corretta visualizzazione di un video caricato nella libreria e visualizzato nei dettagli della risorsa. |
| Bug | Mosaico | È stato risolto un problema a causa del quale un Mosaic visualizzava l&#39;ultimo contenuto di un carosello Instagram come miniatura, invece di una scheda. |
| Bug | Ricerca social | È stato risolto un problema a causa del quale la ricerca social di Instagram non funzionava come previsto. |
