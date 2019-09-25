---
description: Crea la struttura delle richieste pull per ricevere e rispondere alle richieste di accesso al tuo sistema di identità utente.
seo-description: Crea la struttura delle richieste pull per ricevere e rispondere alle richieste di accesso al tuo sistema di identità utente.
seo-title: Struttura richiesta pull
solution: Experience Manager
title: Struttura richiesta pull
uuid: bf6b9e45-d08a-48e6-acc6-e4fa56428d25
translation-type: tm+mt
source-git-commit: cf447db2cb3498fcb01b511848faeee4d1e48481

---


# Struttura richiesta pull{#pull-request-structure}

Crea la struttura delle richieste pull per ricevere e rispondere alle richieste di accesso al tuo sistema di identità utente.

Livefyre invia una richiesta pull all’URL dell’endpoint.

Ad esempio, se l’URL dell’endpoint pull è:

```
https://example.yoursite.com/some_path/?id={id}
```

la richiesta Livefyre pull a questo endpoint sarà:

```
https://example.yoursite.com/some_path/?id={id}&lftoken={UserAuthToken}
```

dove `lftoken` è un token Web JSON firmato con la chiave di rete e **[!UICONTROL {userAuthToken}]** è il token autenticazione utente generato da Livefyre.

1. Utilizzate `lftoken` per convalidare che le richieste al vostro Ping per URL pull siano state inviate da Livefyre e non da un agente dannoso.
1. Per tutte le richieste in arrivo:

   * Verificate che la stringa di `lftoken` query sia presente nella richiesta.
   * Utilizzate il `validateLivefyreToken` metodo nelle librerie Livefyre per verificare che sia `lftoken` stato firmato con la chiave di rete.

   * Se la convalida non `lftoken` è presente o non riesce, non consentire all'endpoint di rispondere con le informazioni del profilo. Al contrario, rispondete con un codice di stato 403 (proibito) e nessun corpo di risposta.

1. `userAuthToken` viene generato dal `buildUserAuthToken` metodo Livefyre per l’utente, con l’ID utente "system". Questo utente è il primo creato per ogni nuova rete.
