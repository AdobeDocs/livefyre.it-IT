---
description: Restituisce un token autenticato utente crittografato per la rete da cui viene invocato.
seo-description: Restituisce un token autenticato utente crittografato per la rete da cui viene invocato.
seo-title: Metodo di rete builduserauthtoken
solution: Experience Manager
title: Metodo di rete builduserauthtoken
uuid: 8828 d 356-c 3 c 6-46 a 6-91 bf -83 bd 59 e 35050
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Metodo di rete builduserauthtoken{#builduserauthtoken-network-method}

Restituisce un token autenticato utente crittografato per la rete da cui viene invocato.

| Variabile | Tipo | Descrizione |
|--- |--- |--- |
| Userid | Stringa | L&#39;ID utente per l&#39;utente a cui appartiene il token. |
| Displayname | Stringa | Nome visualizzato per l&#39;utente. |
| expires | Due volte | Quando il token scade in secondi. |

## Esempio Java {#section_nyl_ycs_rz}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

Output di esempio:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## Esempio nodejs {#section_xkd_gds_rz}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

Output di esempio:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## PHP Example {#section_ghf_gds_rz}

```
$network->buildUserAuthToken(userId, displayName, expires); 
```

Output di esempio:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## Esempio Python {#section_dwg_gds_rz}

```
network.build_user_auth_token(userId, displayName, expires) 
```

Output di esempio:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## Esempio Ruby {#section_enh_gds_rz}

```
network.build_user_auth_token(userId, displayName, expires) 
```

Output di esempio:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```
