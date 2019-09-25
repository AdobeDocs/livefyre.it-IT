---
description: Gli stili personalizzati vengono applicati attraverso un oggetto inserito nel costruttore Sidenotes.
seo-description: Gli stili personalizzati vengono applicati attraverso un oggetto inserito nel costruttore Sidenotes.
seo-title: Note Stili Personalizzati
title: Note Stili Personalizzati
uuid: 0f6d7ad6-1f6a-4ed2-b86a-0d03782e591e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Note Stili Personalizzati{#sidenotes-custom-styles}

Gli stili personalizzati vengono applicati attraverso un oggetto inserito nel costruttore Sidenotes.

Le "chiavi" sono chiavi oggetto che rappresentano elementi DOM, mentre le "proprietà" sono supportate per la chiave specifica. Ad esempio, per personalizzare lo stile del bloccoBtn (che è il pulsante che avvia il puntatore Sidenotes), si crea un oggetto come:

```
var styles = { 
   'blockBtn': { 
      'fontColor': '#555', 
      'fontSize': '18px' 
   } 
}; 
new Livefyre.Sidenotes({ 
   customStyles: styles, 
      ...  
})
```

| **Chiave** | **Proprietà** | Descrizione |
|---|---|---|
| `anonymousAvatar` | "height", "width" | Immagine avatar anonima, a sinistra dell’editor dell’area di testo. |
| `blockBtn` | "fontColor", "fontSize", "left", "position", "right", "top" | L'icona "Launcher" posizionata accanto agli elementi specificati come barra laterale. |
| `blockBtnActive` | "fontColor", "fontSize", "left", "position", "right", "top" | Icona di avvio quando si trova in uno stato attivo. |
| `commentAvatar` | "height", "width" | Immagine avatar a sinistra delle note di livello superiore. |
| `commentBody` | "fontColor", "fontFamily", "fontSize", "fontWeight", "lineHeight" | Corpo del testo delle note concatenate. |
| `commentDisplayName` | "fontColor", "fontFamily", "fontSize", "fontWeight", "lineHeight" | Nome visualizzato dell’utente che ha lasciato una nota. |
| `commentDownvote` | "fontColor", "fontSize" | Pulsante di voto su una nota. |
| `commentReplyExpand` | "backgroundColor", "borderColor", "borderWidth", "fontColor", "fontFamily", "fontSize", "fontWeight", "lineHeight" | Pulsante per espandere i thread con un numero elevato di risposte. |
| `commentTags` | "fontColor", "fontFamily", "fontSize", "fontWeight", "lineHeight" | Tag relativi a un utente su una nota. |
| `commentUpvote` | "fontColor", "fontSize" | Pulsante di voto su una nota. |
| `editorTextarea` | "height", "width", "fontColor", "fontFamily", "fontSize", "fontWeight", "lineHeight" | Casella di immissione area di testo per lasciare le note. |
| `mediaBlockBtn` | "fontColor", "fontSize", "left", "position", "right", "top" | Icona del modulo di avvio multimediale quando si trova sopra un elemento multimediale (img, video). |
| `mediaBlockBtnActive` | "fontColor", "fontSize", "left", "position", "right", "top" | Icona del modulo di avvio multimediale in stato attivo. |
| `numSidenotes` | "fontColor", "fontFamily", "fontSize", "fontWeight", "lineHeight", "backgroundColor", "borderColor", "borderWidth", "height", "width" | Fate clic sul pulsante che mostra il numero di note nella raccolta. |
| `numSidenotesPopover` | "fontColor", "fontFamily", "fontSize", "fontWeight", "lineHeight", "backgroundColor", "borderColor", "borderWidth", "height", "width" | Puntatore con una breve spiegazione dei punti di interesse per l’utente. |
| `popover` | "backgroundColor" | Profilo visualizzato quando viene richiamata l'icona di avvio. |
| `popoverArrowLeft` | "backgroundImage", "height", "left", "right", "top", "width" | Elemento freccia sinistra sul puntatore che punta all'elemento DOM contenente un'icona di avvio. |
| `popoverArrorRight` | "backgroundImage", "height", "left", "right", "top", "width" | Elemento freccia destra sul puntatore che punta all'elemento DOM contenente un'icona di avvio. |
| `popoverArrowTop` | "backgroundImage", "height", "left", "right", "top", "width" | Elemento freccia in alto sul puntatore che punta all'elemento DOM contenente un'icona di avvio. |
| `replyAvatar` | "height", "width" | Immagine avatar a sinistra delle note sul livello di risposta. |
| `streamPoweredBy` | "backgroundColor", "borderColor", "lineHeight" | Piè di pagina "Alimentato da" sul puntatore. |
| `streamQueueButton` | "backgroundColor", "borderColor", "borderWidth", "fontColor", "fontFamily", "fontSize", "fontWeight", "lineHeight" | Pulsante per indicare quando le nuove note scorrono in un contenitore aperto. |
| `userAvatar` | "height", "width" | Immagine avatar dell’utente autenticata, a sinistra dell’editor dell’area di testo. |

