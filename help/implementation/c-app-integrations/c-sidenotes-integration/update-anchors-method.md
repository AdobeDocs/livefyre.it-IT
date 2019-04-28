---
description: La libreria di base Livefyre utilizzata per abilitare Livefyre sul sito.
seo-description: La libreria di base Livefyre utilizzata per abilitare Livefyre sul sito.
seo-title: Metodo updateanchors
solution: Experience Manager
title: Livefyre. js
uuid: null
translation-type: tm+mt
source-git-commit: 097321964ff078bac83c4674100f8c62a8f3a1af

---


# Metodo updateanchors {#updateAnchorsMethod}

Utilizzate il metodo updateanchors per aggiungere alla pagina contenuto sidenizzato in modo dinamico.

Questo metodo è utile per l&#39;impaginazione o in altri casi in cui il contenuto in uso sidenote viene aggiunto alla pagina in modo dinamico. Questo metodo definisce nuovi ancoraggi per gli elementi associati e segue un singolo argomento: Newselectors.

**Newselectors**. Selettori da aggiungere a Sidenotes. Può trattarsi di una stringa di selezione, un oggetto jquery o un array di elementi (qualsiasi dei tipi accettati dall&#39;argomento dei selettori passati durante la creazione delle app).
Formato:

```
app.updateAnchors(newSelectors);
```

Esempio:

```
var app = new Livefyre.Sidenotes(convConfig);// Load more contentapp.updateAnchors('#content');
```
