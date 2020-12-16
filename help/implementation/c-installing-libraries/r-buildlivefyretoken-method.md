---
description: Restituisce un token Livefyre valido crittografato che può essere utilizzato per interagire con altre API Livefyre per la rete da cui viene chiamato.
seo-description: Restituisce un token Livefyre valido crittografato che può essere utilizzato per interagire con altre API Livefyre per la rete da cui viene chiamato.
seo-title: Metodo di rete buildLivefyreToken
solution: Experience Manager
title: Metodo di rete buildLivefyreToken
uuid: 7c72a05f-669b-4df3-8117-aa4af2f7a179
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# Metodo di rete buildLivefyreToken{#buildlivefyretoken-network-method}

Restituisce un token Livefyre valido crittografato che può essere utilizzato per interagire con altre API Livefyre per la rete da cui viene chiamato.

Restituisce un token Livefyre valido crittografato che può essere utilizzato per interagire con altre API Livefyre per la rete da cui viene chiamato.

Per impostazione predefinita, questo token scade dopo 24 ore dalla creazione.

## Esempio Java {#section_nyl_ycs_rz}

```
network.buildLivefyreToken(); 
```

Output campione:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## Esempio NodeJS {#section_xkd_gds_rz}

```
network.buildLivefyreToken(); 
```

Output campione:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## Esempio PHP {#section_ghf_gds_rz}

```
network.buildLivefyreToken(); 
```

Output campione:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## Esempio Python {#section_dwg_gds_rz}

```
network.build_livefyre_token() 
```

Output campione:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## Esempio di ruby {#section_enh_gds_rz}

```
network.build_livefyre_token() 
```

Output campione:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

