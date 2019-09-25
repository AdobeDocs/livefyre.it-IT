---
description: Note sulla versione per la versione del 15 novembre 2018.
seo-description: Note sulla versione per la versione del 15 novembre 2018.
seo-title: Note sulla versione
solution: Experience Manager
title: Note sulla versione
uuid: 34e64943-dea6-46ac-9fcc-8febeab6aa42
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# Note sulla versione{#release-notes} 

Note sulla versione per la versione del 15 novembre 2018.

## Nuove funzionalità {#section_syx_mdt_wcb}

Nella versione di produzione di questa versione sono state rilasciate le seguenti nuove funzioni:

* **Aggiornamenti alla ricerca e allo streaming di Instagram.** Puoi utilizzare un account *aziendale* Instagram per:

   * Effettuate una ricerca tramite social network Instagram per utente (l'utente deve essere anche un account aziendale di Instagram).

   * Crea flussi Instagram da un account utente Instagram specifico (l'account deve anche essere un account aziendale), incluso il tuo.

   * Richiedete i diritti per le risorse da Instagram tramite un flusso di lavoro parzialmente automatizzato.

   * Per informazioni sul tipo di account Instagram da impostare e richiedere i diritti da Instagram, consultate [Informazioni sugli account](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md)Instagram.

* **Monitoraggio automatico delle risposte delle richieste di diritti di utilizzo per ricerche basate su account aziendali.** Solo per ricerche basate su account aziendali, è disponibile la possibilità di monitorare automaticamente le risposte alle richieste di diritti e aggiornare la cronologia delle attività in Livefyre.

Per ulteriori informazioni su come richiedere i diritti per gli account Instagram, consultate [Inviare manualmente](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md) le richieste di diritti Instagram e [Inviare una richiesta](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md)di diritti Instagram parzialmente automatizzata.

* **Integrazione di Adobe Target.** È stata aggiunta l'integrazione con Adobe Target per la condivisione di app Livefyre direttamente nella libreria delle offerte di Adobe Target. Per ulteriori informazioni sull'utilizzo di Livefyre con Adobe Target, consultate la documentazione [di](https://marketing.adobe.com/resources/help/en_US/livefyre/livefyre-target.html)Target.

## Problemi {#section_ehw_ndt_wcb}

In questa versione sono stati risolti i problemi riportati nelle tabelle seguenti.

### Release produzione

| Tipo problema | Componente | Note sulla versione |
|--- |--- |--- |
| Problema | AppService:Identità Livefyre | È stato risolto un problema per cui si faceva clic su [! UICONTROL Reset to Default] non ha reimpostato il logo in Modalità di accesso in Studio &gt; Impostazioni di integrazione &gt; Identità Livefyre sull'immagine predefinita. |
| Problema | Libreria | È stato corretto un problema a causa del quale un video caricato nella libreria e quindi visualizzato nei dettagli delle risorse non veniva visualizzato correttamente. |
| Problema | Streams | È stato risolto un problema che impediva la visualizzazione dei prodotti in una regola di flusso. |
| Problema | Streams | È stato risolto un problema per il quale i tag prodotto non erano disponibili per una regola di flusso. |
| Miglioramento | Studio | È stato risolto un problema che impediva la visualizzazione dell'ID prodotto in Livefyre Studio. |
| Problema | Studio:ModQ | È stato risolto un problema che causava la visualizzazione del contenuto eliminato in ModQ dopo l’eliminazione. |

### Rilascio UAT

| **Tipo problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Problema | Componente social:Carosello | È stato risolto un problema a causa del quale il collegamento Condivisione non rispondeva e copiava l'URL come previsto in IE11 e Mozilla Firefox. |