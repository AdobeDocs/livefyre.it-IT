---
description: Restituisce un oggetto Collection istanziato come tipo Blog. Eseguire create_or_update() dall'oggetto Collection per completare il processo di compilazione.
seo-description: Restituisce un oggetto Collection istanziato come tipo Blog. Eseguire create_or_update() dall'oggetto Collection per completare il processo di compilazione.
seo-title: Metodo del sito buildBlogCollection
solution: Experience Manager
title: Metodo del sito buildBlogCollection
uuid: 6a5ec6b9-bc32-467a-abe6-a57c6defe067
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 6%

---


# Metodo del sito buildBlogCollection{#buildblogcollection-site-method}

Restituisce un oggetto Collection istanziato come tipo Blog. Eseguire create_or_update() dall&#39;oggetto Collection per completare il processo di compilazione.

| Variabile | Tipo | Descrizione |
|--- |--- |--- |
| title | Stringa | Titolo della raccolta. |
| articleId | Stringa | Un ID articolo univoco scelto per identificare una raccolta all&#39;interno del sito. |
| url | Stringa | L&#39;URL assoluto canonico per questa raccolta. |

## Esempio Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildBlogCollection(title, articleId, url); 
```

## Esempio NodeJS {#section_xkd_gds_rz}

```
var collection = site.buildBlogCollection(title, articleId, url); 
```

## Esempio PHP {#section_ghf_gds_rz}

```
$collection = site->buildBlogCollection(title, articleId, url); 
```

## Esempio Python {#section_dwg_gds_rz}

```
collection = site.build_blog_collection(title, articleId, url) 
```

## Esempio di ruby {#section_enh_gds_rz}

```
collection = site.build_blog_collection(title, articleId, url) 
```

