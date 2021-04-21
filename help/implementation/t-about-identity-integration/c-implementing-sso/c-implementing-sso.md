---
description: Per autenticare un utente con Livefyre attraverso un flusso non attivato da un'app Livefyre, Livefyre consiglia di implementare il metodo foreachAuthentication sull'oggetto AuthDelegate .
title: Implementazione SSO
exl-id: 9af75b8a-9d2a-446e-8cce-2de8645038f2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# Implementazione di SSO{#implementing-sso}

Per autenticare un utente con Livefyre attraverso un flusso non attivato da un&#39;app Livefyre, Livefyre consiglia di implementare il metodo foreachAuthentication sull&#39;oggetto AuthDelegate .

Questo verrà richiamato quando `authDelegate` viene passato a `auth.delegate` e verrà passata una funzione di autenticazione che può essere passata più volte. Questo metodo fornisce un&#39;inversione di controllo per gli eventi di autenticazione in modo che il tuo `AuthDelegateobject` possa essere autonomo senza richiedere un riferimento globale ad auth.

```
authDelegate.forEachAuthentication = function (authenticate) { 
 window.addEventListener('userAuthenticated', function(data) { 
  authenticate({livefyre: data.token}); 
 }); 
}
```

Livefyre si basa sui token utente per coordinare l’autenticazione. Di conseguenza, questo token deve essere restituito dal servizio di identità per autenticare un utente con Livefyre. Per informazioni su come creare un token utente Livefyre, consulta Creazione di un token di autenticazione utente.

>[!NOTE]
>
>Dopo l’accesso, auth creerà una sessione per l’utente e cercherà di caricare la sessione di un utente all’aggiornamento della pagina e al ricaricamento. `auth.logout()` cancella questa sessione. Ciò significa che non è necessario gestire la sessione di un utente indipendentemente dall’autorizzazione.
