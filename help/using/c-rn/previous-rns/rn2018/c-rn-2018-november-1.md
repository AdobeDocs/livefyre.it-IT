---
description: Note sulla versione per la versione del 1 novembre 2018.
seo-description: Note sulla versione per la versione del 1 novembre 2018.
seo-title: 1 novembre 2018
solution: Experience Manager
title: 1 novembre 2018
uuid: ed1a3bf1-b3f1-4746-8462-07283723ba62
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 3%

---


# 1° novembre 2018{#november}

Note sulla versione per la versione del 1 novembre 2018.

## Nuove funzionalità {#section_syx_mdt_wcb}

Nella versione di produzione di questa versione sono state rilasciate le seguenti nuove funzioni:

* Tag video avanzati

   Sfruttate la tecnologia di visione computerizzata avanzata, fornita da  Adobe Sensei, per assegnare automaticamente tag ai contenuti video al momento del salvataggio nella libreria. I tag avanzati consentono di gestire gli UGC in modo più efficace, ma anche di creare regole di cura (flussi) super precise che raccolgono i contenuti in base a quanto contenuto nel video, non solo al testo, risparmiando sforzi significativi nella moderazione dei contenuti indesiderati.

   Dettagli delle funzioni:

   * I tag avanzati vengono aggiunti automaticamente ai video ottenuti da ricerche social, flussi e file video caricati nella libreria. Visualizzare i tag nei dettagli delle risorse per un singolo video
   * Assegna tag ai video in formato MP4, MOV e AVI
   * Tag video fino a 60 secondi o 50 MB
   * Due categorie di smart tag si applicano ai video: caratteristiche (animali, oggetti, luoghi, ecc.) e azioni (corsa, passeggiate, canti, ecc.)

   Per ulteriori informazioni, vedere [Smart Tags](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md#c_smart_tags)

* Limitazione della tariffa Instagram

   Instagram ha modificato il numero di richieste che qualsiasi azienda che utilizza l&#39;API di Instagram, incluso Livefyre, può effettuare da 5.000 richieste all&#39;ora per token a 200 richieste all&#39;ora per token. Questa funzione è nota come *limite di velocità*. Per ulteriori informazioni, vedere [Limitazione della frequenza di Instagram](/help/using/c-streams/c-instagram-rate-limiting.md).

* File audio nella libreria

   Ora potete eseguire le seguenti funzioni sui file audio dal pannello Libreria:

   * Cerca
   * Anteprima
   * Importa
   * Filtrare per file audio
   * Trascinare i file nella finestra di progettazione

## Problemi {#section_ehw_ndt_wcb}

Non sono stati risolti nuovi problemi nella versione di produzione di questa versione. Vedere la sezione [sopra](#c_rn/section_syx_mdt_wcb).

## Rilascio UAT {#section_EE91B0C9313E45C5B4CBD59CFBCCFCFE}

I problemi riportati nelle tabelle seguenti sono stati risolti nella versione UAT di questa versione.

| **Tipo problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Miglioramento | GDPR | Tutti i dati attribuiti ai clienti precedenti in Analytics verranno eliminati. |
| Bug | Libreria | È stato corretto un problema a causa del quale un video caricato nella libreria e quindi visualizzato nei dettagli delle risorse non veniva visualizzato correttamente. |
| Bug | Mosaico | È stato risolto un problema a causa del quale un Mosaico visualizzava l&#39;ultimo contenuto di un carosello di Instagram come miniatura, invece che come scheda. |
| Bug | Ricerca social | È stato risolto un problema per il quale la ricerca social di Instagram non funzionava come previsto. |

