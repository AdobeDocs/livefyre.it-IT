---
description: In questa sezione viene descritto come generare l'oggetto JSON UserAuth che crea il token di autenticazione utente richiesto per accedere agli utenti nelle app.
seo-description: In questa sezione viene descritto come generare l'oggetto JSON UserAuth che crea il token di autenticazione utente richiesto per accedere agli utenti nelle app.
seo-title: Token autenticazione utente
solution: Experience Manager
title: Token autenticazione utente
uuid: 6483debd-453c-4780-b19c-1d8041693617
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 1%

---


# Token autenticazione utente{#user-auth-token}

In questa sezione viene descritto come generare l&#39;oggetto JSON UserAuth che crea il token di autenticazione utente richiesto per accedere agli utenti nelle app.

In questa sezione viene descritto come generare l&#39;oggetto JSON UserAuth che crea il token di autenticazione utente richiesto per accedere agli utenti nelle app.

Per creare il token, usate la libreria delle lingue preferita per trasmettere i seguenti parametri:

| Parametro | Tipo | Descrizione |
|---|---|---|
| networkName | Stringa *obbligatoria* | Nome della rete Livefyre (fornito da Livefyre). |
| networkKey | Stringa *obbligatoria* | Chiave segreta per questa specifica rete (fornita da Livefyre). |
| userId | Stringa *obbligatoria* | L’ID dell’utente che accede come memorizzato nel sistema di gestione degli utenti (sono consentiti solo caratteri alfanumerici, trattini, caratteri di sottolineatura e punti): [a-zA-Z0-9_-.]). **Nota:** l&#39;ID utente deve essere univoco. |
| expires | Numero intero *obbligatorio* | Quando il token deve scadere da ora (in secondi). **Nota:** questo valore può anche essere trasmesso come mobile. Il token Web JSON prodotto memorizzerà questo valore in tempo epoch UNIX. |
| displayName | Stringa *obbligatoria* | Testo per identificare l’utente nell’interfaccia utente e nei commenti. (Numero massimo di caratteri: 50) |

## Java {#section_b42_mjz_1cb}

```
network.buildUserAuthToken(userId, displayName, expires); 
 
```

## NodeJS {#section_c42_mjz_1cb}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

## PHP {#section_d42_mjz_1cb}

```
$network->buildUserAuthToken(userId, displayName, expires); 
```

## Python {#section_e42_mjz_1cb}

```
network.build_user_auth_token(userId, displayName, expires) 
```

## Ruby {#section_f42_mjz_1cb}

```
network.build_user_auth_token(userId, displayName, expires) 
```

>[!NOTE]
>
>Le chiavi di rete non sono condivise per gli account demo di Livefyre. Una volta che Livefyre avrà eseguito il provisioning di un ambiente, riceverete una chiave di rete. Questa chiave dovrebbe essere mantenuta privata.

