---
description: Utilizzate l'API Bootstrap e Stream con le app Livefyre.
seo-description: Utilizzate l'API Bootstrap e Stream con le app Livefyre.
seo-title: Utilizzare l'API Bootstrap e Stream con le app Livefyre
solution: Experience Manager
title: Visualizzazione dei dettagli account
uuid: bace558f-ade8-49d6-abda-9ee754ce4ac0
translation-type: tm+mt
source-git-commit: d615705ccf5e4511cc735ce91d95c3e15d0c0160

---


# Utilizzare l'API Bootstrap e Stream con le app Livefyre {#bootstrap-stream-api}

## API di Bootstrap {#bootstrap-api}

### Come è possibile recuperare contenuti più vecchi dei più recenti 50 pezzi? {#howcontentolder}

Bootstrap è tutto il contenuto di un'app Livefyre. Sono i dati memorizzati nella cache, generalmente vecchi di 12-20 minuti. Viene distribuito in blocchi di 50 pezzi ed è impaginato in modo da poter recuperare contenuti più vecchi di 50 pezzi.

[Riferimento API](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:bootstrap:operations:bs3:v3.1:network:site:article:init:method=get)

[Esempio di richiesta](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

La richiesta di esempio sopra carica la `init` pagina che contiene le Impostazioni raccolta e l'unico set iniziale di circa 50 parti di contenuto più recente. Per eseguire il polling del contenuto precedente, è necessario caricare le pagine di avvio successive con `N` il numero di pagina:

Richiesta: `https://{networkName}.bootstrap.fyre.co/bs3/v3.1/{network}/{siteId}/{b64articleId}/N.json`

Ad esempio, un'app di esempio ha 120 contenuti. Il contenuto "1" è il contenuto più vecchio e il contenuto "70" è il contenuto più recente.

* `Init` caricherà circa 120-70 contenuti in ordine decrescente: [https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

* `O.json` verranno caricati ~ 1-50 contenuti in ordine crescente: [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json)

* `1.json` verranno caricati ~ 51-100 contenuti in ordine crescente: [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json)

* `2.json` caricherà circa 101-120 contenuti in ordine crescente:[https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json)

[Fate clic qui per visualizzare il diagramma di flusso del sondaggio di avvio.](https://marketing-resource-help.s3.amazonaws.com/resources/help/en_US/livefyre/bootstrap-poll-flowchart.pdf)

## API di flusso {#stream-api}

Cos'è l'API Stream?
Il flusso è un lungo sondaggio che, per progettazione, deve rimanere aperto per circa 30 secondi. Descrizione della tecnica di polling lungo è disponibile qui: [https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet](https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet)

Questo endpoint di polling lungo trasferisce in un’app Livefyre nuovi contenuti (ad es. un utente pubblica un commento), modifiche allo stato del contenuto (ad es. un utente elimina i propri commenti, mi piace) e modifiche alla moderazione del contenuto (ad es. un moderatore approva un contenuto).

La richiesta all'API Stream deve essere di ~30 secondi (polling lungo) con timeout previsto dopo 30 secondi quando non viene eseguito alcun nuovo flusso di contenuto.

Riferimento API: [https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get)

Esempio di richiesta:

`{"timeout":true,"parked":true,"h":"ct245.dsr.livefyre.com"}`

Nota: La risposta `maxEventId` in un'API Stream corrisponde all'ID evento più alto degli aggiornamenti in questa risposta. Usa questo valore come parametro del `lastEventId` percorso quando crei l'URL della tua richiesta API Stream successiva per ottenere gli aggiornamenti che si verificano dopo tutti gli aggiornamenti di questa risposta.

L'esempio seguente è basato su un'app Commenti:

Il commento "Primo commento" è stato pubblicato per primo. "Second Commment" è stato pubblicato dopo.

Prima risposta API flusso di commenti:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

La `maxEventId` risposta è "1520289700953369", che verrà utilizzata come `lastEventId` per il sondaggio dell’endpoint per ottenere aggiornamenti (ad esempio, secondo commento) dopo tutti gli aggiornamenti di questa risposta.

Seconda risposta API flusso di commenti:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

La risposta `maxEventID` "1520289700953369" dovrebbe a sua volta essere utilizzata come `lastEventID` base per creare la risposta API Stream per il prossimo aggiornamento.