---
description: Potete ascoltare eventi su un'istanza di Sidenotes.
seo-description: Potete ascoltare eventi su un'istanza di Sidenotes.
seo-title: Eventi app Sidenotes
solution: Experience Manager
title: Eventi app Sidenotes
uuid: afca 4 b 03-c 370-41 ca-aa 12-45 bc 357517 ca
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Eventi app Sidenotes {#sidenotes-app-events}

Potete ascoltare eventi su un'istanza di Sidenotes.

I callback possono essere registrati con il `onmethod``removeListener` metodo e non registrati. Un `once` metodo è disponibile per comodità se la callback deve essere chiamata solo una volta e quindi non registrata.

```
var app = Livefyre.Sidenotes(convConfig); 
   app.once('sidenotes.initialized', function () { 
     // Sidenotes initialized!  
});
```

Per ulteriori informazioni sugli eventi Livefyre, consultate la pagina Eventi javascript nella sezione Riferimento.

| Chiave | Descrizione |
|--- |--- |
| sidenotes. initialized | Attivato quando l'istanza viene creata in un'istanza, presenta dati ed è sulla pagina. |
| sidenotes. commentflmarked | Attivato quando un commento è stato contrassegnato come commento. I dati contengono: <br><ul><li>`targetId`: id del commento contrassegnato</li><li>`type`: stringa tipo di flag `(offensive, off-topic, spam, disagree)`</li></ul> |
| `sidenotes.commentPosted` | Attivato quando è stato pubblicato un commento. I dati contengono: <br><ul><li> `authorId`: id dell'autore del commento </li><li>`bodyHtml`: corpo del commento </li><li> `parent`: id dell'elemento padre del commento o null</li></ul> |
| `sidenotes.commentShared` | Attivato quando un commento è stato condiviso. I dati contengono: <br><ul><li>`targetId`: id del commento condiviso </li><li> `sharedToFacebook`: se il commento è stato condiviso su Facebook </li><li>`sharedToTwitter`: se il commento è stato condiviso su Twitter</li></ul> |
| `sidenotes.commentVoted` | Attivato quando un commento è stato votato. I dati contengono: <br><ul><li>`targetId`: id del commento votato </li><li> `targetAuthorId`: id dell'autore il cui commento è stato votato</li><li> `type`: tipo di voto numerico: 0: ' clear ', 1: ' upvotè, or 2: ' downvò </li></ul> |
| `sidenotes.userLoggedIn` | Attivato quando un utente accede. I dati contengono: <br><ul><li>`avatar`: URL avatar per l'utente </li><li>`displayName`: nome visualizzato dell'utente</li><li>`id`: id dell'utente</li><li> `isModerator`: se l'utente è moderatore della raccolta corrente</li></ul> |
| `sidenotes.userLoggedOut` | Attivato quando un utente effettua il login |
