---
description: Scoprite come monitorare e memorizzare i contenuti generati dall'utente attraverso il sistema Livefyre.
seo-description: Scoprite come monitorare e memorizzare i contenuti generati dall'utente attraverso il sistema Livefyre.
seo-title: Flusso attività
solution: Experience Manager
title: Flusso attività
uuid: f 40 deec 1-58 ab -41 c 9-aac 4-d 2 d 8 c 9192 bb 9
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Flusso attività {#activity-stream}

Scoprite come monitorare e memorizzare i contenuti generati dall&#39;utente attraverso il sistema Livefyre.

Utilizzate l&#39;API Activity Flow per utilizzare i dati generati dall&#39;utente attraverso il sistema Livefyre sulla rete o sul sito. Ad esempio: utilizzare dati di questa API per aggiornare gli indici di ricerca in base alle valutazioni, oppure per gestire i badge degli utenti in un sistema di terze parti in base alla loro attività.

API Activity Stream:

Per un elenco completo degli endpoint disponibili, consultate la sezione Riferimento API di Livefyre.

## Risorse {#section_aql_n4l_b1b}

Esistono due endpoint, uno per l&#39;ambiente di staging e uno per la produzione.

### Staging

```
GET https://bootstrap.t402.livefyre.com/api/v3.1/activity/ 
```

### Produzione

```
GET https://bootstrap.livefyre.com/api/v3.1/activity/ 
```

### Parametri

* **risorse:***stringa* Un URN dell&#39;oggetto per il quale si richiede dati dell&#39;attività.

* **poiché:***integer* Un numero intero a 64 bit che rappresenta l&#39;ID dell&#39;ultimo evento ricevuto. Specificatè0 &#39;se non avete dati precedenti.

## Stringhe URN {#section_skl_q4l_b1b}

Esempi:

* **urn: livefyre:**`example.fyre.co` Il flusso attività per `example.fyre.co`.
* **urn: livefyre:**`example.fyre.co:site=54321` Flusso attività per il sito 54321 nella `example.fyre.co` rete.

## Criteri token {#section_nwh_c5j_11b}

L&#39;API Activity Stream utilizza un token Besting oauth per l&#39;autenticazione. I Token del bearer fanno parte della specifica oauth 2.0 e sono descritti ufficialmente [qui](https://tools.ietf.org/html/rfc6750#section-1.2).

Un token contiene diversi elementi:

* Chi ha creato il token.
* A chi è stato assegnato un token.
* Un tempo in cui non è più valido.
* La cosa su cui stiamo lavorando.
* Elenco delle autorizzazioni concesse.

### Passaggi

I passaggi per creare un token per il visualizzatore oauth includono:

* Crea un mappatura/dizionario contenente emittenti, pubblico, oggetto, scadenza e ambito.
* Per codificare un token JWT, utilizzate la libreria JWT.
* Aggiungi autenticazione: Bearer» alla richiesta HTTP.

Il codice seguente illustra i passaggi descritti di seguito in Python:

```
import time 
import jwt 
  
# network data goes here: 
network = "timeout-0.fyre.co" 
network_secret = "...replaceme..." 
  
# api URN 
api_urn = "urn:livefyre:api:core=GetActivityStream" 
  
# expires in 10 seconds 
expiration = int(time.time() + 10) 
  
network_urn = "urn:livefyre:" + network 
  
data = dict(iss=network_urn, aud=network_urn, sub=network_urn, scope=api_urn, exp=expiration) 
  
token = jwt.encode(data, key=network_secret)
```

Se i tasti token del visualizzatore sono definiti come segue:

* **iss** *(emittente)* Un&#39;entità con l&#39;autorità di generare token. Potrebbe trattarsi di Livefyre, di un sito o di una rete. (Per una nota di fine scuola, è l&#39;elemento padre).
* **aud** *(Audience)* La persona per la quale è stato generato questo token. Se create il token stesso, è il sito o la rete.
* **sub** *(Oggetto)* L&#39;oggetto per il quale concedere le autorizzazioni. Ad esempio, se state lavorando su una raccolta, l&#39;oggetto deve essere l&#39;identificatore della raccolta. (Nella nota dell&#39;esempio scolastico, sei tu.)
* **exp** *(Scadenza)* Un punto nel tempo in cui il token non è più valido.
* **scope** *(Scope)* Questo è un elenco delle autorizzazioni concesse per l&#39;oggetto. «Late for school» è un esempio. Il nome di un&#39;API è un altro esempio.

## Esempio {#section_dhl_ytj_11b}

```
curl -H "Authorization: Bearer <BEARER TOKEN>" https://bootstrap.livefyre.com/api/v3.1/activity/?resource=&since=
```

## Risposta {#section_gs2_stj_11b}

```
{ 
"code": 200,  
"data": { 
  "annotations": {},  
  "authors": {  
      /** "a set of every author who generated activity within this window" */ 
      "_up1770425@livefyre.com": { 
        "avatar": "https://gravatar.com/avatar/68c789597150d3e941769a5c0a0c4249/?s=50&d=https://avatars-qa.fyre.co/a/anon/50.jpg",  
        "displayName": "ross_pfahler",   
        "id": "_up1770425@livefyre.com",  
        "profileUrl": "https://www.qa-ext.livefyre.com/profile/1770425/",  
        "tags": [],  
        "type": 1 
      },  
  ... 
  },  
  "collections": {  
      /** "a set of every collection for which an activity was generated" */ 
      "2486601": { 
        "articleIdentifier": "75",  
        "id": "2486601",  
        "site": "290596",  
        "title": "Live Blog",  
        "url": "https://orangesaregreat.com/..." 
      }, 
  ... 
  },  
  /** "the maximum event ID for this window" */ 
  "maxEventId": 1383508243715211, 
  "states": {  
      /** "a set of messages (comments, reviews, etc) for which activity  
           was generated in this window, represents the compiled 
           'state' of the object including visible actions on that object 
           (up-votes, likes, and etc.)" */ 
      "3ad6480eb00c4895b29b7a972380f489@livefyre.com": { 
          "collectionId": "2486685",  
          "content": { 
              "annotations": { 
                "rating": [ 90 ], /** "this object is a Rating (4.5)" */ 
                "vote": [ 
                    { 
                      "author": "_up1792695@livefyre.com",  
                      "collectionId": "2486685",  
                      "value": 1 
                    } 
                ] 
              },  
              "attachments": [  
              /** "a list of oembeds; the body of this Rating included  
                  this Youtube video" */ 
                { 
                  "author_name": "mauricio890",  
                  "author_url": "https://www.youtube.com/user/mauricio890",  
                  "height": 480,  
                  "html": "<iframe width=\"854\" height=\"480\" src=\"https://www.youtube.com/embed/pmMAw5a7POU?autoplay=1&feature=oembed\" frameborder=\"0\" allowfullscreen></iframe>",  
                  "link": "https://www.youtube.com/watch?v=pmMAw5a7POU",  
                  "provider_name": "YouTube",  
                  "provider_url": "https://www.youtube.com/",  
                  "thumbnail_height": 360,  
                  "thumbnail_url": "https://i1.ytimg.com/vi/pmMAw5a7POU/hqdefault.jpg",  
                  "thumbnail_width": 480,  
                  "title": "Napoleon Dynamite dance scene",  
                  "type": "video",  
                  "url": "https://www.youtube.com/watch?v=pmMAw5a7POU",  
                  "version": "1.0",  
                  "width": 854 
                } 
              ],  
              // "who authored the content" 
              "authorId": "_up1793160@livefyre.com",  
              "bodyHtml": "<p><strong>Pros:</strong>Boom</p><p><strong>Cons:</strong>Goes</p><p><strong>Description:</strong>The dynamite:</p><p><a href=\"https://www.youtube.com/watch?v=pmMAw5a7POU\" target=\"_blank\" rel=\"nofollow\">https://www.youtube.com/watch?v=pmMAw5a7POU</a><br/></p>",  
              // "UNIX timestamp" 
              "createdAt": 1383257354,  
              "id": "3ad6480eb00c4895b29b7a972380f489@livefyre.com",  
              // "non-empty only if this were a reply" 
              "parentId": "", 
              // "UNIX timestamp"  
              "updatedAt": 1383257356  
          },  
          // "the event ID of this state." 
          "event": 1383369320554187,  
          "lastVis": 3,  
          "source": 0,  
          "type": 0,  
          // "Object visibility: 0 = deleted, 1 = everyone, 2 = bozo,  
          // 3 = owner + admins (e.g. premod)" 
          "vis": 1  
      },  
      "5943789": { 
          "collectionId": "2486688",  
          "content": { 
            "annotations": { 
                // "posted by a moderator" 
                "moderator": true  
            },  
            "authorId": "_up1792872@livefyre.com",  
            "bodyHtml": "<p>This is a regular comment from a moderator</p>",  
            "createdAt": 1383372338,  
            "id": "5943789",  
            "parentId": "",  
            "updatedAt": 1383372338 
          },  
          "event": 1383372338732492,  
          "lastVis": 0,  
          "source": 5,  
          "type": 0,  
          "vis": 1 
      },  
      "863c616a2c0c44239feed0914c282d7c@livefyre.com": { 
          "collectionId": "2486685",  
          "content": { 
              "id": "863c616a2c0c44239feed0914c282d7c@livefyre.com" 
          },  
          "event": 1383371303805767,  
          "lastVis": 1,  
          "source": 0,  
          "type": 0,  
          "vis": 0 // "0 = deleted; this object was removed" 
      },  
  ... 
},  
"meta": { 
  // "this describes position in the stream" 
  "cursor": {  
    // "maximum number of objects returned in a single call through this API" 
    "limit": 50,  
    // "the final position in the stream, and from where data should be requested" 
    "next": 1383508243715211, 
    // "the initial position (the 'since' parameter value in this request)" 
    "self": 0  
  } 
},  
"status": "ok" 
} 
```

Una risposta con i nuovi dati dall&#39;ultima richiesta:

```
{ 
    "code": 200,  
    "data": { 
        "annotations": {},  
        "authors": {},  
        "collections": {},  
        "maxEventId": -1,  
        "states": {} 
    },  
    "meta": { 
        "cursor": { 
            "limit": 50, 
            /** "indicates there is no data beyond 1383508243715211" */  
            "next": null, 
            "self": 1383508243715211 
        } 
    },  
    "status": "ok" 
}
```

## Note {#section_hj3_crj_11b}

* Una chiamata corretta all&#39;API darà un codice di stato HTTP 200. Tutti gli altri codici di stato devono essere considerati errori.
* Se non-null, utilizzate il valore da `data.meta.cursor.next` come `since` parametro della richiesta successiva.
* Se il valore è `data.meta.cursor.next` nullo, significa che non sono presenti nuovi dati da utilizzare. Per verificare se sono arrivati nuovi dati, è necessario `since` richiedere nuovamente la richiesta in seguito.
* In pratica, è necessario richiedere immediatamente più dati se il `data.meta.cursor.next` valore è diverso da null.
* Tramite questa API in produzione sono disponibili circa due ore di dati recenti.
* Impostate i processi per eseguire il polling di questo endpoint frequentemente su cronoperismo, per evitare dati mancanti. Un intervallo di cinque minuti dovrebbe essere perfettamente adeguato per la maggior parte delle implementazioni.
