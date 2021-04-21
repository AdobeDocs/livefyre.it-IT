---
description: Restituisce un token autenticato dall'utente crittografato per la rete da cui viene richiamato.
title: Metodo di rete buildUserAuthToken
exl-id: dcc61c4b-90d9-42a0-9f46-73a843a4ad78
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 5%

---

# buildUserAuthToken Network Method{#builduserauthtoken-network-method}

Restituisce un token autenticato dall&#39;utente crittografato per la rete da cui viene richiamato.

| Variabile | Tipo | Descrizione |
|--- |--- |--- |
| userId | Stringa | ID utente dell&#39;utente a cui appartiene il token. |
| displayName | Stringa | Nome visualizzato dell&#39;utente. |
| scadenza | Doppio | Quando il token deve scadere in secondi. |

## Esempio Java {#section_nyl_ycs_rz}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

Output campione:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## Esempio NodeJS {#section_xkd_gds_rz}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

Output campione:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## Esempio PHP {#section_ghf_gds_rz}

```
$network->buildUserAuthToken(userId, displayName, expires); 
```

Output campione:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## Esempio di pitone {#section_dwg_gds_rz}

```
network.build_user_auth_token(userId, displayName, expires) 
```

Output campione:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## Esempio di ruby {#section_enh_gds_rz}

```
network.build_user_auth_token(userId, displayName, expires) 
```

Output campione:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```
