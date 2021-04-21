---
description: Livefyre.require fornisce un plug-in che consente ad auth di ascoltare il bus Janrain Backplane.
title: Collegamento di Janrain a Livefyre tramite AuthDelegate
exl-id: d0fe0e88-5827-478b-b2ef-03f06fb3902c
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---

# Connessione di Janrain a Livefyre tramite AuthDelegate{#connecting-janrain-to-livefyre-using-authdelegate}

Livefyre.require fornisce un plug-in che consente ad auth di ascoltare il bus Janrain Backplane.

Quando un messaggio di identità/accesso viene trasmesso sul canale Backplane, auth.authenticate() verrà chiamato con il token di autenticazione Livefyre dell’utente. Devi ancora implementare un AuthDelegate.

```
Livefyre.require(['auth', 'backplane-auth-plugin#0'], function(auth, backplanePluginFactory) { 
   auth.plugin(backplanePluginFactory('network.fyre.co')); 
   auth.delegate({ 
      login: function (finishLogin) { 
         loginWithCapture(finishLogin); 
      } 
   }); 
});
```

>[!NOTE]
>
>L&#39;oggetto window.Backplane deve essere definito sulla pagina prima di richiamare auth.plugin con il plug-in Backplane Livefyre. Per assicurarti che l&#39;oggetto Backplane sia disponibile, chiama il codice di creazione dell&#39;istanza Livefyre da un callback onReady . Consultare il contatto Janrain per determinare quando altre applicazioni possono utilizzare l&#39;oggetto Backplane.

Di seguito sono riportati alcuni esempi di come un delegato di autenticazione può cercare un&#39;integrazione di Janrain Capture.

>[!NOTE]
>
>Il tuo delegato di autenticazione varierà a seconda della tua istanza Janrain.

<!--Hannah: Mystery stray bullet found here. Please check against source. -Bob -->

* Il callback passato al metodo di login del tuo delegato di autenticazione
* Il riferimento alla variabile di acquisizione Janrain.
* : Riferimento all&#39;oggetto Backplane.

```
/** 
* Login function 
* In this case, opens a login modal and triggers Backplane to start listening 
* for login messages 
*/ 
authDelegate.login = function(finishLogin) { 
   var successCallback = function() { 
      // These need to be replaced with the actions that correspond to successful login  
      // and when the Janrain modal is closed. 
      janrain.events.onCaptureLoginSuccess.removeHandler(successCallback); 
      janrain.events.onModalClose.removeHandler(failureCallback); 
      finishLogin(); 
   }; 
  
   var failureCallback = function(e) { 
      janrain.events.onModalClose.removeHandler(failureCallback); 
      janrain.events.onCaptureLoginSuccess.removeHandler(successCallback); 
      finishLogin(e || new Error("Error logging in with Janrain Capture")); 
   }; 
  
   // Open the modal to log a user in 
   janrain.capture.ui.renderScreen('signIn'); 
   // Send a backplane message 
   window.Backplane.expectMessages('identity/login'); 
   // Add handlers to specific janrain events 
   janrain.events.onCaptureLoginSuccess.addHandler(successCallback); 
   janrain.events.onModalClose.addHandler(failureCallback); 
};
```

Logout

* **finishLogout:** il callback passato al metodo di accesso dell’autore delegato.

* **window.Backplane:** riferimento all&#39;oggetto Backplane.

```
/** 
* Logout function 
* In this case, invalidates the session and removes the cookie. 
* Also reloads the page to change state. In order to do this without a reload, 
* it would be necessary to also update the UI. 
*/ 
authDelegate.logout = function(finishLogout) { 
   Backplane.resetCookieChannel(); 
   janrain.capture.ui.endCaptureSession(); 
   finishLogout(); 
}; 
```

Modifica profilo

Questo può essere collegato a qualsiasi parte del sito che desideri che gli utenti visitano per visualizzare la propria pagina del profilo. In questo esempio viene semplicemente stampato l&#39;oggetto autore passato.

```
/** 
* Edit profile function 
* @param user - User who would like to edit their profile 
*/ 
authDelegate.editProfile = function(user) { 
   console.log(user); 
}; 
```

Visualizza profilo

Come Modifica profilo, questo deve essere collegato a una pagina di un utente diversa dall’utente attualmente connesso. Questo può essere implementato come lo ritieni opportuno. In questo esempio il parametro autore viene semplicemente registrato nella console.

```
/** 
* View profile function 
* @param user - User or userId whose profile should be displayed 
*/ 
authDelegate.viewProfile = function(user) { 
   console.log(author); 
};
```
