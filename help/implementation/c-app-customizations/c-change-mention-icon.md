---
description: Modifica l'icona visualizzata per gli utenti Livefyre nel menu a discesa @mention.
seo-description: Modifica l'icona visualizzata per gli utenti Livefyre nel menu a discesa @menzioni.
seo-title: Cambia icona @menzioni
solution: Experience Manager
title: Cambia icona @mention
uuid: a395f4ff-a774-454a-8d94-4a3371d8cc2c
translation-type: tm+mt
source-git-commit: 0d2ff61b1db6100de1d59e6e20c1175f015a78c5

---


# Cambia `@mention` icona {#change-mention-icon}

Change the icon displayed for Livefyre users in the `@mention` pulldown menu.

Modificate l'icona Livefyre utilizzata nel menu a `@mention` discesa impostando un'icona di vostra scelta, per indicare ai membri della community un'icona personalizzata.

## Esempio 

Per modificare questa icona, aggiungere il seguente CSS al foglio di stile. Sostituite l'URL &lt;*risorsa*&gt; con l'URL dell'immagine selezionata per sostituire il contrassegno Livefyre predefinito.

```
.fyre-editor-container .fyre-editor-toolbar > .fyre-mention-menu .fyre-mention-item .fyre-mention-item-livefyre { 
    background: url(<your resource url>) no-repeat center; 
    background-position: 0px 0px; 
    background-size: 22px 22px; 
}
```
