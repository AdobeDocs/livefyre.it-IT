---
description: Implementare Note a margine tramite implementazione .js.
seo-description: Implementare Note a margine tramite implementazione .js.
seo-title: Implementazione delle note
solution: Experience Manager
title: Implementazione delle note
uuid: aa13852e-e2b0-4a86-97cd-d08ab5e2cfab
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Implementazione delle note{#sidenotes-implementation}

## Implementare Note a margine tramite implementazione .js

Per implementare questa funzione, trasmettere una mappatura oggetto 1-1 delle stringhe che si desidera ignorare all'oggetto di configurazione Javascript. Se non si fornisce un campo, verrà utilizzato il testo predefinito.

### Esempio 

```
var customStrings = { postAsButton: "New Post As Text", postEditButton: "New Post Edit Text"};networkConfig["strings"] = customStrings; fyre.conv.load( networkConfig, [convConfig], function(){});
```
