---
description: Utilizza l’API Bootstrap e Stream con le app Livefyre.
title: Visualizzazione dei dettagli account
exl-id: b8458954-3727-4c4d-93dd-d21a4328e069
source-git-commit: 3091db9d7b9611e26ad65c1432856c9465694e92
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# Utilizzare l’API Bootstrap e Stream con le app Livefyre {#bootstrap-stream-api}

## API Bootstrap {#bootstrap-api}

### Come posso recuperare contenuti più vecchi delle ultime 50 parti? {#howcontentolder}

Bootstrap è tutto il contenuto di un’app Livefyre. Si tratta dei dati memorizzati nella cache, generalmente vecchi di 12-20 minuti. Viene distribuito in blocchi di 50 pezzi ed è impaginato in modo da poter recuperare contenuti più vecchi di 50 pezzi.

[Riferimento API](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:bootstrap:operations:bs3:v3.1:network:site:article:init:method=get)

[Esempio di richiesta](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

La richiesta di esempio di cui sopra carica la pagina `init` che contiene Impostazioni raccolta e l’unico set iniziale di circa 50 parti di contenuto più recente. Per eseguire il polling del contenuto precedente, è necessario caricare le pagine di bootstrap successive con `N` come numero di pagina:

Richiesta: `https://{networkName}.bootstrap.fyre.co/bs3/v3.1/{network}/{siteId}/{b64articleId}/N.json`

Ad esempio, un’app di esempio ha 120 contenuti. Il contenuto &quot;1&quot; è il contenuto più vecchio e il contenuto &quot;70&quot; è il contenuto più recente.

* `Init` carica circa 120-70 parti di contenuto in ordine decrescente:  [https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

* `O.json` caricherà ~ 1-50 parti di contenuto in ordine crescente:  `https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json`
* `1.json` caricherà ~ 51-100 parti di contenuto in ordine crescente:  `https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json`
* `2.json` carica circa 101-120 parti di contenuto in ordine crescente:`https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json`

[Fare clic qui per visualizzare il diagramma di flusso del sondaggio Bootstrap.](https://marketing-resource-help.s3.amazonaws.com/resources/help/en_US/livefyre/bootstrap-poll-flowchart.pdf)

## API Streaming {#stream-api}

Cos’è l’API Stream?
Stream è un lungo sondaggio che, per progettazione, è destinato a rimanere aperto per circa 30 secondi. Descrizione sulla tecnica del polling lungo si trova qui: [https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet](https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet)

Questo endpoint con sondaggi a lungo termine invia in un’app Livefyre nuovi contenuti (ad esempio, un utente pubblica un commento), modifiche allo stato del contenuto (ad esempio, l’utente elimina il commento, mi piace) e modifiche alla moderazione del contenuto (ad esempio il moderatore approva un contenuto).

La richiesta all’API Stream deve essere di circa 30 secondi (polling lungo) con timeout previsto dopo 30 secondi in assenza di nuovi flussi di contenuto.

Riferimento API: [https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operazioni:v3.1:collection:aggiornamenti:method=get](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get)

Esempio di richiesta:

`{"timeout":true,"parked":true,"h":"ct245.dsr.livefyre.com"}`

Nota: La `maxEventId` in una risposta API Stream è l’ID evento più alto degli aggiornamenti in questa risposta. Utilizza questo valore come parametro di percorso `lastEventId` quando crei l’URL della tua successiva richiesta API Stream per ottenere gli aggiornamenti che si verificano dopo tutti gli aggiornamenti in questa risposta.

L’esempio seguente è basato su un’app Commenti :

Commento &quot;Primo commento&quot; è stato pubblicato per primo. &quot;Second Comment&quot; è stato pubblicato dopo.

Risposta API del flusso di commenti:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

Il `maxEventId` nella risposta è &quot;1520289700953369&quot; che verrà utilizzato come `lastEventId` per eseguire il polling dell’endpoint per ottenere gli aggiornamenti (ad esempio, secondo commento) che si verificano dopo tutti gli aggiornamenti in questa risposta.

Risposta API del secondo flusso di commenti:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

La risposta `maxEventID` &quot;1520289700953369&quot; deve a sua volta essere utilizzata come `lastEventID` per generare la risposta API Stream per il prossimo aggiornamento.
