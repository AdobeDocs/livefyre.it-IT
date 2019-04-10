---
description: Eventi disponibili a cui è possibile associare JavaScript per le app
  di conversazione (ad esempio Commenti, Chat, Blog live, Recensioni e Note a margine).
seo-description: Eventi disponibili a cui è possibile associare JavaScript per le
  app di conversazione (ad esempio Commenti, Chat, Blog live, Recensioni e Note a
  margine).
seo-title: Definizioni ed esempi degli eventi javascript
solution: Experience Manager
title: Definizioni ed esempi degli eventi javascript
uuid: 61 da 2 e 2 e -8 fcd -482 d -93 df-c 946 f 0475277
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Definizioni ed esempi degli eventi javascript{#javascript-events-definitions-and-examples}

Eventi disponibili a cui è possibile associare JavaScript per le app di conversazione (ad esempio Commenti, Chat, Blog live, Recensioni e Note a margine).

Livefyre fornisce eventi javascript per tenere traccia dell'attività utente nelle app di Livefyre. Ad esempio, potrebbe essere utile aggiornare la pagina quando gli utenti hanno o condividono contenuti su Twitter o Facebook oppure quando si pubblicano nuovi contenuti.

Livefyre consente anche di aggiungere eventi a integrazioni di analisi di terze parti (Adobe Analytics JS, Google Analytics, Gestione tag dinamica ecc.) per tenere traccia degli eventi delle app. Per ulteriori informazioni, rivolgetevi al responsabile dell'integrazione di terze parti per fornire gli eventi corretti.

Per eseguire un binding con questi eventi, aggiungete il codice seguente alla pagina quando create un'istanza dell'app su una pagina. Sostituite il nome dell'evento per `{eventName}`:

```
Livefyre.require(['fyre.conv#3'], function(Conv) { 
   new Conv(networkConfig, [convConfig], function(widget) { 
      widget.on('{eventName}', function (data) { 
         // Do something, perhaps using data 
      }); 
   }); 
});
```

>[!NOTE]
>
>Gli oggetti dati vengono forniti per tutti i gestori di eventi. Gli oggetti dati di esempio seguono ogni evento.

## Commentposting {#section_qfr_51p_xz}

Un utente ha pubblicato un commento.

* Un elemento padre di null è un nuovo commento.
* Un elemento padre di Nessuno è un commento che è stato modificato.
* Un numero per parent è l'ID principale della risposta.

```
data = { 
   authorId: "_u2012@livefyre.com" // The ID of the author of the comment  
   parent: "893549"  
      // The ID of the comment that this new comment is in reply to, else null 
   bodyHtml: "<p>42</>" // The HTML of the submitted Content 
   sharedToFacebook:true // Whether the comment was also posted to Facebook 
   sharedToTwitter:false // Whether the comment was also posted to Twitter 
   title: "demo title" // The title of the review (exists only for Reviews) 
   rating: [90] // Array of ratings for the review (exists only for Reviews) 
} 
```

## Commentflded {#section_szy_s1p_xz}

Un utente ha segnalato un commento.

```
data = { 
   targetId: "789347" // The ID of the comment that was flagged 
   type: ["disagree"] // The type of flag 
   notes: ["I don't entirely agree with this post"] // A note/reason for the flag 
}
```

## Commentliked {#section_vc1_r1p_xz}

A un utente piace un commento.

```
data = { 
   targetId: "245625" // The ID of the comment that was liked 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was liked 
} 
```

## Commentshared {#section_nqb_31p_xz}

Un utente ha condiviso un commento dallo streaming. (Questo evento non viene attivato quando gli utenti condividono dall'Editor commenti.) Questo evento viene attivato quando si fa clic sul pulsante Condividi.

```
data = { 
   targetId: "256255" // The ID of the comment that was shared 
   sharedToFacebook:false // Whether the comment was shared to Facebook 
   sharedToTwitter:true // Whether the comment was shared to Twitter 
}
```

## Commentcountupdated {#section_qdq_f1p_xz}

Il numero totale di commenti visibili in questa conversazione è stato modificato (incrementato o decrementato).

```
data: 34 // The total number of visible comments in the conversation (integer). 
```

## Userloggedin {#section_yjt_vz4_xz}

L'utente ha effettuato l'accesso.

```
data = { 
   avatar: "https://gravatar.com/avatar/50.jpg"  
      // Link to logged in user's avatar image 
   displayName: "NewUser" // Display name of the logged in user 
   id: "newuser@livefyre.com" // ID of the logged in user 
   isModerator:false // Boolean indicating whether logged in user is a moderator 
}
```

## Userloggedout {#section_tsg_5z4_xz}

Un utente ha disconnesso.

i dati non sono definiti.

## Socialmention {#section_a1w_tz4_xz}

Un utente ha incluso un @ menzioni in un commento. Restituisce un array di quanto segue:

```
data = { 
   id: '111111@fb.gw.livefyre.com' // ID of the mentioned user 
   displayName: 'testUser' // Display name of mentioned user 
   message: "@testUser Wow, I can't believe it either!"  
      // Message that was sent to the particular user 
   provider: 'twitter' // Provider to which the mention was shared 
} 
```

## Commentfeatured

Un utente moderatore ha presentato un commento. Restituisce un array di quanto segue:

```
data = { 
   targetId: "134234" // The ID of the comment that was featured 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was featured 
}
```

## Initialrendercomplete {#section_odc_4z4_xz}

Il flusso di commento è stato caricato e il set iniziale di contenuto è stato recuperato dal server e presentato all'utente.

i dati non sono definiti.

## Showmore {#section_pqg_nz4_xz}

Un utente ha fatto clic sul **[!UICONTROL Show More]** pulsante.

i dati non sono definiti.

## Userseguito {#section_xxw_jz4_xz}

Restituisce true quando un utente fa clic sul **[!UICONTROL Follow]** pulsante e false quando il contenuto viene postato nel flusso.

```
data = { 
   id: 'authorId@livefyre.com', 
   optIn: true 
}
```

## Userunfollowed {#section_wm1_gz4_xz}

Restituisce true quando un utente fa clic sul **pulsante Unsegui** e false quando il contenuto viene postato nel flusso.

```
data = { 
   id: 'authorId@livefyre.com', 
   optOut: true 
}
```

