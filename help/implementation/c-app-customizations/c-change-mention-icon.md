---
description: Modifica l'icona visualizzata per gli utenti Livefyre nel menu a discesa
  @mention.
seo-description: Modifica l'icona visualizzata per gli utenti Livefyre nel menu a
  discesa @menzioni.
seo-title: Cambia icona @menzioni
solution: Experience Manager
title: Cambia icona @mention
uuid: a 395 f 4 ff-a 774-454 a -8 d 94-4 a 3371 d 8 cc 2 c
translation-type: tm+mt
source-git-commit: 0d2ff61b1db6100de1d59e6e20c1175f015a78c5

---


# `@mention` Icona Modifica {#change-mention-icon}

Modificate l'icona visualizzata per gli utenti Livefyre nel menu `@mention` a discesa.

Modificate l'icona Livefyre utilizzata nel menu `@mention` a discesa a un'icona di vostra scelta, consentendo di indicare i membri della community con la vostra icona.

## Esempio

Per modificare questa icona, aggiungete i seguenti CSS al foglio di stile. Sostituite <*your resource*> url con l'URL dell'immagine selezionata per sostituire il badge Livefyre predefinito.

```
.fyre-editor-container .fyre-editor-toolbar > .fyre-mention-menu .fyre-mention-item .fyre-mention-item-livefyre { 
    background: url(<your resource url>) no-repeat center; 
    background-position: 0px 0px; 
    background-size: 22px 22px; 
}
```
