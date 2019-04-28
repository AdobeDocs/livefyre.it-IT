---
description: Gli stili personalizzati vengono applicati tramite un oggetto inserito nella costruttore Sidenotes.
seo-description: Gli stili personalizzati vengono applicati tramite un oggetto inserito nella costruttore Sidenotes.
seo-title: Stili personalizzati
title: Stili personalizzati
uuid: 0 f 6 d 7 ad 6-1 f 6 a -4 ed 2 ed 86 a -0 d 03782 e 591 e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Stili personalizzati{#sidenotes-custom-styles}

Gli stili personalizzati vengono applicati tramite un oggetto inserito nella costruttore Sidenotes.

Le «chiavi» sono chiavi oggetti che rappresentano elementi DOM, mentre «proprietà» sono proprietà CSS per la chiave particolare. Ad esempio, per personalizzare lo stile di blocktn (ovvero il pulsante che avvia il popover Sidenotes), si crea un oggetto come:

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
| `anonymousAvatar` | &#39; height &#39;,&#39;width &#39; | Immagine avatar anonima, a sinistra dell&#39;editor dell&#39;area di testo. |
| `blockBtn` | &#39; Fontcolor &#39;,&#39;fontsizè,&#39;left &#39;,&#39;position &#39;,&#39;right &#39;,&#39;top | L &#39;«icona di avvio» posizionata accanto agli elementi specificati come in sidenote. |
| `blockBtnActive` | &#39; Fontcolor &#39;,&#39;fontsizè,&#39;left &#39;,&#39;position &#39;,&#39;right &#39;,&#39;top | Icona di avvio quando si attiva uno stato attivo. |
| `commentAvatar` | &#39; height &#39;,&#39;width &#39; | Immagine avatar a sinistra delle note di livello principale. |
| `commentBody` | &#39; Fontcolor &#39;,&#39;fontfamily &#39;,&#39;fontsizè,&#39;fontweight &#39;,&#39;lineheight &#39; | Corpo del testo delle note concatenate. |
| `commentDisplayName` | &#39; Fontcolor &#39;,&#39;fontfamily &#39;,&#39;fontsizè,&#39;fontweight &#39;,&#39;lineheight &#39; | Nome visualizzato dell&#39;utente che ha lasciato una nota. |
| `commentDownvote` | &#39; Fontcolor &#39;,&#39;fontsizè | Pulsante Downvoto su una nota. |
| `commentReplyExpand` | &#39; Backgroundcolor &#39;,&#39;bordercolor &#39;,&#39;borderwidth &#39;,&#39;fontcolor &#39;,&#39;fontfamily &#39;,&#39;fontsizè,&#39;fontweight &#39;,&#39;lineheight &#39; | Pulsante per espandere i thread con un numero elevato di risposte. |
| `commentTags` | &#39; Fontcolor &#39;,&#39;fontfamily &#39;,&#39;fontsizè,&#39;fontweight &#39;,&#39;lineheight &#39; | Tag su un utente. |
| `commentUpvote` | &#39; Fontcolor &#39;,&#39;fontsizè | Pulsante Upvote su una nota. |
| `editorTextarea` | &#39; height &#39;,&#39;width &#39;,&#39;fontcolor &#39;,&#39;fontfamily &#39;,&#39;fontsizè,&#39;fontweight &#39;,&#39;lineheight &#39; | Casella di testo Area di testo per uscire dalle note. |
| `mediaBlockBtn` | &#39; Fontcolor &#39;,&#39;fontsizè,&#39;left &#39;,&#39;position &#39;,&#39;right &#39;,&#39;top | Icona di avvio file multimediali quando si trova sopra un elemento multimediale (img, video). |
| `mediaBlockBtnActive` | &#39; Fontcolor &#39;,&#39;fontsizè,&#39;left &#39;,&#39;position &#39;,&#39;right &#39;,&#39;top | Icona di avvio file multimediali in stato attivo. |
| `numSidenotes` | &#39; Fontcolor &#39;,&#39;fontfamily &#39;,&#39;fontsizè,&#39;fontweight &#39;,&#39;lineheight &#39;,&#39;backgroundcolor &#39;,&#39;bordercolor &#39;,&#39;borderwidth &#39;,&#39;height &#39;,&#39;width | Pulsante selezionabile che mostra il numero di Sidenotes nella raccolta. |
| `numSidenotesPopover` | &#39; Fontcolor &#39;,&#39;fontfamily &#39;,&#39;fontsizè,&#39;fontweight &#39;,&#39;lineheight &#39;,&#39;backgroundcolor &#39;,&#39;bordercolor &#39;,&#39;borderwidth &#39;,&#39;height &#39;,&#39;width | Contenitore con breve spiegazione di Sidenotes. |
| `popover` | &#39; Backgroundcolor &#39; | Contenitore che viene richiamato quando l&#39;icona di avvio viene richiamata. |
| `popoverArrowLeft` | &#39; Backgroundimagè,&#39;height &#39;,&#39;left &#39;,&#39;right &#39;,&#39;top &#39;,&#39;width &#39; | Elemento freccia sinistra nel contenitore che indica l&#39;elemento DOM contenente un&#39;icona di avvio. |
| `popoverArrorRight` | &#39; Backgroundimagè,&#39;height &#39;,&#39;left &#39;,&#39;right &#39;,&#39;top &#39;,&#39;width &#39; | Elemento freccia destra nel contenitore che indica l&#39;elemento DOM contenente un&#39;icona di avvio. |
| `popoverArrowTop` | &#39; Backgroundimagè,&#39;height &#39;,&#39;left &#39;,&#39;right &#39;,&#39;top &#39;,&#39;width &#39; | Elemento freccia superiore nel contenitore che punta all&#39;elemento DOM contenente un&#39;icona di avvio. |
| `replyAvatar` | &#39; height &#39;,&#39;width &#39; | Immagine avatar a sinistra delle note sul livello di risposta. |
| `streamPoweredBy` | &#39; Backgroundcolor &#39;,&#39;bordercolor &#39;,&#39;lineheight &#39; | «Gestito da» nel contenitore. |
| `streamQueueButton` | &#39; Backgroundcolor &#39;,&#39;bordercolor &#39;,&#39;borderwidth &#39;,&#39;fontcolor &#39;,&#39;fontfamily &#39;,&#39;fontsizè,&#39;fontweight &#39;,&#39;lineheight &#39; | Pulsante per indicare quando le nuove note vengono trasmesse in un contenitore aperto. |
| `userAvatar` | &#39; height &#39;,&#39;width &#39; | Immagine avatar dell&#39;utente autenticata, a sinistra dell&#39;editor dell&#39;area di testo. |

