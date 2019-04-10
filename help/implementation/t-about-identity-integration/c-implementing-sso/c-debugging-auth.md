---
description: Potete registrare un utente tramite la console durante l'integrazione
  e il test per l'autorizzazione di debug.
seo-description: Potete registrare un utente tramite la console durante l'integrazione
  e il test per l'autorizzazione di debug.
seo-title: Debug di auth Delegate
solution: Experience Manager
title: Debug di auth Delegate
uuid: fb 0 c 7396-190 e -4 dc 9-bf 26-23 dde 9 efd 45 d
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Debug di auth Delegate{#debugging-auth-delegate}

Potete registrare un utente tramite la console durante l'integrazione e il test per l'autorizzazione di debug.

Inserite un utente nella console utilizzando il seguente `auth.authenticate` token (token) e passate un token utente Livefyre per l'autenticazione degli utenti sulla pagina.

Potete anche modificare l'esempio illustrato qui sopra e aggiungere il seguente snippet in linea nel codice javascript per registrare rapidamente un utente in Livefyre (richiede un riferimento a autenticazione).

```
window.addEventListener('userAuthenticated', function(data) { 
 Livefyre.require(['auth'], function (auth) { 
  auth.authenticate({livefyre: data.token}); 
 }); 
});
```

