---
description: L'oggetto AuthDelegate implementa il comportamento desiderato per eseguire azioni ed eventi di autenticazione in modo da personalizzare l'integrazione con il sistema di autenticazione esistente del sito.
seo-description: L'oggetto AuthDelegate implementa il comportamento desiderato per eseguire azioni ed eventi di autenticazione in modo da personalizzare l'integrazione con il sistema di autenticazione esistente del sito.
seo-title: Oggetto AuthDelegate
solution: Experience Manager
title: Oggetto AuthDelegate
uuid: a6acc4ef-d442-4782-9bfa-bbe494547c2e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Oggetto AuthDelegate{#authdelegate-object}

L'oggetto AuthDelegate implementa il comportamento desiderato per eseguire azioni ed eventi di autenticazione in modo da personalizzare l'integrazione con il sistema di autenticazione esistente del sito.

## Creazione di un delegato di autenticazione {#section_wmn_tv2_gz}

Per poter eseguire un'azione, il pacchetto di autenticazione deve essere fornito con un delegato di autenticazione. Un delegato di autenticazione è qualsiasi oggetto JavaScript che implementa uno dei metodi in questo argomento.

## .login(FinishLogin) {#section_mpk_lv2_gz}

Accedete a un utente valido e richiamate la funzione FinishLogin con un oggetto Error in caso di errore o con le credenziali Livefyre dell'utente. Implementazioni comuni di questo metodo reindirizzano l’utente a una pagina di login o aprono una nuova finestra o modale.

Questo esempio notifica automaticamente l’autenticazione di un utente Livefyre con il token di autenticazione, il token:

```
authDelegate.login = function (finishLogin) { 
 finishLogin(null, { 
   livefyre: 'token' 
 }); 
};
```

Il delegato di accesso più semplice potrebbe richiedere all'utente finale il token di autenticazione Livefyre.

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

## .logout(FinishLogout) {#section_uqz_2v2_gz}

Disconnettete un utente e richiamate la funzione FinishLogout con un oggetto Error in caso di errore o con un valore null per notificare all'autenticazione l'esito del logout.

Ad esempio:

```
authDelegate.logout = function (finishLogout) { 
 clearUserSession(); //logic to clear a user session  
 finishLogout(null); 
}
```

## .viewProfile(utente) {#section_kkv_dv2_gz}

Per visualizzare il profilo di un utente, effettuate le operazioni necessarie.

```
authDelegate.viewProfile = function (user) { 
 window.open(user.get('profileUrl')); 
}
```

## .editProfile(utente) {#section_bkx_pq2_gz}

Intervenite per modificare il profilo di un utente.

```
authDelegate.editProfile = function (user) { 
 window.open(user.get('profileUrl') + '/edit/'); 
}
```

Implementando tutti i metodi elencati sopra, l'autenticazione può essere configurata con un delegato di autenticazione personalizzato. Una volta costruito, un delegato può essere fornito per l'autenticazione tramite il metodo delegate.

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

