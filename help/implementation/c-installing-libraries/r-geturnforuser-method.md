---
description: Questo metodo restituisce l'URN per l'utente di questa rete.
seo-description: Questo metodo restituisce l'URN per l'utente di questa rete.
seo-title: Geturnforuser Network Method
solution: Experience Manager
title: Geturnforuser Network Method
uuid: b 70 b 8 b 0 f -2 b 3 a -4 a 1 d -90 d 0-93 a 97 a 137 ad 4
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Geturnforuser Network Method{#geturnforuser-network-method}

Questo metodo restituisce l&#39;URN per l&#39;utente di questa rete.

| Variabile | Tipo | Descrizione |
|--- |--- |--- |
| Userid | Stringa | Userid da utilizzare nell&#39;URN. |

## Esempio Java {#section_nyl_ycs_rz}

```
network.getUrnForUser(userId);
```

Output di esempio:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Esempio nodejs {#section_xkd_gds_rz}

```
network.getUrnForUser(userId);
```

Output di esempio:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## PHP Example {#section_ghf_gds_rz}

```
$network->getUrnForUser(userId); 
```

Output di esempio:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Esempio Python {#section_dwg_gds_rz}

```
network.get_urn_for_user(userId) 
```

Output di esempio:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Esempio Ruby {#section_enh_gds_rz}

```
network.get_urn_for_user(userId) 
```

Output di esempio:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```
