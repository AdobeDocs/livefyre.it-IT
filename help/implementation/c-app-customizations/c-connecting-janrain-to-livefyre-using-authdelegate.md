---
description: Livefyre. require fornisce un plug-plugin che consente all'autenticazione di ascoltare l'autobus Janrain Backplane.
seo-description: Livefyre. require fornisce un plug-plugin che consente all'autenticazione di ascoltare l'autobus Janrain Backplane.
seo-title: Connessione di Janrain a Livefyre tramite authdelegate
title: Connessione di Janrain a Livefyre tramite authdelegate
uuid: 9 d 56 e 3 f 4-960 a -4108-aab 5-2795 b 0 e 71 c 88
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Connessione di Janrain a Livefyre tramite authdelegate{#connecting-janrain-to-livefyre-using-authdelegate}

Livefyre. require fornisce un plug-plugin che consente all&#39;autenticazione di ascoltare l&#39;autobus Janrain Backplane.

Quando viene trasmesso un messaggio di identità/login sul canale Backplane, auth. authenticate () verrà chiamato con il token di autenticazione Livefyre dell&#39;utente. Dovete comunque implementare un authdelegate.

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
>L&#39;oggetto window. Backplane deve essere definito sulla pagina prima della chiamata di autenticazione. plugin con il plug-plugin di Livefyre Backplane. Per verificare che l&#39;oggetto Backplane sia disponibile, chiamate il codice di istanza di Livefyre da una callback onready. Rivolgersi al contatto Janrain per determinare quando altre applicazioni possono utilizzare l&#39;oggetto Backplane.

Di seguito sono riportati alcuni esempi di come un delegato di autenticazione potrebbe cercare un&#39;integrazione Janrain Capture.

>[!NOTE]
>
>Il delegato di autenticazione varia a seconda dell&#39;istanza Janrain.

<!--Hannah: Mystery stray bullet found here. Please check against source. -Bob -->

* Callback passato al metodo di login di autenticazione dell&#39;autenticazione
* Riferimento alla variabile di acquisizione Janrain.
* : Un riferimento all&#39;oggetto Backplane.

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

Disconnessione

* **Finishlogout:** Callback passato al metodo di login di autenticazione dell&#39;autenticazione.

* **window. Backplane:** Un riferimento all&#39;oggetto Backplane.

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

Questo collegamento può essere collegato a qualsiasi parte del sito che desiderate venga visitata dagli utenti per visualizzare la propria pagina del profilo. Questo esempio stampa semplicemente l&#39;oggetto di authoring trasmesso.

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

Come Edit Profile (Modifica profilo), questo collegamento deve essere collegato alla pagina di un utente diversa da quella attualmente registrata. Questo può essere implementato in base alle esigenze. Questo esempio collega semplicemente il parametro autore alla console.

```
/** 
* View profile function 
* @param user - User or userId whose profile should be displayed 
*/ 
authDelegate.viewProfile = function(user) { 
   console.log(author); 
};
```

