---
description: Crea la struttura delle richieste pull per ricevere e rispondere alle richieste di accesso al sistema di identità dell’utente.
seo-description: Crea la struttura delle richieste pull per ricevere e rispondere alle richieste di accesso al sistema di identità dell’utente.
seo-title: Struttura richiesta pull
solution: Experience Manager
title: Struttura richiesta pull
uuid: bf6b9e45-d08a-48e6-acc6-e4fa56428d25
translation-type: tm+mt
source-git-commit: cf447db2cb3498fcb01b511848faeee4d1e48481
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---


# Struttura richiesta pull{#pull-request-structure}

Crea la struttura delle richieste pull per ricevere e rispondere alle richieste di accesso al sistema di identità dell’utente.

Livefyre invia una richiesta pull all’URL dell’endpoint.

Ad esempio, se l’URL dell’endpoint pull è:

```
https://example.yoursite.com/some_path/?id={id}
```

la richiesta Livefyre Pull per questo endpoint sarà:

```
https://example.yoursite.com/some_path/?id={id}&lftoken={UserAuthToken}
```

dove `lftoken` è un token Web JSON firmato con la chiave di rete e **[!UICONTROL {userAuthToken}]** è il token di autenticazione utente generato da Livefyre.

1. Utilizzate `lftoken` per convalidare che le richieste al vostro Ping per URL pull siano state inviate da Livefyre e non da un agente dannoso.
1. Per tutte le richieste in arrivo:

   * Verificate che la stringa di query `lftoken` sia presente nella richiesta.
   * Utilizzate il metodo `validateLivefyreToken` nelle librerie Livefyre per verificare che `lftoken` sia stato firmato con la chiave di rete.

   * Se `lftoken` non è presente o la convalida non riesce, non consentire all&#39;endpoint di rispondere con le informazioni sul profilo. Al contrario, rispondete con un codice di stato 403 (proibito) e nessun corpo di risposta.

1. `userAuthToken` viene generato dal  `buildUserAuthToken` metodo Livefyre per l’utente, con l’ID utente &quot;system&quot;. Questo utente è il primo creato per ogni nuova rete.
