---
description: Informa Livefyre di estrarre informazioni utente da un URL di sincronizzazione
  utente precedentemente impostato. Restituisce un valore booleano.
seo-description: Informa Livefyre di estrarre informazioni utente da un URL di sincronizzazione
  utente precedentemente impostato. Restituisce un valore booleano.
seo-title: Metodo di rete syncuser
solution: Experience Manager
title: Metodo di rete syncuser
uuid: 2 affb 03 d -3907-4 b 01-9 a 64-02 ba 1 b 06 da 14
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Metodo di rete syncuser{#syncuser-network-method}

Informa Livefyre di estrarre informazioni utente da un URL di sincronizzazione utente precedentemente impostato. Restituisce un valore booleano.

| Variabile | Tipo | Descrizione |
|--- |--- |--- |
| Userid | Stringa | L'ID utente da sincronizzare con Livefyre. Dovete disporre di un URL di sincronizzazione utente con Livefyre prima di richiamare questo metodo. |

## Esempio Java {#section_nyl_ycs_rz}

```
network.syncUser(userId); 
```

Output di esempio:

```
true
```

## Esempio nodejs {#section_xkd_gds_rz}

```
network.syncUser(userId); 
```

Output di esempio:

```
true
```

## PHP Example {#section_ghf_gds_rz}

```
$network->syncUser(userId); 
```

Output di esempio:

```
true
```

## Esempio Python {#section_dwg_gds_rz}

```
network.sync_user(userId) 
```

Output di esempio:

```
True
```

## Esempio Ruby {#section_enh_gds_rz}

```
network.sync_user(userId) 
```

Output di esempio:

```
True
```
