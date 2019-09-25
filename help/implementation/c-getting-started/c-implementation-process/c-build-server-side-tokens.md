---
description: Una guida per la creazione di token di autenticazione e raccoltaMeta.
seo-description: Una guida per la creazione di token di autenticazione e raccoltaMeta.
seo-title: Crea token lato server
solution: Experience Manager
title: Crea token lato server
uuid: 8313f26e-5ceb-414e-a61a-480bb7a8ba66
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e

---


# Crea token lato server{#build-server-side-tokens}

Una guida per la creazione di token di autenticazione e raccoltaMeta.

La creazione dei token utilizzati da Livefyre per convalidare le richieste garantisce che solo gli utenti possano effettuare aggiornamenti alla rete Livefyre.

## CollectionMeta Token

Scopri come creare un token per creare nuove conversazioni e visualizzarle.

## Token autenticazione

Scoprite come creare un token per l'autenticazione degli utenti, un passaggio necessario nel processo di integrazione se non utilizzate Janrain Capture per la gestione degli utenti.

## Token autenticazione utente {#section_l5l_hwt_bbb}

In questa sezione viene descritto come generare l'oggetto JSON UserAuth che crea il token di autenticazione utente richiesto per accedere agli utenti nelle app.

Per creare il token, usate la libreria delle lingue preferita per trasmettere i seguenti parametri:

| Parametro | Tipo | Descrizione |
|---|---|---|
| networkName | Stringa *richiesta* | Nome della rete Livefyre (fornito da Livefyre). |
| networkKey | Stringa *richiesta* | Chiave segreta per questa specifica rete (fornita da Livefyre). |
| userId | Stringa *richiesta* | L’ID dell’utente che accede come memorizzato nel sistema di gestione degli utenti (sono consentiti solo caratteri alfanumerici, trattini, caratteri di sottolineatura e punti): `[a-zA-Z0-9_-.]`). **** Nota: L'ID utente deve essere univoco. |
| expires | Numero intero *richiesto* | Quando il token deve scadere da ora (in secondi). **** Nota: Questo valore può anche essere passato come float. Il token Web JSON prodotto memorizzerà questo valore in tempo epoch UNIX. |
| displayName | Stringa *richiesta* | Testo per identificare questo utente nell’interfaccia utente e nei commenti. (Numero massimo di caratteri: 50) |

