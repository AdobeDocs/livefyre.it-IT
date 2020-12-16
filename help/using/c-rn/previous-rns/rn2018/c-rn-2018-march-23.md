---
description: Note sulla versione per la release del 23 marzo 2018.
seo-description: Note sulla versione per la release del 23 marzo 2018.
seo-title: 23 marzo 2018
solution: Experience Manager
title: 23 marzo 2018
uuid: b69b8715-ace4-48e0-8f54-ce4e12170ef3
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 5%

---


# 23 marzo 2018{#march}

Note sulla versione per la release del 23 marzo 2018.

## Nuove funzionalità {#section_syx_mdt_wcb}

Le seguenti funzionalità sono nuove nella versione di produzione di questa versione:

* **Novità in produzione:** Facebook ha creato un aggiornamento di sicurezza per l&#39;accesso a Facebook che causerà il malfunzionamento dell&#39;accesso a Facebook di un cliente. Per risolvere il problema, è necessario:

   1. Aggiungete il seguente URL al campo **[!UICONTROL Valid OAuth redirect URIs]** in Impostazioni OAuth client. Sostituire `<networkname>` con il nome di rete corretto:
      `https://identity.livefyre.com/<networkname>/api/v1.0/public/profile/social/complete/facebook_fyre`

   1. Passare da **[!UICONTROL Use Strict Mode for Redirect URI]** a **[!UICONTROL Yes]**.

* **Novità in UAT:** ora potete scegliere la soglia di confidenza per gli smart tag nei flussi. L’impostazione del punteggio di precisione (0-100) per i tag consente di controllare l’accuratezza delle risorse recuperate.

## Problemi {#section_ehw_ndt_wcb}

In questa versione sono stati risolti i problemi riportati nelle tabelle seguenti.

## Release produzione

| **Tipo problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Bug | Muro di supporto | È stato risolto un problema in Media Wall a causa del quale non era possibile fare clic sui tag quando un post di Instagram veniva aggiunto da una regola di flusso. |
| Bug | ModQ | È stato risolto un problema che impediva il caricamento corretto di ModQ. |
| Bug | ModQ | È stato risolto un problema a causa del quale l’incorporamento dell’audio causava il blocco di ModQ. |

## Rilascio UAT

| **Tipo problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Miglioramento | Filmstrip | Sono stati risolti alcuni problemi per rendere più accessibile Filmstrip. |
| Miglioramento | Studio | Ora potete accedere a Livefyre utilizzando un login IMS. |

