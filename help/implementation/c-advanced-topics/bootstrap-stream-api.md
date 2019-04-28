---
description: Utilizzate l'API Bootstrap e Stream con Livefyre Apps.
seo-description: Utilizzate l'API Bootstrap e Stream con Livefyre Apps.
seo-title: Utilizzare l'API Bootstrap e Stream con Livefyre Apps
solution: Experience Manager
title: Visualizzazione dei dettagli account
uuid: bace 558 f-ade 8-49 d 6-abda -9 ee 754 ce 4 ac 0
translation-type: tm+mt
source-git-commit: d615705ccf5e4511cc735ce91d95c3e15d0c0160

---


# Utilizzare l&#39;API Bootstrap e Stream con Livefyre Apps {#bootstrap-stream-api}

## API di Bootstrap {#bootstrap-api}

### Come posso recuperare il contenuto precedente ai 50 pezzi più recenti? {#howcontentolder}

Bootstrap è tutto il contenuto di un&#39;app Livefyre. Sono i dati memorizzati nella cache, generalmente di 12-20 minuti. Viene distribuito in blocchi di 50 pezzi ed è impaginato in modo da poter recuperare contenuti precedenti a 50 pezzi.

[Riferimento API](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:bootstrap:operations:bs3:v3.1:network:site:article:init:method=get)

[Richiesta di esempio](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

La richiesta di esempio sopra carica la `init` pagina che contiene Impostazioni raccolta e l&#39;unico set iniziale di ~ 50 parti del contenuto più recente. Per eseguire il polling del contenuto precedente, dovete caricare le pagine di avvio successive con `N` il numero di pagina:

Richiesta: `https://{networkName}.bootstrap.fyre.co/bs3/v3.1/{network}/{siteId}/{b64articleId}/N.json`

Ad esempio, un&#39;app di esempio ha 120 parti di contenuto. Il contenuto &quot;1&quot; è la parte più vecchia del contenuto e il contenuto &quot;70&quot; è la parte più recente del contenuto.

* `Init` caricheranno ~ 120-70 pezzi di contenuto in ordine decrescente: [https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

* `O.json` caricheranno ~ 1-50 pezzi di contenuto in ordine crescente: [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json)

* `1.json` caricheranno ~ 51-100 pezzi di contenuto in ordine crescente: [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json)

* `2.json` caricheranno ~ 101-120 pezzi di contenuto in ordine crescente:[https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json)

[Fate clic qui per visualizzare il diagramma di flusso Sondaggio di Bootstrap.](https://marketing-resource-help.s3.amazonaws.com/resources/help/en_US/livefyre/bootstrap-poll-flowchart.pdf)

## API Flusso {#stream-api}

Cos&#39;è il flusso API?
Il flusso è un sondaggio lungo che per la progettazione viene mantenuto per circa 30 secondi. La descrizione sulla tecnica di polling estesa è disponibile qui: [https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet](https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet)

Questo endpoint di polling lungo trasmette nuovi contenuti (ad es. un utente post un commento), lo stato del contenuto cambia (ad es. l&#39;utente elimina i commenti, le mi piace) e le modifiche di moderazione al contenuto (ad es. moderatore approva una parte del contenuto) a un&#39;app Livefyre.

La richiesta all&#39;API di flusso deve essere ~ 30 secondi (long polling) con timeout previsto dopo 30 secondi quando non sono presenti nuovi flussi di contenuto.

Riferimento API: [https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get)

Esempio di richiesta:

`{"timeout":true,"parked":true,"h":"ct245.dsr.livefyre.com"}`

Nota: La `maxEventId` risposta all&#39;API di flusso è l&#39;ID evento più alto degli aggiornamenti in questa risposta. Utilizzate questo valore come `lastEventId` parametro path quando create l&#39;URL della successiva richiesta di streaming API per ottenere aggiornamenti dopo tutti gli aggiornamenti in questa risposta.

L&#39;esempio seguente si basa su un&#39;app Commenti:

Per primo è stato pubblicato il commento «Primo commento». &quot; Second Comment &quot;è stato pubblicato dopo.

Risposta API per il primo commento:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

La `maxEventId` risposta è &quot;1520289700953369&quot; che verrà utilizzata come `lastEventId` per il polling dell&#39;endpoint per ottenere gli aggiornamenti (ovvero Secondo commento) si verifica dopo tutti gli aggiornamenti di questa risposta.

Second Comment Stream API response:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

L&#39; `maxEventID` elemento «1520289700953369» nella risposta dovrebbe a sua volta essere usato come creare `lastEventID` la risposta API Flusso per l&#39;aggiornamento successivo.