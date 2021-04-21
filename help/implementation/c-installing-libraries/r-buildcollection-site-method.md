---
title: Metodo Site buildCollection
description: Metodo Site buildCollection
exl-id: d5c9a2fb-2d30-44f4-8ebf-24b0ec7babee
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 15%

---

# metodo del sito buildCollection{#buildcollection-site-method}

| Variabile | Tipo | Descrizione |
|--- |--- |--- |
| type | CollectionType | Tipo di raccolta. |
| title | Stringa | Titolo della raccolta. |
| articleId | Stringa | Un ID articolo univoco scelto per identificare una raccolta all&#39;interno del sito. |
| url | Stringa | URL assoluto canonico per questa raccolta. |

## Esempio Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildCollection(type, title, articleId, url); 
```

## Esempio NodeJS {#section_xkd_gds_rz}

```
var collection = site.buildCollection(type, title, articleId, url); 
```

## Esempio PHP {#section_ghf_gds_rz}

```
$collection = site->buildCollection(type, title, articleId, url); 
```

## Esempio di pitone {#section_dwg_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```

## Esempio di ruby {#section_enh_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```
