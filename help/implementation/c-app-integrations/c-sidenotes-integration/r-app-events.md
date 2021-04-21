---
description: È possibile ascoltare gli eventi su un'istanza di Sidenotes.
title: Sidenote Eventi App
exl-id: e341ca76-002d-425c-8d1a-35c3253fb254
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Note eventi app {#sidenotes-app-events}

È possibile ascoltare gli eventi su un&#39;istanza di Sidenotes.

I callback possono essere registrati con il metodo `onmethod` e non registrati con il metodo `removeListener`. È disponibile un metodo `once` per comodità se il callback deve essere chiamato una sola volta e poi non registrato.

```
var app = Livefyre.Sidenotes(convConfig); 
   app.once('sidenotes.initialized', function () { 
     // Sidenotes initialized!  
});
```

Per ulteriori informazioni sugli eventi Livefyre, consulta la pagina Eventi JavaScript nella sezione Riferimento .

| Chiave | Descrizione |
|--- |--- |
| sidenotes.initialized | Generato quando l’app viene creata, dispone di dati ed è presente nella pagina. |
| sidenotes.commentFlagged | Generato quando un commento è stato contrassegnato. I dati contengono: <br><ul><li>`targetId`: id del commento contrassegnato</li><li>`type`: stringa del tipo di flag  `(offensive, off-topic, spam, disagree)`</li></ul> |
| `sidenotes.commentPosted` | Generato quando è stato pubblicato un commento. I dati contengono: <br><ul><li> `authorId`: id dell’autore del commento </li><li>`bodyHtml`: corpo del commento </li><li> `parent`: id dell&#39;elemento padre del commento o null</li></ul> |
| `sidenotes.commentShared` | Generato quando un commento è stato condiviso. I dati contengono: <br><ul><li>`targetId`: id del commento condiviso </li><li> `sharedToFacebook`: se il commento è stato condiviso su Facebook </li><li>`sharedToTwitter`: se il commento è stato condiviso su Twitter</li></ul> |
| `sidenotes.commentVoted` | Viene attivato quando viene votato un commento. I dati contengono: <br><ul><li>`targetId`: id del commento che è stato votato </li><li> `targetAuthorId`: id dell&#39;autore il cui commento è stato votato</li><li> `type`: tipo di voto numerico: 0: &quot;clear&quot;, 1: &quot;voto contrario&quot;, o 2: &quot;voto negativo&quot;</li></ul> |
| `sidenotes.userLoggedIn` | Generato quando un utente effettua l’accesso. I dati contengono: <br><ul><li>`avatar`: url avatar per l’utente </li><li>`displayName`: nome visualizzato dell&#39;utente</li><li>`id`: id dell&#39;utente</li><li> `isModerator`: se l&#39;utente è un moderatore della raccolta corrente</li></ul> |
| `sidenotes.userLoggedOut` | Generato quando un utente si disconnette |
