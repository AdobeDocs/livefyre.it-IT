---
description: Questa sezione descrive come generare l’oggetto JSON UserAuth che crea il token di autenticazione utente necessario per accedere agli utenti nelle app.
title: Token di autenticazione utente
exl-id: 564144dd-6db4-447b-80ac-b743ecac833d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 2%

---

# Token di autenticazione utente{#user-auth-token}

Questa sezione descrive come generare l’oggetto JSON UserAuth che crea il token di autenticazione utente necessario per accedere agli utenti nelle app.

Questa sezione descrive come generare l’oggetto JSON UserAuth che crea il token di autenticazione utente necessario per accedere agli utenti nelle app.

Per creare il token, utilizza la libreria di lingue preferita per trasmettere i seguenti parametri:

| Parametro | Tipo | Descrizione |
|---|---|---|
| networkName | Stringa *obbligatoria* | Nome della rete Livefyre (fornito da Livefyre). |
| networkKey | Stringa *obbligatoria* | La chiave segreta per questa rete specifica (fornita da Livefyre). |
| userId | Stringa *obbligatoria* | L’ID dell’utente che effettua l’accesso come memorizzato nel sistema di gestione utenti (sono consentiti solo caratteri alfanumerici, trattini, caratteri di sottolineatura e punti): [a-zA-Z0-9_-.]). **Nota:** l&#39;ID utente deve essere univoco. |
| scadenza | Intero *obbligatorio* | Quando il token deve scadere da ora (in secondi). **Nota:** questo valore può anche essere passato come mobile. Il token web JSON prodotto memorizzerà questo valore in tempo epoca UNIX. |
| displayName | Stringa *obbligatoria* | Testo per identificare questo utente nell’interfaccia utente e nei commenti. (Numero massimo di caratteri: 50) |

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
>Le chiavi di rete non sono condivise per gli account demo di Livefyre. Riceverai una chiave di rete una volta effettuato il provisioning di un ambiente da parte di Livefyre. Questa chiave dovrebbe essere mantenuta privata.
