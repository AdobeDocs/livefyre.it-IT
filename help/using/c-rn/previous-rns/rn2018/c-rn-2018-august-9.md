---
description: Note sulla versione per la versione del 9 agosto 2018.
title: 9 agosto 2018
exl-id: 7b2fb562-33bf-4c34-ab83-5fc34f5d1f4f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 7%

---

# 9 agosto 2018{#august}

Note sulla versione per la versione del 9 agosto 2018.

## Nuove funzionalità {#section_syx_mdt_wcb}

**Tag video avanzati:** gli utenti possono ora vedere i tag avanzati per i video con meno di 50 MB.

## Problemi {#section_ehw_ndt_wcb}

I problemi nelle tabelle seguenti sono stati risolti in questa versione.

## Versione di produzione

| **Tipo di problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Bug | Contenuto app | È stato risolto un problema che impediva ad amministratori e gestori di contenuti di modificare il contenuto in Contenuto app. |
| Miglioramento | App | I social network hanno apportato modifiche alla privacy che significano che le menzioni social non saranno più supportate per Facebook o Twitter. |
| Miglioramento | App | I social network hanno apportato delle modifiche alla privacy. La funzione &quot;Post to&quot; che pubblica automaticamente i contenuti sui social network (Facebook, LinkedIn, Twitter) è stata rimossa. |
| Miglioramento | GDPR | È stato rimosso l’interruttore per la modalità dettagli dalla pagina dei dettagli della richiesta in Impostazioni > Privacy. È ancora possibile accedere alla modalità Dettagli aggiungendo /dbg alla fine dell’URL. |
| Bug | Integrazione: AEM | È stato risolto un problema a causa del quale il trascinamento e il rilascio delle app Livefyre in AEM appariva per creare più app. |
| Bug | Libreria | È stato risolto un problema a causa del quale una risorsa non veniva salvata correttamente nella libreria. |
| Bug | Identità Livefyre | È stato risolto un problema relativo all’identità LF che causava errori 403 durante l’accesso. |
| Bug | Ricerca social | È stato risolto un problema che impediva agli utenti di cercare post pubblici di Facebook utilizzando l&#39;opzione URL nella ricerca social. |
| Miglioramento | Sincronizzazione social | I social network hanno apportato modifiche alla privacy che significano che Social Sync non sarà più supportato per Facebook. |
| Miglioramento | Flussi | Ora, quando elimini un’app, elimina tutti i flussi associati a essa. |
| Miglioramento | Studio | I clienti ora possono emettere eventi Livefyre singolarmente per Adobe Analytics anziché in batch. |
| Miglioramento | Studio | Le finestre modali visualizzate nelle app di conversazione per i social network ora saranno finestre modali dal social network invece di Adobe Experience Manager Livefyre o altre finestre modali con marchio. |

## Versione UAT

I problemi nelle tabelle seguenti sono stati risolti nella versione UAT.

| **Tipo di problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Bug | RGPD | È stato risolto un problema che impediva la visualizzazione dei messaggi di rinuncia per alcuni video di Instagram. |
| Bug | Libreria | È stato risolto un problema che causava la visualizzazione manuale dello stato errato della richiesta di diritti da parte di una scheda con diritti concessi. |
| Bug | Libreria | È stato risolto un problema che impediva il salvataggio di una risorsa in una cartella. |
| Bug | Libreria/Ricerca | È stata ripristinata la possibilità di cercare URL da Instagram nella ricerca per social network. |
| Bug | ModQ | È stato risolto un problema a causa del quale il menu Ulteriori informazioni in ModQ non veniva visualizzato dove previsto. |
| Bug | Rights Management | È stato risolto un problema a causa del quale l’ordinamento in ModQ doveva trovarsi in una posizione fissa durante lo scorrimento della pagina. |
| Bug | Flussi | È stato risolto un problema relativo alla visualizzazione dei flussi nell’ambiente di staging. |
| Miglioramento | Flussi | È stata aggiunta l’opzione Sicuro per lavoro (SFW) e non sicuro per lavoro (NSFW) ai flussi. |
| Miglioramento | Studio | Funzionalità smart tag aggiunta al contenuto caricato nella libreria Livefyre Studio tramite FileStack (funzionalità di caricamento in Tutte le risorse). |
