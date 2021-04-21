---
description: L'oggetto AuthDelegate implementa il comportamento desiderato per eseguire azioni ed eventi di autenticazione in modo da poter personalizzare l'integrazione con il sistema di autenticazione esistente del sito.
title: Oggetto AuthDelegate
exl-id: 7c669138-627e-476e-a177-c71346f730df
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Oggetto AuthDelegate{#authdelegate-object}

L&#39;oggetto AuthDelegate implementa il comportamento desiderato per eseguire azioni ed eventi di autenticazione in modo da poter personalizzare l&#39;integrazione con il sistema di autenticazione esistente del sito.

## Creazione di un delegato di autenticazione {#section_wmn_tv2_gz}

Il pacchetto di autenticazione deve essere fornito con un delegato di autenticazione prima di poter eseguire un&#39;azione. Un delegato di autenticazione è qualsiasi oggetto JavaScript che implementa uno dei metodi di questo argomento.

## .login(finishLogin) {#section_mpk_lv2_gz}

Accedi a un utente valido e richiama la funzione FinishLogin con un oggetto Error in caso di errore o con le credenziali Livefyre dell’utente. Implementazioni comuni di questo metodo reindirizzano l’utente a una pagina di accesso o aprono una nuova finestra o modale.

Questo esempio notifica automaticamente l’autenticazione di un utente Livefyre con il token di autenticazione, il token:

```
authDelegate.login = function (finishLogin) { 
 finishLogin(null, { 
   livefyre: 'token' 
 }); 
};
```

Il delegato di accesso più semplice potrebbe chiedere all&#39;utente finale il proprio token di autenticazione Livefyre.

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

## .logout(finishLogout) {#section_uqz_2v2_gz}

Disconnetti un utente e richiama la funzione finishLogout con un oggetto Error in caso di errore o con un valore null per notificare all’autorità di autenticazione l’esito del logout.

Ad esempio:

```
authDelegate.logout = function (finishLogout) { 
 clearUserSession(); //logic to clear a user session  
 finishLogout(null); 
}
```

## .viewProfile(user) {#section_kkv_dv2_gz}

Intervieni per visualizzare il profilo di un utente.

```
authDelegate.viewProfile = function (user) { 
 window.open(user.get('profileUrl')); 
}
```

## .editProfile(user) {#section_bkx_pq2_gz}

Intervieni per modificare il profilo di un utente.

```
authDelegate.editProfile = function (user) { 
 window.open(user.get('profileUrl') + '/edit/'); 
}
```

Implementando tutti i metodi elencati sopra, auth può essere configurato con un delegato di autenticazione personalizzato. Una volta costruito un delegato, questo può essere fornito all&#39;autenticazione utilizzando il metodo delegato .

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
