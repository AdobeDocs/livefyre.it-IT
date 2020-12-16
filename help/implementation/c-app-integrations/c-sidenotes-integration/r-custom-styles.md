---
description: Gli stili personalizzati vengono applicati attraverso un oggetto inserito nel costruttore Sidenotes.
seo-description: Gli stili personalizzati vengono applicati attraverso un oggetto inserito nel costruttore Sidenotes.
seo-title: Note Stili Personalizzati
title: Note Stili Personalizzati
uuid: 0f6d7ad6-1f6a-4ed2-b86a-0d03782e591e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%

---


# Note Stili personalizzati{#sidenotes-custom-styles}

Gli stili personalizzati vengono applicati attraverso un oggetto inserito nel costruttore Sidenotes.

Le &quot;chiavi&quot; sono chiavi oggetto che rappresentano elementi DOM, mentre le &quot;proprietà&quot; sono supportate per la chiave specifica. Ad esempio, per personalizzare lo stile del bloccoBtn (che è il pulsante che avvia il puntatore Sidenotes), si crea un oggetto come:

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
| `anonymousAvatar` | &quot;height&quot;, &quot;width&quot; | Immagine avatar anonima, a sinistra dell’editor dell’area di testo. |
| `blockBtn` | &quot;fontColor&quot;, &quot;fontSize&quot;, &quot;left&quot;, &quot;position&quot;, &quot;right&quot;, &quot;top&quot; | L&#39;icona &quot;Launcher&quot; posizionata accanto agli elementi specificati come barra laterale. |
| `blockBtnActive` | &quot;fontColor&quot;, &quot;fontSize&quot;, &quot;left&quot;, &quot;position&quot;, &quot;right&quot;, &quot;top&quot; | Icona di avvio quando si trova in uno stato attivo. |
| `commentAvatar` | &quot;height&quot;, &quot;width&quot; | Immagine avatar a sinistra delle note di livello superiore. |
| `commentBody` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Corpo del testo delle note concatenate. |
| `commentDisplayName` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Nome visualizzato dell’utente che ha lasciato una nota. |
| `commentDownvote` | &quot;fontColor&quot;, &quot;fontSize&quot; | Pulsante di voto su una nota. |
| `commentReplyExpand` | &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;borderWidth&quot;, &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Pulsante per espandere i thread con un numero elevato di risposte. |
| `commentTags` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Tag relativi a un utente su una nota. |
| `commentUpvote` | &quot;fontColor&quot;, &quot;fontSize&quot; | Pulsante di voto su una nota. |
| `editorTextarea` | &quot;height&quot;, &quot;width&quot;, &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Casella di immissione area di testo per lasciare le note. |
| `mediaBlockBtn` | &quot;fontColor&quot;, &quot;fontSize&quot;, &quot;left&quot;, &quot;position&quot;, &quot;right&quot;, &quot;top&quot; | Icona del modulo di avvio multimediale quando si trova sopra un elemento multimediale (img, video). |
| `mediaBlockBtnActive` | &quot;fontColor&quot;, &quot;fontSize&quot;, &quot;left&quot;, &quot;position&quot;, &quot;right&quot;, &quot;top&quot; | Icona del modulo di avvio multimediale in stato attivo. |
| `numSidenotes` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot;, &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;borderWidth&quot;, &quot;height&quot;, &quot;width&quot; | Fate clic sul pulsante che mostra il numero di note nella raccolta. |
| `numSidenotesPopover` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot;, &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;borderWidth&quot;, &quot;height&quot;, &quot;width&quot; | Puntatore con una breve spiegazione dei punti di interesse per l’utente. |
| `popover` | &quot;backgroundColor&quot; | Profilo visualizzato quando viene richiamata l&#39;icona di avvio. |
| `popoverArrowLeft` | &quot;backgroundImage&quot;, &quot;height&quot;, &quot;left&quot;, &quot;right&quot;, &quot;top&quot;, &quot;width&quot; | Elemento freccia sinistra sul puntatore che punta all&#39;elemento DOM contenente un&#39;icona di avvio. |
| `popoverArrorRight` | &quot;backgroundImage&quot;, &quot;height&quot;, &quot;left&quot;, &quot;right&quot;, &quot;top&quot;, &quot;width&quot; | Elemento freccia destra sul puntatore che punta all&#39;elemento DOM contenente un&#39;icona di avvio. |
| `popoverArrowTop` | &quot;backgroundImage&quot;, &quot;height&quot;, &quot;left&quot;, &quot;right&quot;, &quot;top&quot;, &quot;width&quot; | Elemento freccia in alto sul puntatore che punta all&#39;elemento DOM contenente un&#39;icona di avvio. |
| `replyAvatar` | &quot;height&quot;, &quot;width&quot; | Immagine avatar a sinistra delle note sul livello di risposta. |
| `streamPoweredBy` | &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;lineHeight&quot; | Piè di pagina &quot;Alimentato da&quot; sul puntatore. |
| `streamQueueButton` | &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;borderWidth&quot;, &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Pulsante per indicare quando le nuove note scorrono in un contenitore aperto. |
| `userAvatar` | &quot;height&quot;, &quot;width&quot; | Immagine avatar dell’utente autenticata, a sinistra dell’editor dell’area di testo. |

