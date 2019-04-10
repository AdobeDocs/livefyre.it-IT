---
description: Implementare Note a margine tramite implementazione .js.
seo-description: Implementare Note a margine tramite implementazione .js.
seo-title: Implementazione Sidenotes
solution: Experience Manager
title: Implementazione Sidenotes
uuid: aa 13852 e-e 2 b 0-4 a 86-97 cd-d 08 ab 5 e 2 cfab
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Implementazione Sidenotes{#sidenotes-implementation}

## Implementare Note a margine tramite implementazione .js

Per implementare questa funzione, passare una mappatura di oggetti 1-1 delle stringhe che desiderate ignorare all'oggetto di configurazione Javascript. Se non fornite un campo, verrà utilizzato il testo predefinito.

### Esempio

```
var customStrings = { postAsButton: "New Post As Text", postEditButton: "New Post Edit Text"};networkConfig["strings"] = customStrings; fyre.conv.load( networkConfig, [convConfig], function(){});
```
