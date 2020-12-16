---
description: nulle
seo-description: nulle
seo-title: Metodo del sito buildCollection
solution: Experience Manager
title: Metodo del sito buildCollection
uuid: 52abc42a-9506-4492-b219-f2e05eb79c5f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 17%

---


# Metodo del sito buildCollection{#buildcollection-site-method}

| Variabile | Tipo | Descrizione |
|--- |--- |--- |
| type | CollectionType | Il tipo di raccolta. |
| title | Stringa | Titolo della raccolta. |
| articleId | Stringa | Un ID articolo univoco scelto per identificare una raccolta all&#39;interno del sito. |
| url | Stringa | L&#39;URL assoluto canonico per questa raccolta. |

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

## Esempio Python {#section_dwg_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```

## Esempio di ruby {#section_enh_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```
