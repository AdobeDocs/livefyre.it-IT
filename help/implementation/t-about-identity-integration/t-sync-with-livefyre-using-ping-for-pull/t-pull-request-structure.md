---
description: Create la struttura di richiesta di pull per ricevere e rispondere alle
  richieste di accesso al sistema di identità dell'utente.
seo-description: Create la struttura di richiesta di pull per ricevere e rispondere
  alle richieste di accesso al sistema di identità dell'utente.
seo-title: Struttura richiesta pull
solution: Experience Manager
title: Struttura richiesta pull
uuid: bf 6 b 9 e 45-d 08 a -48 e 6-acc 6-e 4 fa 56428 d 25
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Struttura richiesta pull{#pull-request-structure}

Create la struttura di richiesta di pull per ricevere e rispondere alle richieste di accesso al sistema di identità dell'utente.

Livefyre emette una richiesta pull all'URL dell'endpoint.

Ad esempio, se l'URL dell'endpoint Pull è:

```
https://example.yoursite.com/some_path/?id={id}
```

la richiesta Livefyre Pull a questo endpoint sarà:

```
https://example.yoursite.com/some_path/?id={id}&lftoken={UserAuthToken}
```

where `lftoken` is a JSON Web Token signed with your network key, and **[!UICONTROL {userAuthToken}]** is the user autentth token generated by Livefyre.

1. Utilizzate `lftoken` per convalidare che le richieste all'URL di Ping per Pull vengano inviate da Livefyre e non da un agente dannoso.
1. Per tutte le richieste in entrata:

   * Verificate che nella richiesta sia `lftoken` presente la stringa query.
   * Utilizzate il `validateLivefyreToken` metodo nelle librerie di Livefyre per verificare `lftoken` che sia stato firmato con la vostra chiave di rete.

   * Se `lftoken` non è presente o non si verifica un errore di convalida, non consentire all'endpoint di rispondere alle informazioni sul profilo. Rispondi, invece, con un codice di stato 403 (Proibito) e senza corpo della risposta.

1. `userAuthToken` è generato dal metodo Livefyre `buildUserAuthToken` per l'utente, con ID utente «system». Questo utente è il primo utente creato per ogni nuova rete.
1. Per testare la pagina, utilizzate [il tester Ping for Pull](https://livefyre-p4p-wizard.herokuapp.com/home) per confermare che tutto funziona come previsto.