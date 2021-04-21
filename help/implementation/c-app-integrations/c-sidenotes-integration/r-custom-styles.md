---
description: Gli stili personalizzati vengono applicati attraverso un oggetto inserito nel costruttore Sidenotes.
title: Note Sidenote Stili Personalizzati
exl-id: 846605b7-a21e-4600-bf17-18841d2ed96d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Note Stili personalizzati{#sidenotes-custom-styles}

Gli stili personalizzati vengono applicati attraverso un oggetto inserito nel costruttore Sidenotes.

Le &quot;chiavi&quot; sono chiavi oggetto che rappresentano elementi DOM, mentre le &quot;proprietà&quot; sono proprietà CSS supportate per la chiave specifica. Ad esempio, per personalizzare lo stile del blockBtn (che è il pulsante che avvia il puntatore Note a margine), si crea un oggetto come:

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
| `anonymousAvatar` | &quot;height&quot;, &quot;width&quot; | Immagine avatar anonima, a sinistra dell&#39;editor dell&#39;area di testo. |
| `blockBtn` | &quot;fontColor&quot;, &quot;fontSize&quot;, &quot;left&quot;, &quot;position&quot;, &quot;right&quot;, &quot;top&quot; | L’&quot;icona del lanciatore&quot; posta accanto agli elementi specificati come separabili. |
| `blockBtnActive` | &quot;fontColor&quot;, &quot;fontSize&quot;, &quot;left&quot;, &quot;position&quot;, &quot;right&quot;, &quot;top&quot; | Icona di avvio quando è in uno stato attivo. |
| `commentAvatar` | &quot;height&quot;, &quot;width&quot; | Immagine avatar a sinistra delle note di livello superiore. |
| `commentBody` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Corpo del testo delle note filettate. |
| `commentDisplayName` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Visualizza il nome dell&#39;utente che ha lasciato una nota. |
| `commentDownvote` | &quot;fontColor&quot;, &quot;fontSize&quot; | Pulsante di voto su una nota. |
| `commentReplyExpand` | &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;borderWidth&quot;, &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Pulsante per espandere i thread con un numero elevato di risposte. |
| `commentTags` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Tag relativi a un utente su una nota. |
| `commentUpvote` | &quot;fontColor&quot;, &quot;fontSize&quot; | Pulsante di voto su una nota. |
| `editorTextarea` | &quot;height&quot;, &quot;width&quot;, &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Casella di immissione area di testo per lasciare le note. |
| `mediaBlockBtn` | &quot;fontColor&quot;, &quot;fontSize&quot;, &quot;left&quot;, &quot;position&quot;, &quot;right&quot;, &quot;top&quot; | Icona del modulo di avvio multimediale quando è sopra un elemento multimediale (img, video). |
| `mediaBlockBtnActive` | &quot;fontColor&quot;, &quot;fontSize&quot;, &quot;left&quot;, &quot;position&quot;, &quot;right&quot;, &quot;top&quot; | Icona del modulo di avvio multimediale in uno stato attivo. |
| `numSidenotes` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot;, &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;borderWidth&quot;, &quot;height&quot;, &quot;width&quot; | Pulsante selezionabile che mostra il numero di note nella raccolta. |
| `numSidenotesPopover` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot;, &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;borderWidth&quot;, &quot;height&quot;, &quot;width&quot; | Popover con una breve spiegazione di Note a margine per l&#39;utente. |
| `popover` | &quot;backgroundColor&quot; | Pover che viene visualizzato quando viene richiamata l’icona del lanciatore. |
| `popoverArrowLeft` | &quot;backgroundImage&quot;, &quot;height&quot;, &quot;left&quot;, &quot;right&quot;, &quot;top&quot;, &quot;width&quot; | Elemento freccia a sinistra sul puntatore che punta all’elemento DOM contenente un’icona di avvio. |
| `popoverArrorRight` | &quot;backgroundImage&quot;, &quot;height&quot;, &quot;left&quot;, &quot;right&quot;, &quot;top&quot;, &quot;width&quot; | Elemento freccia a destra sul puntatore che punta all’elemento DOM contenente un’icona di avvio. |
| `popoverArrowTop` | &quot;backgroundImage&quot;, &quot;height&quot;, &quot;left&quot;, &quot;right&quot;, &quot;top&quot;, &quot;width&quot; | Elemento freccia in alto sul puntatore che punta all’elemento DOM contenente un’icona di avvio. |
| `replyAvatar` | &quot;height&quot;, &quot;width&quot; | Immagine avatar a sinistra delle note del livello di risposta. |
| `streamPoweredBy` | &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;lineHeight&quot; | Piè di pagina &quot;Powered by&quot; sul pover. |
| `streamQueueButton` | &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;borderWidth&quot;, &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Pulsante per indicare quando le nuove note scorrono in un pover aperto. |
| `userAvatar` | &quot;height&quot;, &quot;width&quot; | Immagine avatar dell’utente autenticata, a sinistra dell’editor dell’area di testo. |
