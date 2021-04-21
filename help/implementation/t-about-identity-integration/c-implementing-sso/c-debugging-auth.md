---
description: È possibile accedere a un utente tramite la console durante l'integrazione e il test per eseguire il debug dell'autorizzazione.
title: Delega autenticazione debug
exl-id: fa1c17fa-5aba-4f4c-9217-5823af30af61
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---

# Delega autenticazione debug{#debugging-auth-delegate}

È possibile accedere a un utente tramite la console durante l&#39;integrazione e il test per eseguire il debug dell&#39;autorizzazione.

Accedi a un utente tramite la console utilizzando il seguente `auth.authenticate` (token) e passa un token utente Livefyre per autenticare gli utenti sulla pagina.

Puoi anche modificare l’esempio mostrato sopra e aggiungere il seguente frammento in linea nel tuo JavaScript per accedere rapidamente un utente a Livefyre (richiede un riferimento ad auth).

```
window.addEventListener('userAuthenticated', function(data) { 
 Livefyre.require(['auth'], function (auth) { 
  auth.authenticate({livefyre: data.token}); 
 }); 
});
```
