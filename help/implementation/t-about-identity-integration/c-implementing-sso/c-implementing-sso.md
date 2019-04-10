---
description: Per autenticare un utente con Livefyre tramite un flusso non attivato
  da Livefyre App, Livefyre consiglia di implementare il metodo foreachauthentication
  sull'oggetto authdelegate.
seo-description: Per autenticare un utente con Livefyre tramite un flusso non attivato
  da Livefyre App, Livefyre consiglia di implementare il metodo foreachauthentication
  sull'oggetto authdelegate.
seo-title: Implementazione SSO
solution: Experience Manager
title: Implementazione SSO
uuid: c 96 d 456 c-b 1 ac -40 e 0-8 d 18-224652 b 9697 f
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Implementazione SSO{#implementing-sso}

Per autenticare un utente con Livefyre tramite un flusso non attivato da Livefyre App, Livefyre consiglia di implementare il metodo foreachauthentication sull'oggetto authdelegate.

This will be invoked when the `authDelegate` is pass to `auth.delegate`, and will be passed an authenticate function that can be passed multiple. Questo metodo fornisce un'inversion of control per gli eventi di autenticazione in modo che sia `AuthDelegateobject` indipendente senza richiedere un riferimento globale all'autenticazione.

```
authDelegate.forEachAuthentication = function (authenticate) { 
 window.addEventListener('userAuthenticated', function(data) { 
  authenticate({livefyre: data.token}); 
 }); 
}
```

Livefyre si avvale dei token utente per l'autenticazione. Di conseguenza, questo token deve essere restituito dal servizio identità per autenticare un utente con Livefyre. Per informazioni su come creare un token utente Livefyre, consultate Creazione di un token di autenticazione utente.

>[!NOTE]
>
>Dopo l'accesso, l'autenticazione crea una sessione per l'utente e tenterà di caricare una sessione dell'utente dopo l'aggiornamento e il ricaricamento della pagina. `auth.logout()` cancella questa sessione. Ciò significa che non è necessario gestire la sessione di un utente indipendentemente dall'autorizzazione.
