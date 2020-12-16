---
description: Imposta SSL per attivare o disattivare le chiamate API.
seo-description: Imposta SSL per attivare o disattivare le chiamate API.
seo-title: setSSL, metodo di rete
solution: Experience Manager
title: setSSL, metodo di rete
uuid: 8d989e63-c859-456a-99ca-8d87933913ba
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 7%

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

## Esempio Python {#section_dwg_gds_rz}

```
network.ssl = False 
```

## Esempio di ruby {#section_enh_gds_rz}

```
network.ssl = false 
```
