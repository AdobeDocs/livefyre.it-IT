---
description: La libreria principale Livefyre utilizzata per alimentare Livefyre sul tuo sito.
title: Livefyre.js
uuid: null
exl-id: 5f60ce54-5669-4768-912d-c1b13946d8b8
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 2%

---

# updateAnchors, metodo {#updateAnchorsMethod}

Utilizzare il metodo updateAnchors per aggiungere dinamicamente alla pagina il contenuto basato su barre.

Questo metodo è utile per l’impaginazione o in altri casi in cui il contenuto scorrevole viene aggiunto alla pagina in modo dinamico. Questo metodo definisce nuovi ancoraggi per gli elementi corrispondenti e utilizza un singolo argomento: newSelectors.

**newSelectors**. I selettori da aggiungere alle note. Può trattarsi di una stringa di selettore, di un oggetto jQuery o di una matrice di elementi (uno qualsiasi dei tipi accettati dall’argomento selettori passato durante la costruzione dell’app).
Formato:

```
app.updateAnchors(newSelectors);
```

Esempio:

```
var app = new Livefyre.Sidenotes(convConfig);// Load more contentapp.updateAnchors('#content');
```
