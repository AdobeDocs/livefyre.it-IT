---
description: Modifica l'icona visualizzata per gli utenti Livefyre nel menu a discesa @menzioni.
title: Cambia icona @menzioni
exl-id: e078ef7f-7f16-4f5d-9152-95ae7fe7e4bd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 19%

---

# Cambia icona `@mention` {#change-mention-icon}

Modifica l’icona visualizzata per gli utenti Livefyre nel menu a discesa `@mention` .

Cambia l’icona Livefyre utilizzata nel menu a discesa `@mention` in un’icona a scelta, consentendoti di indicare i membri della community con la tua icona.

## Esempio 

Per modificare questa icona, aggiungere il seguente CSS al foglio di stile. Sostituisci &lt;*l&#39;url della risorsa* con l&#39;URL dell&#39;immagine selezionata per sostituire il badge Livefyre predefinito.

```
.fyre-editor-container .fyre-editor-toolbar > .fyre-mention-menu .fyre-mention-item .fyre-mention-item-livefyre { 
    background: url(<your resource url>) no-repeat center; 
    background-position: 0px 0px; 
    background-size: 22px 22px; 
}
```
