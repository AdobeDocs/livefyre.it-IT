---
description: Rendi il contenuto della community disponibile per i crawler dei motori di ricerca.
seo-description: Rendi il contenuto della community disponibile per i crawler dei motori di ricerca.
seo-title: Bootstrap HTML
solution: Experience Manager
title: Bootstrap HTML
uuid: 137e4382-4e7b-4124-9d35-1d872a497bc7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Bootstrap HTML

Rendi il contenuto della community disponibile per i crawler dei motori di ricerca.

Per un elenco completo degli endpoint disponibili, consultate la sezione Riferimento [](https://api.livefyre.com/docs) API Livefyre.

Le app Livefyre richiedono l'esecuzione di JavaScript sulla pagina per visualizzare il contenuto per le raccolte. Poiché la maggior parte dei crawler dei motori di ricerca non è in grado di eseguire JavaScript, non sono in grado di visualizzare il contenuto pubblicato dalla community. Utilizzate l'API HTML di avvio per aggiungere frammenti di questo contenuto ricercabili alla risposta HTTP iniziale della pagina, consentendo al contenuto e alle parole chiave di migliorare l'ottimizzazione del motore di ricerca.

>[!NOTE]
>
>Questa API è disponibile solo per i tipi di commenti e raccolte di blog dal vivo.

## Integrazione

L'API HTML Bootstrap di Livefyre restituirà un frammento HTML del contenuto utente, che potrebbe essere incluso nella risposta HTTP della pagina. Questa risposta sarà leggibile dai crawler dei motori di ricerca senza eseguire JavaScript. Una volta che la pagina è live nel browser di un utente, il frammento HTML viene sostituito con il widget interattivo completo e l'utente potrà pubblicare contenuti.

Per implementare l’API HTML di Bootstrap:

1. Eseguite una richiesta dell'API server all'endpoint HTML di Bootstrap, come descritto di seguito.

   >[!NOTE]
   >
   >Se state tentando di acquisire l'HTML di Bootstrap per una conversazione che non esiste ancora (ovvero, se non avete ancora incorporato l'app o creato la raccolta), riceverete un 200, ma con un contenuto simile a: `<!- HTTP 404 example.fyre.co/000000/MTEwMTo2NDEyOD1RS/bootstrap.html ->`

1. Se la restituzione non include il contenuto con un codice "404", salvatelo in una stringa. Potete memorizzare la risposta nella cache per un utilizzo successivo per evitare di richiedere l'API HTML di Bootstrap su ogni caricamento di pagina.
1. Inserite la stringa HTML Bootstrap nella pagina Web in cui desiderate visualizzare il contenuto.
1. Trasmettere la pagina Web al browser (o al crawler del motore di ricerca).

## Risorsa

```
GET https://{networkName}.bootstrap.fyre.co/bs3/{networkName}.fyre.co/{siteId}/{base64 encoded article ID}/bootstrap.html 
```

## Parametri

* **networkName** Il nome di rete fornito da Livefyre. Ad esempio: *laboratori* in `labs.fyre.co`.
* **siteId** L'ID del sito della raccolta.
* **b64articleId** L'ID articolo della raccolta utilizzando la codifica base64url.

## Esempio 

```
https://labs.bootstrap.fyre.co/bs3/labs.fyre.com/4/NTg0/bootstrap.html 
```

## Risposta

```
https://gist.github.com/ec5c2457322faf9cf515 
```
