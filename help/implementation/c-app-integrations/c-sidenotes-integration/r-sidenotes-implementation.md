---
description: Implementare Note a margine tramite implementazione .js.
title: Implementazione di Sidenote
exl-id: 07a68677-c67e-4128-8cb7-c5fb9e0ecc60
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 22%

---

# Implementazione di Sidenote{#sidenotes-implementation}

## Implementare Note a margine tramite implementazione .js

Per implementare questa funzione, passa una mappatura oggetto 1-1 delle stringhe che desideri ignorare all&#39;oggetto di configurazione Javascript. Se non si fornisce un campo, verrà utilizzato il testo predefinito.

### Esempio 

```
var customStrings = { postAsButton: "New Post As Text", postEditButton: "New Post Edit Text"};networkConfig["strings"] = customStrings; fyre.conv.load( networkConfig, [convConfig], function(){});
```
