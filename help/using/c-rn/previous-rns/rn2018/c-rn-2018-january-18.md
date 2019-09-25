---
description: Note sulla versione per la versione del 18 gennaio 2018.
seo-description: Note sulla versione per la versione del 18 gennaio 2018.
seo-title: 18 gennaio 2018
solution: Experience Manager
title: 18 gennaio 2018
uuid: 8141f431-c154-4c8f-bcd-b7c712fe5f7d
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# January 18, 2018{#january}

Note sulla versione per la versione del 18 gennaio 2018.

## Release produzione

| **Tipo problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Bug | App | È stato corretto un bug che impediva il corretto rendering degli Avatar in caso di utilizzo di un file jpeg. |
| Bug | ModQ | È stato corretto un bug che consentiva ai clienti S1 di filtrare in base alle raccolte in ModQ. |
| Bug | Streams | È stato corretto un bug a causa del quale una regola di flusso veniva interrotta quando il filtro della lingua era impostato su "none". |
| Bug | Streams | È stato corretto un bug che impediva il salvataggio delle regole del flusso di YouTube. |
| Bug | Streams | È stato corretto un bug a causa del quale gli utenti potevano creare delle voci geografiche con formattazione errata nelle regole del flusso e salvarle, il che causava un errore nel flusso. Ora, gli utenti non possono più salvare i tag geografici in formato errato. |
| Bug | Studio | È stato risolto un problema che impediva ad alcuni utenti di accedere a Livefyre. |

## Rilascio UAT

| **Tipo problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Bug | Libreria | Correzione dei bug di sicurezza. Tutte le chiamate di autenticazione ora vengono effettuate utilizzando il protocollo HTTPS invece di HTTP. |
| Miglioramento | Tag avanzati | I contenuti in streaming vengono ora automaticamente contrassegnati con smart tag da Adobe Sensei mentre vengono salvati in una cartella o pubblicati in un'app. |
| Bug | Streams | È stato risolto un problema per cui le regole del flusso Instagram non riconoscevano i caratteri giapponesi. |
| Miglioramento | Streams | I clienti possono ora utilizzare gli operatori logici (ANY, ALL, NOT) per creare filtri smart tag dettagliati nei flussi che curano contenuti molto più precisi. Ad esempio, se uso l'hashtag #himalyas, posso scegliere di mostrare solo immagini che includono "montagne nevose". |
| Bug | Studio | Correzione di un bug che mostrava caratteri speciali nei nomi come HTML. |

