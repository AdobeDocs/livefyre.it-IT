---
description: Una guida per la creazione di token di raccoltaMeta e autenticazione.
title: Creare token lato server
exl-id: f709b79e-9236-443e-b862-c7d281815d91
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 1%

---

# Crea token lato server{#build-server-side-tokens}

Una guida per la creazione di token di raccoltaMeta e autenticazione.

La creazione dei token utilizzati da Livefyre per convalidare le richieste assicura che solo tu possa effettuare aggiornamenti alla tua rete Livefyre.

## Token CollectionMeta

Scopri come creare un token per creare conversazioni nuove e visualizzare quelle esistenti.

## Token di autenticazione

Scopri come creare un token per l’autenticazione degli utenti, un passaggio necessario nel processo di integrazione se non utilizzi Janrain Capture per la gestione degli utenti.

## Token di autenticazione utente {#section_l5l_hwt_bbb}

Questa sezione descrive come generare l’oggetto JSON UserAuth che crea il token di autenticazione utente necessario per accedere agli utenti nelle app.

Per creare il token, utilizza la libreria di lingue preferita per trasmettere i seguenti parametri:

| Parametro | Tipo | Descrizione |
|---|---|---|
| networkName | Stringa *obbligatoria* | Nome della rete Livefyre (fornito da Livefyre). |
| networkKey | Stringa *obbligatoria* | La chiave segreta per questa rete specifica (fornita da Livefyre). |
| userId | Stringa *obbligatoria* | L’ID dell’utente che effettua l’accesso come memorizzato nel sistema di gestione utenti (sono consentiti solo caratteri alfanumerici, trattini, caratteri di sottolineatura e punti): `[a-zA-Z0-9_-.]`). **Nota:** l&#39;ID utente deve essere univoco. |
| scadenza | Intero *obbligatorio* | Quando il token deve scadere da ora (in secondi). **Nota:** questo valore può anche essere passato come mobile. Il token web JSON prodotto memorizzerà questo valore in tempo epoca UNIX. |
| displayName | Stringa *obbligatoria* | Testo per identificare questo utente nell’interfaccia utente e nei commenti. (Numero massimo di caratteri: 50) |
