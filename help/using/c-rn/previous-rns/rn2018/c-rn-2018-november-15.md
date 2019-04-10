---
description: Note sulla versione del 15 novembre 2018.
seo-description: Note sulla versione del 15 novembre 2018.
seo-title: Note sulla versione
solution: Experience Manager
title: Note sulla versione
uuid: 34 e 64943-dea 6-46 ac -9 fcc -8 febeab 6 aa 42
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Note sulla versione{#release-notes}

Note sulla versione del 15 novembre 2018.

## Nuove funzionalità {#section_syx_mdt_wcb}

Le seguenti nuove funzioni sono state rilasciate nella versione di produzione di questa versione:

* **Aggiornamenti alla ricerca e al flusso di istagram.** Potete utilizzare un *account business di Instagram* per:

   * Eseguite una ricerca social di Instagram per utente (l'utente deve essere anche un account business di Instagram).

   * Creare flussi Instagram da un account utente Instagram specifico (l'account deve anche essere un account aziendale), incluso il vostro.

   * Richiedete i diritti per le risorse di Instagram mediante un flusso di lavoro parzialmente automatizzato.

   * Per informazioni sul tipo di account Istagram necessario per configurare e richiedere i diritti da Instagram, consultate [Informazioni su Account Instagram](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md).

* **Il monitoraggio automatico dei diritti di utilizzo richiede risposte per le ricerche basate sull'account aziendale.** Solo per ricerche basate su account aziendali—È disponibile la capacità di monitorare automaticamente le risposte alle richieste di diritti e aggiornare la cronologia dell'attività in Livefyre.

Per ulteriori informazioni su come richiedere i diritti per gli account Instagram, consultate [Inviare manualmente la richiesta dei diritti di istagram](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md) e [Inviare una richiesta di Rights Rights parzialmente automatica](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md).

* **Integrazione di Adobe Target.** Integrazione con Adobe Target che consente di condividere le app Livefyre direttamente in Adobe Target Offers Library. Per ulteriori informazioni sull'utilizzo di Livefyre con Adobe Target, consulta [la documentazione di Target](https://marketing.adobe.com/resources/help/en_US/livefyre/livefyre-target.html).

## Problemi {#section_ehw_ndt_wcb}

I problemi delle tabelle seguenti sono stati risolti in questa versione.

### Versione produzione

| Tipo di edizione | Componente | Nota sulla versione |
|--- |--- |--- |
| Problema | Appservice: Livefyre Identity | È stato risolto un problema a causa del quale si faceva clic [su UICONTROL Reset to Default] did not reset the logo under Login Modal in Studio > Integration Settings > Livefyre Identity to the default image. |
| Problema | Libreria | È stato corretto un problema a causa del quale un video caricato nella libreria e visualizzato nei dettagli delle risorse non veniva visualizzato correttamente. |
| Problema | Flussi | È stato risolto un problema che impediva la visualizzazione dei prodotti in una regola di flusso. |
| Problema | Flussi | È stato risolto un problema per il quale i tag di prodotto non erano disponibili per una regola di flusso. |
| Miglioramento | Studio | È stato risolto un problema a causa del quale l'ID prodotto non veniva visualizzato in Livefyre Studio. |
| Problema | Studio: Modq | È stato risolto un problema che causava la visualizzazione del contenuto eliminato in modq dopo l'eliminazione. |

### Versione UAT

| **Tipo di edizione** | **Componente** | **Nota sulla versione** |
|---|---|---|
| Problema | Componente social: Carosello | Risolto un problema per il quale il collegamento Condividi non rispondeva e copiava l'URL come previsto in IE 11 e Mozilla Firefox. |