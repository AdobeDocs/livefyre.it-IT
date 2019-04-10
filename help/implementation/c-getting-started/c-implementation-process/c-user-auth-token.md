---
description: In questa sezione viene descritto come generare l'oggetto JSON userauth
  che crea il token di autenticazione utente richiesto per il registro degli utenti
  nelle app.
seo-description: In questa sezione viene descritto come generare l'oggetto JSON userauth
  che crea il token di autenticazione utente richiesto per il registro degli utenti
  nelle app.
seo-title: Token autenticazione utente
solution: Experience Manager
title: Token autenticazione utente
uuid: 6483 debd -453 c -4780-b 19 c -1 d 8041693617
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Token autenticazione utente{#user-auth-token}

In questa sezione viene descritto come generare l'oggetto JSON userauth che crea il token di autenticazione utente richiesto per il registro degli utenti nelle app.

In questa sezione viene descritto come generare l'oggetto JSON userauth che crea il token di autenticazione utente richiesto per il registro degli utenti nelle app.

Per creare il token, usate la libreria preferita della lingua per passare i seguenti parametri:

| Parametro | Tipo | Descrizione |
|---|---|---|
| Networkname | Stringa *richiesta* | Nome della rete Livefyre (fornito da Livefyre). |
| Networkkey | Stringa *richiesta* | La chiave segreta per questa rete specifica (fornita da Livefyre). |
| Userid | Stringa *richiesta* | L'ID dell'utente che accede come memorizzato nel sistema di gestione degli utenti (sono consentiti solo i caratteri alfanumerici, trattini, di sottolineatura e punti): [a-zA-Z 0-9_-.]). **Nota:** L'ID utente deve essere univoco. |
| expires | Numero intero *richiesto* | Quando il token scade da ora (in secondi). **Nota:** Questo valore può essere trasmesso anche come mobile. Il token Web JSON prodotto memorizzerà questo valore in ora epoch UNIX. |
| Displayname | Stringa *richiesta* | Testo per identificare questo utente nell'interfaccia utente e nei commenti. (Numero massimo di caratteri: 50.) |

## Java {#section_b42_mjz_1cb}

```
network.buildUserAuthToken(userId, displayName, expires); 
 
```

## Nodejs {#section_c42_mjz_1cb}

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
>Le chiavi di rete non vengono condivise per gli account demosite di Livefyre. Riceverete una chiave di rete dopo che Livefyre avrà effettuato il provisioning di un ambiente. Questa chiave deve essere mantenuta privata.

