---
description: Modifica l'icona visualizzata per gli utenti Livefyre nel menu a discesa @mention.
seo-description: Modifica l'icona visualizzata per gli utenti Livefyre nel menu a discesa @menzioni.
seo-title: Cambia icona @menzioni
solution: Experience Manager
title: Cambia icona @mention
uuid: a395f4ff-a774-454a-8d94-4a3371d8cc2c
translation-type: tm+mt
source-git-commit: 0d2ff61b1db6100de1d59e6e20c1175f015a78c5
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 31%

---


# Modifica icona `@mention` {#change-mention-icon}

Modificate l&#39;icona visualizzata per gli utenti Livefyre nel menu a discesa `@mention`.

Modificate l&#39;icona Livefyre utilizzata nel menu a discesa `@mention` impostando un&#39;icona di vostra scelta, in modo da poter indicare i membri della community con una propria icona.

## Esempio 

Per modificare questa icona, aggiungere il seguente CSS al foglio di stile. Sostituite &lt;*l&#39;URL della risorsa*> con l&#39;URL dell&#39;immagine selezionata per sostituire il contrassegno Livefyre predefinito.

```
.fyre-editor-container .fyre-editor-toolbar > .fyre-mention-menu .fyre-mention-item .fyre-mention-item-livefyre { 
    background: url(<your resource url>) no-repeat center; 
    background-position: 0px 0px; 
    background-size: 22px 22px; 
}
```
