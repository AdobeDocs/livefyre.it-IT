---
description: Eventi disponibili a cui è possibile associare JavaScript per le app di conversazione (ad esempio Commenti, Chat, Blog live, Recensioni e Note a margine).
seo-description: Eventi disponibili a cui è possibile associare JavaScript per le app di conversazione (ad esempio Commenti, Chat, Blog live, Recensioni e Note a margine).
seo-title: Definizioni ed esempi di eventi JavaScript
solution: Experience Manager
title: Definizioni ed esempi di eventi JavaScript
uuid: 61da2e2e-8fcd-482d-93df-c946f0475277
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Definizioni ed esempi di eventi JavaScript{#javascript-events-definitions-and-examples}

Eventi disponibili a cui è possibile associare JavaScript per le app di conversazione (ad esempio Commenti, Chat, Blog live, Recensioni e Note a margine).

Livefyre fornisce eventi JavaScript per monitorare l'attività degli utenti nelle app Livefyre. Ad esempio, potete decidere di aggiornare la pagina quando gli utenti desiderano o condividono contenuti su Twitter o Facebook, oppure quando vengono pubblicati nuovi contenuti.

Livefyre consente inoltre di aggiungere eventi alle integrazioni di analisi di terze parti (Adobe Analytics JS, Google Analytics, Gestione tag dinamica, ecc.) per tenere traccia degli eventi delle app. Per ulteriori informazioni, rivolgiti al tuo responsabile dell'integrazione di terze parti per fornire gli eventi corretti.

Per eseguire un binding con questi eventi, aggiungi il codice seguente alla pagina quando crei un'istanza dell'app su una pagina. Sostituite il nome dell’evento per `{eventName}`:

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
>Gli oggetti dati sono forniti per tutti i gestori di eventi. Gli oggetti dati di esempio seguono ogni evento.

## commentPosted {#section_qfr_51p_xz}

Un utente ha pubblicato un commento.

* Un elemento padre di null è un nuovo commento.
* Un elemento padre di None è un commento modificato.
* Un numero per parent è l'ID padre della risposta.

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

## commentFlagged {#section_szy_s1p_xz}

Un utente ha segnalato un commento.

```
data = { 
   targetId: "789347" // The ID of the comment that was flagged 
   type: ["disagree"] // The type of flag 
   notes: ["I don't entirely agree with this post"] // A note/reason for the flag 
}
```

## commentLiked {#section_vc1_r1p_xz}

A un utente è piaciuto un commento.

```
data = { 
   targetId: "245625" // The ID of the comment that was liked 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was liked 
} 
```

## commentShared {#section_nqb_31p_xz}

Un utente ha condiviso un commento dal flusso. (Questo evento non viene attivato quando gli utenti condividono l’audio dall’editor commenti). Questo evento viene attivato quando si fa clic sul pulsante Condividi.

```
data = { 
   targetId: "256255" // The ID of the comment that was shared 
   sharedToFacebook:false // Whether the comment was shared to Facebook 
   sharedToTwitter:true // Whether the comment was shared to Twitter 
}
```

## commentCountUpdated {#section_qdq_f1p_xz}

Il numero totale di commenti visibili in questa conversazione è cambiato (incrementato o decrementato).

```
data: 34 // The total number of visible comments in the conversation (integer). 
```

## userLoggedIn {#section_yjt_vz4_xz}

Un utente ha eseguito l'accesso.

```
data = { 
   avatar: "https://gravatar.com/avatar/50.jpg"  
      // Link to logged in user's avatar image 
   displayName: "NewUser" // Display name of the logged in user 
   id: "newuser@livefyre.com" // ID of the logged in user 
   isModerator:false // Boolean indicating whether logged in user is a moderator 
}
```

## userLoggedOut {#section_tsg_5z4_xz}

Un utente si è disconnesso.

data non definito.

## socialMention {#section_a1w_tz4_xz}

Un utente ha incluso un @reference in un commento. Restituisce un array dei seguenti elementi:

```
data = { 
   id: '111111@fb.gw.livefyre.com' // ID of the mentioned user 
   displayName: 'testUser' // Display name of mentioned user 
   message: "@testUser Wow, I can't believe it either!"  
      // Message that was sent to the particular user 
   provider: 'twitter' // Provider to which the mention was shared 
} 
```

## commentFeatured

Un utente moderatore ha presentato un commento. Restituisce un array dei seguenti elementi:

```
data = { 
   targetId: "134234" // The ID of the comment that was featured 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was featured 
}
```

## initialRenderComplete {#section_odc_4z4_xz}

Il flusso dei commenti è stato caricato e il set iniziale di contenuti è stato recuperato dal server e visualizzato all'utente.

data non definito.

## showMore {#section_pqg_nz4_xz}

Un utente ha fatto clic sul **[!UICONTROL Show More]** pulsante.

data non definito.

## userFollowed {#section_xxw_jz4_xz}

Restituisce true quando un utente fa clic sul **[!UICONTROL Follow]** pulsante, false quando il contenuto viene inviato al flusso.

```
data = { 
   id: 'authorId@livefyre.com', 
   optIn: true 
}
```

## userUnFollow {#section_wm1_gz4_xz}

Restituisce true quando un utente fa clic sul pulsante **Non seguire** e false quando il contenuto viene inviato al flusso.

```
data = { 
   id: 'authorId@livefyre.com', 
   optOut: true 
}
```

