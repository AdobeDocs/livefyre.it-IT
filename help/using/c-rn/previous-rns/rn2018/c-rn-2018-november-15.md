---
description: Note sulla versione del 15 novembre 2018.
title: Note sulla versione
exl-id: 3f904022-b770-4f35-a3b0-790e15748763
source-git-commit: beb224fdccf68c98fc3eff62b0867f22fa52902b
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 5%

---

# Note sulla versione{#release-notes}

Note sulla versione del 15 novembre 2018.

## Nuove funzionalità {#section_syx_mdt_wcb}

Nella versione di produzione di questa versione sono state rilasciate le seguenti nuove funzioni:

* **Aggiornamenti alla ricerca e al flusso di Instagram.** Puoi utilizzare un  *account aziendale Instagram* per:

   * Esegui una ricerca social Instagram per utente (l&#39;utente deve essere anche un account aziendale Instagram).

   * Crea flussi Instagram da un account utente Instagram specifico (l&#39;account deve anche essere un account aziendale), incluso il tuo.

   * Richiedi diritti per le risorse da Instagram utilizzando un flusso di lavoro parzialmente automatizzato.

   * Per informazioni sul tipo di account Instagram da impostare e richiedere diritti da Instagram, consulta [Informazioni sugli account Instagram](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md).

* **Monitoraggio automatico delle risposte alle richieste di diritti di utilizzo per ricerche basate su account aziendali.** Solo per ricerche basate su account aziendali: è disponibile la possibilità di monitorare automaticamente le risposte alle richieste di diritti e aggiornare la cronologia delle attività in Livefyre.

Per ulteriori informazioni su come richiedere i diritti per gli account Instagram, consulta [Inviare manualmente una richiesta di diritti Instagram](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md) e [Inviare una richiesta di diritti Instagram parzialmente automatizzata](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md).

* **Integrazione di Adobe Target.** È stata aggiunta l’integrazione con Adobe Target che consente di condividere le app Livefyre direttamente nella libreria delle offerte Adobe Target. Per ulteriori informazioni sull&#39;utilizzo di Livefyre con Adobe Target, consulta la [documentazione di Target](https://experienceleague.adobe.com/docs/livefyre/using/library/livefyre-target.html).

## Problemi {#section_ehw_ndt_wcb}

I problemi nelle tabelle seguenti sono stati risolti in questa versione.

### Versione di produzione

| Tipo di problema | Componente | Note sulla versione |
|--- |--- |--- |
| Problema | AppService: Identità Livefyre | È stato risolto un problema a causa del quale facendo clic su [!UICONTROL Reset to Default] non veniva reimpostato il logo in Modalità di accesso in Studio > Impostazioni integrazione > Identità Livefyre sull’immagine predefinita. |
| Problema | Libreria | È stato risolto un problema che impediva la corretta visualizzazione di un video caricato nella libreria e visualizzato nei dettagli della risorsa. |
| Problema | Flussi | È stato risolto un problema che impediva la visualizzazione dei prodotti in una regola di flusso. |
| Problema | Flussi | È stato risolto un problema a causa del quale i tag prodotto non erano disponibili per una regola di flusso. |
| Miglioramento | Studio | È stato risolto un problema che impediva la visualizzazione dell’ID prodotto in Livefyre Studio. |
| Problema | Studio: ModQ | È stato risolto un problema a causa del quale il contenuto eliminato veniva comunque visualizzato in ModQ dopo essere stato eliminato. |

### Versione UAT

| **Tipo di problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Problema | Componente social: Carosello | È stato risolto un problema a causa del quale il collegamento Condividi non rispondeva e copiava l’URL come previsto in IE11 e Mozilla Firefox. |
