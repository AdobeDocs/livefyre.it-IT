---
description: Potete ascoltare gli eventi su un’istanza di Sidenotes.
seo-description: Potete ascoltare gli eventi su un’istanza di Sidenotes.
seo-title: Sidenotes Eventi App
solution: Experience Manager
title: Sidenotes Eventi App
uuid: afca4b03-c370-41ca-aa12-45bc357517ca
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934

---


# Sidenotes Eventi App {#sidenotes-app-events}

Potete ascoltare gli eventi su un’istanza di Sidenotes.

Le callback possono essere registrate con il `onmethod` `removeListener` metodo e non registrate con esso. Un `once` metodo è disponibile per comodità se il callback deve essere chiamato solo una volta e poi non registrato.

```
var app = Livefyre.Sidenotes(convConfig); 
   app.once('sidenotes.initialized', function () { 
     // Sidenotes initialized!  
});
```

Per ulteriori informazioni sugli eventi Livefyre, consultate la pagina Eventi JavaScript nella sezione Riferimento.

| Chiave | Descrizione |
|--- |--- |
| sidenotes.initialize | Generato quando l'app viene creata, dispone di dati ed è sulla pagina. |
| sidenotes.commentFlagged | Generato quando un commento è stato contrassegnato. I dati contengono: <br><ul><li>`targetId`: id del commento contrassegnato</li><li>`type`: flag type string `(offensive, off-topic, spam, disagree)`</li></ul> |
| `sidenotes.commentPosted` | Generato quando viene pubblicato un commento. I dati contengono: <br><ul><li> `authorId`: id dell’autore del commento </li><li>`bodyHtml`: corpo del commento </li><li> `parent`: id dell'elemento padre del commento o null</li></ul> |
| `sidenotes.commentShared` | Generato quando un commento è stato condiviso. I dati contengono: <br><ul><li>`targetId`: id del commento condiviso </li><li> `sharedToFacebook`: se il commento è stato condiviso su Facebook </li><li>`sharedToTwitter`: se il commento è stato condiviso su Twitter</li></ul> |
| `sidenotes.commentVoted` | Generato quando si vota un commento. I dati contengono: <br><ul><li>`targetId`: id del commento sul quale è stato votato </li><li> `targetAuthorId`: id dell'autore il cui commento è stato votato</li><li> `type`: tipo di voto numerico:0: "clear", 1: "voto contrario", o 2: "voto negativo"</li></ul> |
| `sidenotes.userLoggedIn` | Generato quando un utente effettua l’accesso. I dati contengono: <br><ul><li>`avatar`: url avatar per l’utente </li><li>`displayName`: nome visualizzato dell'utente</li><li>`id`: id dell’utente</li><li> `isModerator`: se l'utente è un moderatore della raccolta corrente</li></ul> |
| `sidenotes.userLoggedOut` | Generato quando un utente si disconnette |
