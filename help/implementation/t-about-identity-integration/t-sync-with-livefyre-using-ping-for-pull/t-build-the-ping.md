---
description: Create il ping in modo che la pagina pings Livefyre possa aggiornare
  il proprio profilo.
seo-description: Create il ping in modo che la pagina pings Livefyre possa aggiornare
  il proprio profilo.
seo-title: Creare il ping
solution: Experience Manager
title: Creare il ping
uuid: cb 8 cc 043-9 ea 5-407 c-b 70 f -3 f 1 e 37 accdae
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Creare il ping{#build-the-ping}

Create il ping in modo che la pagina pings Livefyre possa aggiornare il proprio profilo.

Quando Livefyre riceve una notifica di aggiornamento con `networkName` e `user_id`, il sistema invierà una richiesta di pull al PING per l'URL pull.

>[!NOTE]
>
>403/Non autorizzato in risposta al ping indica un'aggiunta non valida `lftoken` alla richiesta di ping. Verificate che sia `lftoken` disponibile per i `user_id` privilegi di proprietario di rete o per l'utente del sistema. Se utilizzate le librerie Livefyre, utilizzate il `buildLivefyreToken` metodo per generare un token di sistema valido per la richiesta.

1. Aggiungete codice alla pagina che esegue il ping di Livefyre quando gli utenti aggiornano il profilo. Create l'URL in questo modo:

```
 POSThttps://{networkName}.quill.fyre.co/api/v3.0/user/{user_id}/refresh?lftoken={token}
```

* **[!UICONTROL networkName:]** Il nome di rete fornito da Livefyre.
* **[!UICONTROL user_id:]** L'ID dell'utente.
* **[!UICONTROL token:]** Token di sistema valido.

1. Estraete la struttura della richiesta.