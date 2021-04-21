---
description: Eventi disponibili a cui è possibile associare JavaScript per le app di conversazione (ad esempio Commenti, Chat, Blog live, Recensioni e Note a margine).
title: Definizioni ed esempi di eventi JavaScript
exl-id: 5b865974-69aa-4d51-ac26-60f1d8a114fc
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 11%

---

# Definizioni ed esempi di eventi JavaScript{#javascript-events-definitions-and-examples}

Eventi disponibili a cui è possibile associare JavaScript per le app di conversazione (ad esempio Commenti, Chat, Blog live, Recensioni e Note a margine).

Livefyre fornisce eventi JavaScript per monitorare l’attività dell’utente nelle app Livefyre. Ad esempio, puoi aggiornare la pagina quando gli utenti amano o condividono contenuti su Twitter o Facebook o quando vengono pubblicati nuovi contenuti.

Livefyre consente inoltre di aggiungere eventi alle integrazioni di analisi di terze parti (Adobe Analytics JS, Google Analytics, Dynamic Tag Management, ecc.) per tenere traccia degli eventi delle app. Per ulteriori informazioni, collabora con il tuo gestore di integrazione di terze parti per fornire gli eventi corretti.

Per eseguire il binding a questi eventi, aggiungi il codice seguente alla pagina durante la creazione di un’istanza dell’app su una pagina. Sostituisci il nome dell&#39;evento per `{eventName}`:

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
>Gli oggetti dati vengono forniti per tutti i gestori eventi. Gli oggetti dati di esempio seguono ogni evento.

## commentPosted {#section_qfr_51p_xz}

Un utente ha postato un commento.

* Un elemento padre di null è un nuovo commento.
* Un elemento padre di Nessuno è un commento modificato.
* Un numero per padre è l&#39;ID padre della risposta.

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

## commentContrassegnato {#section_szy_s1p_xz}

Un utente ha segnalato un commento.

```
data = { 
   targetId: "789347" // The ID of the comment that was flagged 
   type: ["disagree"] // The type of flag 
   notes: ["I don't entirely agree with this post"] // A note/reason for the flag 
}
```

## commentLiked {#section_vc1_r1p_xz}

A un utente piaceva un commento.

```
data = { 
   targetId: "245625" // The ID of the comment that was liked 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was liked 
} 
```

## commentShared {#section_nqb_31p_xz}

Un utente ha condiviso un commento dal flusso. (Questo evento non si attiva quando gli utenti condividono dall’editor Commenti). Questo evento viene attivato quando si fa clic sul pulsante Condividi .

```
data = { 
   targetId: "256255" // The ID of the comment that was shared 
   sharedToFacebook:false // Whether the comment was shared to Facebook 
   sharedToTwitter:true // Whether the comment was shared to Twitter 
}
```

## commentCountUpdated {#section_qdq_f1p_xz}

Il numero totale di commenti visibili in questa conversazione è cambiato (incrementato o diminuito).

```
data: 34 // The total number of visible comments in the conversation (integer). 
```

## userLoggedIn {#section_yjt_vz4_xz}

Un utente ha effettuato l&#39;accesso.

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

i dati non sono definiti.

## socialMention {#section_a1w_tz4_xz}

Un utente ha incluso un @mention in un commento. Restituisce una matrice dei seguenti elementi:

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

Un utente moderatore ha presentato un commento. Restituisce una matrice dei seguenti elementi:

```
data = { 
   targetId: "134234" // The ID of the comment that was featured 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was featured 
}
```

## initialRenderComplete {#section_odc_4z4_xz}

Il flusso dei commenti è stato caricato e il set iniziale di contenuti è stato recuperato dal server e visualizzato all’utente.

i dati non sono definiti.

## showMore {#section_pqg_nz4_xz}

Un utente ha fatto clic sul pulsante **[!UICONTROL Show More]** .

i dati non sono definiti.

## userSeguito {#section_xxw_jz4_xz}

Restituisce true quando un utente fa clic sul pulsante **[!UICONTROL Follow]** e false quando il contenuto viene inviato al flusso.

```
data = { 
   id: 'authorId@livefyre.com', 
   optIn: true 
}
```

## utenteNon seguito {#section_wm1_gz4_xz}

Restituisce true quando un utente fa clic sul pulsante **Non seguire** e false quando il contenuto viene inviato al flusso.

```
data = { 
   id: 'authorId@livefyre.com', 
   optOut: true 
}
```
