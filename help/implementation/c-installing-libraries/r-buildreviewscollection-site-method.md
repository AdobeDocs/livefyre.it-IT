---
description: Restituisce un oggetto Collection istanziato come tipo Reviews. Esegui create_or_update() dall'oggetto Collection per completare il processo di compilazione.
title: Metodo Site buildReviewsCollection
exl-id: 581ad24c-d115-4ffb-93eb-936c2da6e3fa
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 8%

---

# Metodo del sito buildReviewsCollection{#buildreviewscollection-site-method}

Restituisce un oggetto Collection istanziato come tipo Reviews. Esegui create_or_update() dall&#39;oggetto Collection per completare il processo di compilazione.

| Variabile | Tipo | Descrizione |
|--- |--- |--- |
| title | Stringa | Titolo della raccolta. |
| articleId | Stringa | Un ID articolo univoco scelto per identificare una raccolta all&#39;interno del sito. |
| url | Stringa | URL assoluto canonico per questa raccolta. |


## Esempio Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildReviewsCollection(title, articleId, url); 
```

## Esempio NodeJS {#section_xkd_gds_rz}

```
var collection = site.buildReviewsCollection(title, articleId, url); 
```

## Esempio PHP {#section_ghf_gds_rz}

```
$collection = site->buildReviewsCollection(title, articleId, url); 
```

## Esempio di pitone {#section_dwg_gds_rz}

```
collection = site.build_reviews_collection(title, articleId, url) 
```

## Esempio di ruby {#section_enh_gds_rz}

```
collection = site.build_reviews_collection(title, articleId, url) 
```
