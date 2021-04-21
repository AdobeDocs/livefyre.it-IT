---
description: Crea la struttura della richiesta di pull per ricevere e rispondere alle richieste di accesso al sistema di identità utente.
title: Struttura della richiesta di pull
exl-id: 70203b23-9d7c-4a22-94ba-2a763e200972
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---

# Struttura della richiesta di pull{#pull-request-structure}

Crea la struttura della richiesta di pull per ricevere e rispondere alle richieste di accesso al sistema di identità utente.

Livefyre invia una richiesta Pull all’URL dell’endpoint.

Ad esempio, se l’URL dell’endpoint Pull è:

```
https://example.yoursite.com/some_path/?id={id}
```

la richiesta Livefyre Pull a questo endpoint sarà:

```
https://example.yoursite.com/some_path/?id={id}&lftoken={UserAuthToken}
```

dove `lftoken` è un token web JSON firmato con la tua chiave di rete e **[!UICONTROL {userAuthToken}]** è il token di autenticazione dell’utente generato da Livefyre.

1. Utilizza `lftoken` per convalidare che le richieste al tuo Ping per l&#39;URL di pull inviate da Livefyre e non da un agente dannoso.
1. Per tutte le richieste in arrivo:

   * Verifica che la stringa di query `lftoken` sia presente nella richiesta.
   * Utilizza il metodo `validateLivefyreToken` nelle librerie Livefyre per assicurarti che `lftoken` sia stato firmato con la chiave di rete.

   * Se `lftoken` non è presente o la convalida non riesce, non consentire all&#39;endpoint di rispondere con le informazioni sul profilo. Al contrario, rispondi con un codice di stato 403 (proibito) e nessun corpo di risposta.

1. `userAuthToken` viene generato dal  `buildUserAuthToken` metodo Livefyre per l’utente, con l’ID utente &quot;system&quot;. Questo utente è il primo utente creato per ogni nuova rete.
