---
description: Note sulla versione per la versione del 23 marzo 2018.
title: 23 marzo 2018
exl-id: 85fd6f79-7fa8-425e-b4c7-2e1635d6ef17
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 5%

---

# 23 marzo 2018{#march}

Note sulla versione per la versione del 23 marzo 2018.

## Nuove funzionalità {#section_syx_mdt_wcb}

Le seguenti funzioni sono nuove nella versione di produzione di questa versione:

* **Novità in produzione:** Facebook ha creato un aggiornamento di sicurezza per l’accesso a Facebook che causerà il malfunzionamento dell’accesso a Facebook da parte di un cliente. Per risolvere questo problema, devi:

   1. Aggiungi il seguente URL al campo **[!UICONTROL Valid OAuth redirect URIs]** in Impostazioni OAuth client. Sostituisci `<networkname>` con il nome di rete corretto:
      `https://identity.livefyre.com/<networkname>/api/v1.0/public/profile/social/complete/facebook_fyre`

   1. Passa **[!UICONTROL Use Strict Mode for Redirect URI]** a **[!UICONTROL Yes]**.

* **Novità dell’UAT:** ora puoi scegliere la soglia di affidabilità per gli smart tag nei flussi. L’impostazione del punteggio di precisione (0-100) per i tag consente di controllare la precisione delle risorse recuperate.

## Problemi {#section_ehw_ndt_wcb}

I problemi nelle tabelle seguenti sono stati risolti in questa versione.

## Versione di produzione

| **Tipo di problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Bug | Parete multimediale | È stato risolto un problema in Media Wall a causa del quale i tag non potevano essere cliccati quando un post di Instagram veniva aggiunto da una regola di flusso. |
| Bug | ModQ | È stato risolto un problema a causa del quale ModQ non veniva caricato correttamente. |
| Bug | ModQ | È stato risolto un problema a causa del quale l’incorporazione dell’audio causava l’interruzione del funzionamento di ModQ. |

## Versione UAT

| **Tipo di problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Miglioramento | Filmstrip | Sono stati risolti alcuni problemi per rendere Filmstrip più accessibile. |
| Miglioramento | Studio | Ora puoi accedere a Livefyre utilizzando un accesso IMS. |
