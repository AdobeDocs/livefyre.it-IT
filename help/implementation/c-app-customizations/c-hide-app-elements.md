---
description: Rimuovete i componenti standard Livefyre App dall'app.
seo-description: Rimuovete i componenti standard Livefyre App dall'app.
seo-title: Nascondi elementi app
solution: Experience Manager
title: Nascondi elementi app
uuid: ea 090 b 6 e -99 f 5-4 bd 7-aa 9 e-d 39 a 4 dff 1543
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Nascondi elementi app{#hide-app-elements}

Rimuovete i componenti standard Livefyre App dall'app.

Utilizzate CSS per nascondere elementi Livefyre App predefiniti dalla pagina, consentendovi di personalizzare l'esperienza utente in base alle vostre esigenze.

Per nascondere elementi dall'app, impostate semplicemente la visualizzazione su Nessuno.

Esempi:

```
/* Hide the 'reply' button */ 
.fyre-comment-reply { 
    display: none !important; 
} 
  
/* Hide all user avatars */ 
.fyre-comment-user .fyre-mention-item-avatar .fyre-listener-avatars .fyre-avatar fyre-user-avatar-25 { 
    display: none !important; 
} 
.fyre-comment-head .fyre-comment-body .fyre-comment-footer .fyre-comment-divider { 
    margin-left: 0; 
} 
  
/* Hide 'Edit Profile' link */ 
.fyre-edit-profile-link { 
    display: none !important; 
} 
  
/* Hide 'Logout' link */ 
.fyre-logout-link { 
    display: none; 
} 
  
/* Hide 'Comment Notifier' */ 
.fyre-notifier-message { 
    display:none; 
}
```
