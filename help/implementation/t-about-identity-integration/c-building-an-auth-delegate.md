---
description: L'oggetto authdelegate implementa il comportamento desiderato per l'esecuzione
  di azioni ed eventi di autenticazione in modo da personalizzare l'integrazione con
  il sistema di autenticazione esistente del sito.
seo-description: L'oggetto authdelegate implementa il comportamento desiderato per
  l'esecuzione di azioni ed eventi di autenticazione in modo da personalizzare l'integrazione
  con il sistema di autenticazione esistente del sito.
seo-title: Authdelegate Object
solution: Experience Manager
title: Authdelegate Object
uuid: a 6 acc 4 ef-d 442-4782-9 bfa-bbe 494547 c 2 e
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Authdelegate Object{#authdelegate-object}

L'oggetto authdelegate implementa il comportamento desiderato per l'esecuzione di azioni ed eventi di autenticazione in modo da personalizzare l'integrazione con il sistema di autenticazione esistente del sito.

## Creazione di un delegato Auth {#section_wmn_tv2_gz}

Il pacchetto di autenticazione deve essere fornito con un delegato di autenticazione prima di poter eseguire un'azione. Un delegato auth è un qualsiasi oggetto javascript che implementa uno dei metodi in questo argomento.

## . login (finishlogin) {#section_mpk_lv2_gz}

Eseguite il login a un utente valido e richiamate la funzione finishlogin con un oggetto Error in caso di errore o le credenziali di Livefyre dell'utente. Implementazioni comuni di questo metodo reindirizzano l'utente a una pagina di login o aprono una nuova finestra o modale.

Questo esempio notifica automaticamente l'autenticazione di un utente Livefyre con il token di autenticazione, token:

```
authDelegate.login = function (finishLogin) { 
 finishLogin(null, { 
   livefyre: 'token' 
 }); 
};
```

Il delegato di accesso più semplice può chiedere all'utente finale il token di autenticazione Livefyre.

```
authDelegate.login = function contrivedLogin(finishLogin) { 
  var lfToken = prompt("Please type your Livefyre Token");  
  if (lfToken.length === 0) { 
   return finishLogin(new Error("User failed to type their lftoken")); 
  }  
 finishLogin(null, { 
   livefyre: lfToken 
 }); 
};
```

## . logout (finishlogout) {#section_uqz_2v2_gz}

Disconnettete un utente e richiamate la funzione finishlogout con un oggetto Error in caso di errore, o null per notificare all'autenticazione che il logout è stato eseguito correttamente.

Ad esempio:

```
authDelegate.logout = function (finishLogout) { 
 clearUserSession(); //logic to clear a user session  
 finishLogout(null); 
}
```

## . Viewprofile (user) {#section_kkv_dv2_gz}

Esegui l'azione per visualizzare il profilo di un utente.

```
authDelegate.viewProfile = function (user) { 
 window.open(user.get('profileUrl')); 
}
```

## . Editprofile (user) {#section_bkx_pq2_gz}

Intraprendere azioni per modificare il profilo di un utente.

```
authDelegate.editProfile = function (user) { 
 window.open(user.get('profileUrl') + '/edit/'); 
}
```

Implementando tutti i metodi elencati qui sopra, l'autenticazione può essere configurata con un delegato personalizzato. Una volta creato un delegato, questo può essere fornito a autenticazione utilizzando il metodo delegate.

```
var authDelegate = { 
 login: function(cb) { 
  ... 
  cb(null); 
 }, 
 ... 
} 
  
auth.delegate(authDelegate);
```

