---
description: Rendi il contenuto della community disponibile per i crawler dei motori di ricerca.
title: Bootstrap HTML
exl-id: 22ab4f2d-f433-4805-b0dd-16d4531e425d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 1%

---

# Bootstrap HTML

Rendi il contenuto della community disponibile per i crawler dei motori di ricerca.

Per un elenco completo degli endpoint disponibili, consulta la sezione Livefyre [Riferimento API](https://api.livefyre.com/docs) .

Le app Livefyre richiedono l’esecuzione di JavaScript sulla pagina per visualizzare il contenuto per le raccolte. Poiché la maggior parte dei crawler dei motori di ricerca non possono eseguire JavaScript, non sono in grado di visualizzare il contenuto pubblicato dalla community. Utilizza l’API HTML Bootstrap per aggiungere frammenti ricercabili di questo contenuto alla risposta HTTP iniziale della pagina, consentendo al contenuto e alle parole chiave di migliorare l’ottimizzazione del motore di ricerca.

>[!NOTE]
>
>Questa API è disponibile solo per i tipi di Raccolta commenti e Live Blog.

## Integrazione

L’API HTML Bootstrap di Livefyre restituirà un frammento HTML del contenuto utente, che potrebbe essere incluso nella risposta HTTP della pagina. Questa risposta sarà leggibile dai crawler dei motori di ricerca senza eseguire alcun JavaScript. Una volta che la pagina è attiva nel browser di un utente, il frammento HTML viene sostituito con il widget interattivo completo e l’utente può pubblicare contenuti.

Per implementare l’API HTML Bootstrap:

1. Effettua una richiesta server-to-server API all’endpoint HTML Bootstrap descritto di seguito.

   >[!NOTE]
   >
   >Se cerchi di recuperare la Bootstrap HTML per una conversazione che non esiste ancora (ovvero, se devi ancora incorporare l’app o creare la raccolta), riceverai un 200, ma con contenuti che hanno un aspetto simile al seguente: `<!- HTTP 404 example.fyre.co/000000/MTEwMTo2NDEyOD1RS/bootstrap.html ->`

1. Se nella restituzione non è incluso contenuto con un &quot;404&quot;, salvarlo in una stringa. Puoi memorizzare in cache questa risposta per un utilizzo successivo per evitare di richiedere l’API HTML Bootstrap su ogni caricamento di pagina.
1. Inserisci la stringa HTML Bootstrap nella pagina web in cui desideri visualizzare il contenuto.
1. Distribuisci la pagina web al browser (o al crawler del motore di ricerca).

## Risorsa

```
GET https://{networkName}.bootstrap.fyre.co/bs3/{networkName}.fyre.co/{siteId}/{base64 encoded article ID}/bootstrap.html 
```

## Parametri

* **** networkNameYour Livefyre ha fornito il nome di rete. Ad esempio: *laboratori* in `labs.fyre.co`.
* **** siteIdL&#39;ID sito della raccolta.
* **b64** articleIdL&#39;ID articolo della raccolta utilizzando la codifica base64url.

## Esempio 

```
https://labs.bootstrap.fyre.co/bs3/labs.fyre.com/4/NTg0/bootstrap.html 
```

## Risposta

```
https://gist.github.com/ec5c2457322faf9cf515 
```
