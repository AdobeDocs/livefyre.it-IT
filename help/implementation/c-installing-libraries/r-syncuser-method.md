---
description: Informa Livefyre a richiamare informazioni utente da un URL di sincronizzazione utente precedentemente impostato. Restituisce un valore Boolean.
title: Metodo di rete syncUser
exl-id: a21ff487-2ab1-4788-b455-84941f03a98f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 4%

---

# syncUser Network Method{#syncuser-network-method}

Informa Livefyre a richiamare informazioni utente da un URL di sincronizzazione utente precedentemente impostato. Restituisce un valore Boolean.

| Variabile | Tipo | Descrizione |
|--- |--- |--- |
| userId | Stringa | ID utente da sincronizzare con Livefyre. Prima di chiamare questo metodo, è necessario disporre di un URL di sincronizzazione utente impostato con Livefyre. |

## Esempio Java {#section_nyl_ycs_rz}

```
network.syncUser(userId); 
```

Output campione:

```
true
```

## Esempio NodeJS {#section_xkd_gds_rz}

```
network.syncUser(userId); 
```

Output campione:

```
true
```

## Esempio PHP {#section_ghf_gds_rz}

```
$network->syncUser(userId); 
```

Output campione:

```
true
```

## Esempio di pitone {#section_dwg_gds_rz}

```
network.sync_user(userId) 
```

Output campione:

```
True
```

## Esempio di ruby {#section_enh_gds_rz}

```
network.sync_user(userId) 
```

Output campione:

```
True
```
