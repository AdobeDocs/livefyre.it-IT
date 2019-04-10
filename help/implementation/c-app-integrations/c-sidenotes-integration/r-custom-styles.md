---
description: Gli stili personalizzati vengono applicati tramite un oggetto inserito
  nella costruttore Sidenotes.
seo-description: Gli stili personalizzati vengono applicati tramite un oggetto inserito
  nella costruttore Sidenotes.
seo-title: Stili personalizzati
title: Stili personalizzati
uuid: 0 f 6 d 7 ad 6-1 f 6 a -4 ed 2 ed 86 a -0 d 03782 e 591 e
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

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
| `anonymousAvatar` | ' height ','width ' | Immagine avatar anonima, a sinistra dell'editor dell'area di testo. |
| `blockBtn` | ' Fontcolor ','fontsizè,'left ','position ','right ','top | L '«icona di avvio» posizionata accanto agli elementi specificati come in sidenote. |
| `blockBtnActive` | ' Fontcolor ','fontsizè,'left ','position ','right ','top | Icona di avvio quando si attiva uno stato attivo. |
| `commentAvatar` | ' height ','width ' | Immagine avatar a sinistra delle note di livello principale. |
| `commentBody` | ' Fontcolor ','fontfamily ','fontsizè,'fontweight ','lineheight ' | Corpo del testo delle note concatenate. |
| `commentDisplayName` | ' Fontcolor ','fontfamily ','fontsizè,'fontweight ','lineheight ' | Nome visualizzato dell'utente che ha lasciato una nota. |
| `commentDownvote` | ' Fontcolor ','fontsizè | Pulsante Downvoto su una nota. |
| `commentReplyExpand` | ' Backgroundcolor ','bordercolor ','borderwidth ','fontcolor ','fontfamily ','fontsizè,'fontweight ','lineheight ' | Pulsante per espandere i thread con un numero elevato di risposte. |
| `commentTags` | ' Fontcolor ','fontfamily ','fontsizè,'fontweight ','lineheight ' | Tag su un utente. |
| `commentUpvote` | ' Fontcolor ','fontsizè | Pulsante Upvote su una nota. |
| `editorTextarea` | ' height ','width ','fontcolor ','fontfamily ','fontsizè,'fontweight ','lineheight ' | Casella di testo Area di testo per uscire dalle note. |
| `mediaBlockBtn` | ' Fontcolor ','fontsizè,'left ','position ','right ','top | Icona di avvio file multimediali quando si trova sopra un elemento multimediale (img, video). |
| `mediaBlockBtnActive` | ' Fontcolor ','fontsizè,'left ','position ','right ','top | Icona di avvio file multimediali in stato attivo. |
| `numSidenotes` | ' Fontcolor ','fontfamily ','fontsizè,'fontweight ','lineheight ','backgroundcolor ','bordercolor ','borderwidth ','height ','width | Pulsante selezionabile che mostra il numero di Sidenotes nella raccolta. |
| `numSidenotesPopover` | ' Fontcolor ','fontfamily ','fontsizè,'fontweight ','lineheight ','backgroundcolor ','bordercolor ','borderwidth ','height ','width | Contenitore con breve spiegazione di Sidenotes. |
| `popover` | ' Backgroundcolor ' | Contenitore che viene richiamato quando l'icona di avvio viene richiamata. |
| `popoverArrowLeft` | ' Backgroundimagè,'height ','left ','right ','top ','width ' | Elemento freccia sinistra nel contenitore che indica l'elemento DOM contenente un'icona di avvio. |
| `popoverArrorRight` | ' Backgroundimagè,'height ','left ','right ','top ','width ' | Elemento freccia destra nel contenitore che indica l'elemento DOM contenente un'icona di avvio. |
| `popoverArrowTop` | ' Backgroundimagè,'height ','left ','right ','top ','width ' | Elemento freccia superiore nel contenitore che punta all'elemento DOM contenente un'icona di avvio. |
| `replyAvatar` | ' height ','width ' | Immagine avatar a sinistra delle note sul livello di risposta. |
| `streamPoweredBy` | ' Backgroundcolor ','bordercolor ','lineheight ' | «Gestito da» nel contenitore. |
| `streamQueueButton` | ' Backgroundcolor ','bordercolor ','borderwidth ','fontcolor ','fontfamily ','fontsizè,'fontweight ','lineheight ' | Pulsante per indicare quando le nuove note vengono trasmesse in un contenitore aperto. |
| `userAvatar` | ' height ','width ' | Immagine avatar dell'utente autenticata, a sinistra dell'editor dell'area di testo. |

