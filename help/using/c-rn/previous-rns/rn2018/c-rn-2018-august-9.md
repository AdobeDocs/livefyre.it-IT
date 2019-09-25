---
description: Note sulla versione per la versione del 9 agosto 2018.
seo-description: Note sulla versione per la versione del 9 agosto 2018.
seo-title: 9 agosto 2018
solution: Experience Manager
title: 9 agosto 2018
uuid: c59ae5ec-9d26-41c4-9a98-cb95c89ee26a
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# 9 agosto 2018{#august}

Note sulla versione per la versione del 9 agosto 2018.

## Nuove funzionalità {#section_syx_mdt_wcb}

**** Tag video avanzati: Gli utenti possono ora visualizzare gli smart tag per i video con meno di 50 MB.

## Problemi {#section_ehw_ndt_wcb}

In questa versione sono stati risolti i problemi riportati nelle tabelle seguenti.

## Release produzione

| **Tipo problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Bug | Contenuto app | È stato risolto un problema che impediva agli amministratori e ai manager del contenuto di modificare il contenuto in Contenuto app. |
| Miglioramento | App | I social network hanno modificato la privacy, il che significa che le menzioni social non saranno più supportate per Facebook o Twitter. |
| Miglioramento | App | I social network hanno modificato la privacy. La funzione "Post To" che pubblica automaticamente i contenuti sui social network (Facebook, LinkedIn, Twitter) è stata rimossa. |
| Miglioramento | GDPR | È stato rimosso l’interruttore per la modalità dettagli dalla pagina dei dettagli della richiesta in Impostazioni &gt; Privacy. È ancora possibile accedere alla modalità Dettagli aggiungendo /dbg alla fine dell’URL. |
| Bug | Integrazione: AEM | È stato risolto un problema a causa del quale il trascinamento delle app Livefyre in AEM sembrava creare più app. |
| Bug | Libreria | È stato corretto un problema a causa del quale una risorsa non veniva salvata correttamente nella libreria. |
| Bug | Identità Livefyre | È stato risolto un problema con l'identità LF che causava 403 errori durante l'accesso. |
| Bug | Ricerca social | È stato risolto un problema che impediva agli utenti di cercare post pubblici su Facebook utilizzando l'opzione URL in Social Search. |
| Miglioramento | Social Sync | I social network hanno apportato modifiche alla privacy che significano che Social Sync non sarà più supportato per Facebook. |
| Miglioramento | Streams | Ora, quando elimini un'app, elimina tutti i flussi associati a tale app. |
| Miglioramento | Studio | I clienti ora possono emettere eventi Livefyre singolarmente in Adobe Analytics anziché in batch. |
| Miglioramento | Studio | Le finestre modali che vengono visualizzate nelle app di conversazione per i social network ora saranno finestre modali dal social network invece di Adobe Experience Manager Livefyre o altre finestre modali con il marchio. |

## Rilascio UAT

I problemi riportati nelle tabelle seguenti sono stati risolti nella versione UAT.

| **Tipo problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Bug | GDPR | È stato risolto un problema che impediva la visualizzazione dei messaggi di rifiuto per alcuni video di Instagram. |
| Bug | Libreria | È stato risolto un problema che causava la visualizzazione manuale dello stato errato della richiesta di diritti da parte di una scheda con diritti assegnati. |
| Bug | Libreria | È stato risolto un problema che impediva il salvataggio di una risorsa in una cartella. |
| Bug | Libreria/Ricerca | È stata ripristinata la possibilità di cercare URL da Instagram in Social Search. |
| Bug | ModQ | È stato risolto un problema per il quale il menu Ulteriori informazioni in ModQ non veniva visualizzato dove previsto. |
| Bug | Rights Management | È stato corretto un problema a causa del quale l'ordinamento in ModQ deve trovarsi in una posizione fissa quando la pagina scorre. |
| Bug | Streams | È stato risolto un problema con la visualizzazione dei flussi nell'ambiente di staging. |
| Miglioramento | Streams | È stato aggiunto l’interruttore Safe For Work (SFW) e Not Safe For Work (NSFW) ai flussi. |
| Miglioramento | Studio | Funzionalità smart tag aggiunta al contenuto caricato nella libreria Livefyre Studio tramite FileStack (funzionalità di caricamento in Tutte le risorse). |

