---
description: È possibile accedere a un utente dalla console durante l'integrazione e il test per eseguire il debug dell'autorizzazione.
seo-description: È possibile accedere a un utente dalla console durante l'integrazione e il test per eseguire il debug dell'autorizzazione.
seo-title: Debug delegato autenticazione
solution: Experience Manager
title: Debug delegato autenticazione
uuid: fb0c7396-190e-4dc9-bf26-23dde9efd45d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Debug delegato autenticazione{#debugging-auth-delegate}

È possibile accedere a un utente dalla console durante l'integrazione e il test per eseguire il debug dell'autorizzazione.

Accedete a un utente tramite la console utilizzando il seguente `auth.authenticate` (token) e passate un token utente Livefyre per autenticare gli utenti sulla pagina.

Potete anche modificare l'esempio riportato sopra e aggiungere il seguente snippet in linea nel codice JavaScript per registrare rapidamente un utente in Livefyre (richiede un riferimento ad auth).

```
window.addEventListener('userAuthenticated', function(data) { 
 Livefyre.require(['auth'], function (auth) { 
  auth.authenticate({livefyre: data.token}); 
 }); 
});
```

