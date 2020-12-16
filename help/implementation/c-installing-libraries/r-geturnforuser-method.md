---
description: Questo metodo restituisce l’URL per l’utente della rete.
seo-description: Questo metodo restituisce l’URL per l’utente della rete.
seo-title: getUrnForUser, metodo di rete
solution: Experience Manager
title: getUrnForUser, metodo di rete
uuid: b70b8b0f-2b3a-4a1d-90d0-93a97a137ad4
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 5%

---


# getUrnForUser Network Method{#geturnforuser-network-method}

Questo metodo restituisce l’URL per l’utente della rete.

| Variabile | Tipo | Descrizione |
|--- |--- |--- |
| userId | Stringa | L’ID utente da utilizzare nell’URL. |

## Esempio Java {#section_nyl_ycs_rz}

```
network.getUrnForUser(userId);
```

Output campione:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Esempio NodeJS {#section_xkd_gds_rz}

```
network.getUrnForUser(userId);
```

Output campione:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Esempio PHP {#section_ghf_gds_rz}

```
$network->getUrnForUser(userId); 
```

Output campione:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Esempio Python {#section_dwg_gds_rz}

```
network.get_urn_for_user(userId) 
```

Output campione:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Esempio di ruby {#section_enh_gds_rz}

```
network.get_urn_for_user(userId) 
```

Output campione:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```
