---
description: Informa Livefyre a richiamare le informazioni utente da un URL di sincronizzazione utente precedentemente impostato. Restituisce un valore Boolean.
seo-description: Informa Livefyre a richiamare le informazioni utente da un URL di sincronizzazione utente precedentemente impostato. Restituisce un valore Boolean.
seo-title: syncUser, metodo di rete
solution: Experience Manager
title: syncUser, metodo di rete
uuid: 2affb03d-3907-4b01-9a64-02ba1b06da14
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 3%

---


# syncUser Network Method{#syncuser-network-method}

Informa Livefyre a richiamare le informazioni utente da un URL di sincronizzazione utente precedentemente impostato. Restituisce un valore Boolean.

| Variabile | Tipo | Descrizione |
|--- |--- |--- |
| userId | Stringa | L&#39;ID utente da sincronizzare con Livefyre. Prima di richiamare questo metodo, dovete disporre di un URL di sincronizzazione utente impostato con Livefyre. |

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

## Esempio Python {#section_dwg_gds_rz}

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
