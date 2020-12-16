---
description: Per autenticare un utente con Livefyre attraverso un flusso non attivato da un'app Livefyre, Livefyre consiglia di implementare il metodo foreachAuthentication sull'oggetto AuthDelegate.
seo-description: Per autenticare un utente con Livefyre attraverso un flusso non attivato da un'app Livefyre, Livefyre consiglia di implementare il metodo foreachAuthentication sull'oggetto AuthDelegate.
seo-title: Implementazione SSO
solution: Experience Manager
title: Implementazione SSO
uuid: c96d456c-b1ac-40e0-8d18-224652b9697f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---


# Implementazione di SSO{#implementing-sso}

Per autenticare un utente con Livefyre attraverso un flusso non attivato da un&#39;app Livefyre, Livefyre consiglia di implementare il metodo foreachAuthentication sull&#39;oggetto AuthDelegate.

Questo verrà richiamato quando `authDelegate` viene passato a `auth.delegate` e verrà passata una funzione di autenticazione che può essere passata più volte. Questo metodo fornisce un&#39;inversione del controllo per gli eventi di autenticazione in modo che il `AuthDelegateobject` possa essere contenuto autonomamente senza richiedere un riferimento globale ad auth.

```
authDelegate.forEachAuthentication = function (authenticate) { 
 window.addEventListener('userAuthenticated', function(data) { 
  authenticate({livefyre: data.token}); 
 }); 
}
```

Livefyre si basa sui token utente per coordinare l&#39;autenticazione. Di conseguenza, questo token deve essere restituito dal servizio di identità per autenticare un utente con Livefyre. Per informazioni su come creare un token utente Livefyre, consultate Creazione di un token di autenticazione utente.

>[!NOTE]
>
>Dopo l’accesso, l’autenticazione creerà una sessione per l’utente e tenterà di caricare la sessione di un utente dopo l’aggiornamento e il ricaricamento della pagina. `auth.logout()` cancella la sessione. Ciò significa che non è necessario gestire una sessione di un utente indipendentemente dall&#39;autorizzazione.

