---
description: Rendete disponibile il contenuto della community per le gamme laterali
  dei motori di ricerca.
seo-description: Rendete disponibile il contenuto della community per le gamme laterali
  dei motori di ricerca.
seo-title: HTML Bootstrap
solution: Experience Manager
title: HTML Bootstrap
uuid: 137 e 4382-4 e 7 b -4124-9 d 35-1 d 872 a 497 bc 7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# HTML Bootstrap

Rendete disponibile il contenuto della community per le gamme laterali dei motori di ricerca.

Per un elenco completo degli endpoint disponibili, consultate la sezione [Riferimento](https://api.livefyre.com/docs) API di Livefyre.

Livefyre Apps richiede di eseguire javascript sulla pagina per visualizzare il contenuto per le vostre raccolte. Poiché la maggior parte dei dispositivi esterni dei motori di ricerca non è in grado di eseguire javascript, non sono in grado di visualizzare il contenuto dei post della community. Utilizzate l'API HTML di Bootstrap per aggiungere frammenti ricercabili di questo contenuto alla risposta HTTP iniziale della pagina, consentendo ai contenuti e alle parole chiave di migliorare l'ottimizzazione del motore di ricerca.

>[!NOTE]
>
>Questa API è disponibile solo per i tipi di commenti e di raccolta blog live.

## Integrazione

L'API HTML di Livefyre restituirà un frammento HTML del contenuto dell'utente, che può essere incluso nella risposta HTTP della pagina. Questa risposta sarà leggibile dai tasti di ricerca dei motori di ricerca senza eseguire javascript. Quando la pagina è live nel browser di un utente, il frammento HTML verrà sostituito con il widget interattivo completo e l'utente sarà in grado di pubblicare il contenuto.

Per implementare l'API HTML di Bootstrap:

1. Eseguite un server sulla richiesta API server all'endpoint HTML Bootstrap documentato di seguito.

   >[!NOTE]
   >
   >Se state tentando di acquisire l'HTML di Bootstrap per una conversazione che non esiste ancora (ovvero se dovete ancora incorporare l'app o creare la raccolta), riceverete un 200, ma con un contenuto simile a: `<!- HTTP 404 example.fyre.co/000000/MTEwMTo2NDEyOD1RS/bootstrap.html ->`

1. Se la restituzione non include contenuto con un '404, salvatelo in una stringa. Potete memorizzare nella cache questa risposta per evitare di richiedere l'API HTML di Bootstrap su ogni pagina.
1. Inserite la stringa HTML di Bootstrap nella pagina Web in cui desiderate che venga visualizzato il contenuto.
1. Distribuite la pagina Web al browser (o al modulo crawler del motore di ricerca).

## Risorsa

```
GET https://{networkName}.bootstrap.fyre.co/bs3/{networkName}.fyre.co/{siteId}/{base64 encoded article ID}/bootstrap.html 
```

## Parametri

* **Networkname** Your Livefyre fornisce il nome della rete. Ad esempio: *in*`labs.fyre.co`.
* **Siteid** L'ID del sito della raccolta.
* **b 64 articleid** L'ID articolo della raccolta utilizzando la codifica URL base 64.

## Esempio

```
https://labs.bootstrap.fyre.co/bs3/labs.fyre.com/4/NTg0/bootstrap.html 
```

## Risposta

```
https://gist.github.com/ec5c2457322faf9cf515 
```
