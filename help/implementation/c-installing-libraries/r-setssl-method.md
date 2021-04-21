---
description: Imposta SSL per attivare o disattivare le chiamate API.
title: setSSL Network, metodo
exl-id: 5682b84a-0b4d-479b-af40-60d2c6c38155
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 8%

---

# setSSL Network Method{#setssl-network-method}

Imposta SSL per attivare o disattivare le chiamate API.

| Variabile | Tipo | Descrizione |
|--- |--- |--- |
| ssl | Booleano | Il valore predefinito è true. se si desidera che SSL sia attivato, altrimenti è false. <br><ul><li>True - SSL attivato </li><li>False - SSL disattivato</li></ul> |

## Esempio Java {#section_nyl_ycs_rz}

```
network.setSsl(ssl); 
```

## Esempio NodeJS {#section_xkd_gds_rz}

```
network.ssl = false; 
```

## Esempio PHP {#section_ghf_gds_rz}

```
$network->setSsl(false); 
```

## Esempio di pitone {#section_dwg_gds_rz}

```
network.ssl = False 
```

## Esempio di ruby {#section_enh_gds_rz}

```
network.ssl = false 
```
