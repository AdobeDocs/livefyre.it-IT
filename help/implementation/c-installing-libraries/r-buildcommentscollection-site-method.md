---
description: Restituisce un oggetto Collection istanziato come tipo Comments. Eseguire createOrUpdate() dall'oggetto Collection per completare il processo di compilazione.
seo-description: Restituisce un oggetto Collection istanziato come tipo Comments. Eseguire createOrUpdate() dall'oggetto Collection per completare il processo di compilazione.
seo-title: Metodo del sito buildCommentsCollection
solution: Experience Manager
title: Metodo del sito buildCommentsCollection
uuid: 0e5c062e-960d-4ab0-ba32-0965731a1571
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 7%

---


# Metodo del sito buildCommentsCollection{#buildcommentscollection-site-method}

Restituisce un oggetto Collection istanziato come tipo Comments. Eseguire createOrUpdate() dall&#39;oggetto Collection per completare il processo di compilazione.

| Variabile | Tipo | Descrizione |
|--- |--- |--- |
| title | Stringa | Titolo della raccolta. |
| articleId | Stringa | Un ID articolo univoco scelto per identificare una raccolta all&#39;interno del sito. |
| url | Stringa | L&#39;URL assoluto canonico per questa raccolta. |

## Esempio Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildCommentsCollection(title, articleId, url);
```

## Esempio NodeJS {#section_xkd_gds_rz}

```
var collection = site.buildCommentsCollection(title, articleId, url); 
```

## Esempio PHP {#section_ghf_gds_rz}

```
$collection = site->buildCommentsCollection(title, articleId, url); 
```

## Esempio Python {#section_dwg_gds_rz}

```
collection = site.build_comments_collection(title, articleId, url) 
```

## Esempio di ruby {#section_enh_gds_rz}

```
collection = site.build_comments_collection(title, articleId, url) 
```
