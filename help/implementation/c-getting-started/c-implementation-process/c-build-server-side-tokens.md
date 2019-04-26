---
description: Guida per la creazione di token collectionmeta e di autenticazione.
seo-description: Guida per la creazione di token collectionmeta e di autenticazione.
seo-title: Genera token lato server
solution: Experience Manager
title: Genera token lato server
uuid: 8313 f 26 e -5 ceb -414 e-a 61 a -480 bb 7 a 8 ba 66
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e

---


# Genera token lato server{#build-server-side-tokens}

Guida per la creazione di token collectionmeta e di autenticazione.

La creazione dei token utilizzati da Livefyre per convalidare le richieste assicura che solo tu effettui aggiornamenti alla rete Livefyre.

## Token collectionmeta

Scoprite come creare un token per creare nuove conversazioni e visualizzarle.

## Token di autenticazione

Scoprite come creare un token per l'autenticazione degli utenti, un passo necessario nel processo di integrazione se non utilizzate Janrain Capture per la gestione degli utenti.

## Token autenticazione utente {#section_l5l_hwt_bbb}

In questa sezione viene descritto come generare l'oggetto JSON userauth che crea il token di autenticazione utente richiesto per il registro degli utenti nelle app.

Per creare il token, usate la libreria preferita della lingua per passare i seguenti parametri:

| Parametro | Tipo | Descrizione |
|---|---|---|
| Networkname | Stringa *richiesta* | Nome della rete Livefyre (fornito da Livefyre). |
| Networkkey | Stringa *richiesta* | La chiave segreta per questa rete specifica (fornita da Livefyre). |
| Userid | Stringa *richiesta* | L'ID dell'utente che accede come memorizzato nel sistema di gestione degli utenti (sono consentiti solo i caratteri alfanumerici, trattini, di sottolineatura e punti): `[a-zA-Z0-9_-.]`). **Nota:** L'ID utente deve essere univoco. |
| expires | Numero intero *richiesto* | Quando il token scade da ora (in secondi). **Nota:** Questo valore può essere trasmesso anche come mobile. Il token Web JSON prodotto memorizzerà questo valore in ora epoch UNIX. |
| Displayname | Stringa *richiesta* | Testo per identificare questo utente nell'interfaccia utente e nei commenti. (Numero massimo di caratteri: 50.) |

