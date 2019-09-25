---
description: Livefyre.request fornisce un plugin che consente all'auth di ascoltare il bus Janrain Backplane.
seo-description: Livefyre.request fornisce un plugin che consente all'auth di ascoltare il bus Janrain Backplane.
seo-title: Connessione di Janrain a Livefyre tramite AuthDelegate
title: Connessione di Janrain a Livefyre tramite AuthDelegate
uuid: 9d56e3f4-960a-4108-aab5-2795b0e71c88
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Connessione di Janrain a Livefyre tramite AuthDelegate{#connecting-janrain-to-livefyre-using-authdelegate}

Livefyre.request fornisce un plugin che consente all'auth di ascoltare il bus Janrain Backplane.

Quando un messaggio di identità/login viene trasmesso sul canale Backplane, auth.authenticate() verrà chiamato con il token di autenticazione Livefyre dell'utente. Devi ancora implementare un AuthDelegate.

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
>L'oggetto window.Backplane deve essere definito sulla pagina prima di chiamare auth.plugin con il plug-in Livefyre Backplane. Per essere certi che l'oggetto Backplane sia disponibile, chiamate il codice di creazione dell'istanza Livefyre da un callback onReady. Consultate il contatto di Janrain per determinare quando altre applicazioni possono utilizzare l'oggetto Backplane.

Di seguito sono riportati alcuni esempi di come un delegato audio potrebbe cercare un'integrazione di Janrain Capture.

>[!NOTE]
>
>Il delegato di autenticazione varia a seconda dell’istanza di Janrain.

<!--Hannah: Mystery stray bullet found here. Please check against source. -Bob -->

*  Callback passato al metodo di login del delegato di autenticazione
*  Il riferimento alla variabile di acquisizione Janrain.
* : Riferimento all'oggetto Backplane.

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

* **** completionLogout: Il callback passato al metodo di login del delegato dell’autenticazione.

* **** window.Backplane: Riferimento all'oggetto Backplane.

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

Questo può essere collegato a qualsiasi parte del sito che desideri che gli utenti visitino per visualizzare la propria pagina del profilo. In questo esempio viene semplicemente stampato l'oggetto autore passato.

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

Come Edit Profile (Modifica profilo), questo collegamento deve essere collegato a una pagina dell'utente diversa dall'utente attualmente connesso. Questa funzione può essere implementata a seconda delle esigenze. In questo esempio il parametro author viene semplicemente registrato nella console.

```
/** 
* View profile function 
* @param user - User or userId whose profile should be displayed 
*/ 
authDelegate.viewProfile = function(user) { 
   console.log(author); 
};
```

