---
description: La libreria Livefyre di base utilizzata per alimentare Livefyre sul sito.
seo-description: La libreria Livefyre di base utilizzata per alimentare Livefyre sul sito.
seo-title: updateAnchors, metodo
solution: Experience Manager
title: Livefyre.js
uuid: null
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# updateAnchors, metodo {#updateAnchorsMethod}

Utilizzate il metodo updateAnchors per aggiungere dinamicamente alla pagina contenuto ancorato.

Questo metodo è utile per l’impaginazione, o in altri casi in cui il contenuto laterale viene aggiunto dinamicamente alla pagina. Questo metodo definisce nuovi ancoraggi per gli elementi associati e utilizza un singolo argomento: newSelectors.

**newSelectors**. I selettori da aggiungere alle note. Può trattarsi di una stringa selettore, di un oggetto jQuery o di un array di elementi (uno qualsiasi dei tipi accettati dall'argomento selettori passati durante la creazione dell'app).
Formato:

```
app.updateAnchors(newSelectors);
```

Esempio:

```
var app = new Livefyre.Sidenotes(convConfig);// Load more contentapp.updateAnchors('#content');
```
