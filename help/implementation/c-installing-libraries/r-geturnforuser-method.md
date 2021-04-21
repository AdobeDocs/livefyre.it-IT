---
description: Questo metodo restituisce l'URN per l'utente della rete.
title: getUrnForUser, metodo di rete
exl-id: 272e724e-d09d-4d7d-9967-a229707ff47f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 7%

---

# getUrnForUser Network Method{#geturnforuser-network-method}

Questo metodo restituisce l&#39;URN per l&#39;utente della rete.

| Variabile | Tipo | Descrizione |
|--- |--- |--- |
| userId | Stringa | ID utente da utilizzare nell&#39;URL. |

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

## Esempio di pitone {#section_dwg_gds_rz}

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
