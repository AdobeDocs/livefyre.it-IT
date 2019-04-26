---
description: Note sulla versione del 23 marzo 2018.
seo-description: Note sulla versione del 23 marzo 2018.
seo-title: 23 marzo 2018
solution: Experience Manager
title: 23 marzo 2018
uuid: b 69 b 8715-ace 4-48 e 0-8 f 54-ce 4 e 12170 ef 3
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# 23 marzo 2018{#march}

Note sulla versione del 23 marzo 2018.

## Nuove funzionalità {#section_syx_mdt_wcb}

Le seguenti funzionalità sono nuove nella versione di produzione di questa versione:

* **Novità in Produzione:** Facebook ha creato un aggiornamento di sicurezza all'accesso Facebook che causerà il malfunzionamento di Facebook Login di Facebook. Per risolvere questo problema dovete:

   1. Aggiungi il seguente URL al **[!UICONTROL Valid OAuth redirect URIs]** campo in Impostazioni client oauth. Sostituite `<networkname>` con il nome di rete corretto:
      `https://identity.livefyre.com/<networkname>/api/v1.0/public/profile/social/complete/facebook_fyre`

   1. Passa **[!UICONTROL Use Strict Mode for Redirect URI]****[!UICONTROL Yes]**a.

* **Nuovo nell'UAT:** Ora potete scegliere la soglia di confidenza per i tag avanzati nei flussi. L'impostazione della valutazione di precisione (0-100) per i tag consente di controllare la precisione delle risorse che stiamo recuperando.

## Problemi {#section_ehw_ndt_wcb}

I problemi delle tabelle seguenti sono stati risolti in questa versione.

## Versione produzione

| **Tipo di edizione** | **Componente** | **Nota sulla versione** |
|---|---|---|
| Bug | Media Wall | È stato risolto un problema in Media Wall che impediva ai tag di fare clic quando un post di Instagram veniva aggiunto da una regola di flusso. |
| Bug | Modq | Risolto un problema che impediva il caricamento di modq. |
| Bug | Modq | Risolto un problema per il quale l'incorporazione dell'audio causava la cessazione di modq. |

## Versione UAT

| **Tipo di edizione** | **Componente** | **Nota sulla versione** |
|---|---|---|
| Miglioramento | Filmstrip | Sono stati corretti alcuni problemi per rendere Filmstrip più accessibile. |
| Miglioramento | Studio | Ora potete accedere a Livefyre utilizzando un login IMS. |

