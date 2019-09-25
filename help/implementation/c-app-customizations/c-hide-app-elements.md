---
description: Rimuovere dall'app i componenti standard dell'app Livefyre.
seo-description: Rimuovere dall'app i componenti standard dell'app Livefyre.
seo-title: Nascondi elementi app
solution: Experience Manager
title: Nascondi elementi app
uuid: ea090b6e-99f5-4bd7-aa9e-d39a4dff1543
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Nascondi elementi app{#hide-app-elements}

Rimuovere dall'app i componenti standard dell'app Livefyre.

Utilizzare i CSS per nascondere gli elementi predefiniti dell'app Livefyre dalla pagina, consentendo di personalizzare l'esperienza utente in base alle proprie esigenze.

Per nascondere gli elementi dall'app, è sufficiente impostare la visualizzazione su Nessuno.

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

