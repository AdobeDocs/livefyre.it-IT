---
description: Restituisce un oggetto Collection istanziato come tipo Reviews. Eseguire create_or_update() dall'oggetto Collection per completare il processo di compilazione.
seo-description: Restituisce un oggetto Collection istanziato come tipo Reviews. Eseguire create_or_update() dall'oggetto Collection per completare il processo di compilazione.
seo-title: Metodo del sito buildReviewsCollection
solution: Experience Manager
title: Metodo del sito buildReviewsCollection
uuid: 88af4c68-57de-4ae9-9394-550c94ede48f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Metodo del sito buildReviewsCollection{#buildreviewscollection-site-method}

Restituisce un oggetto Collection istanziato come tipo Reviews. Eseguire create_or_update() dall'oggetto Collection per completare il processo di compilazione.

| Variabile | Tipo | Descrizione |
|--- |--- |--- |
| title | Stringa | Titolo della raccolta. |
| articleId | Stringa | Un ID articolo univoco scelto per identificare una raccolta all'interno del sito. |
| url | Stringa | L'URL assoluto canonico per questa raccolta. |


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

## Esempio di Python {#section_dwg_gds_rz}

```
collection = site.build_reviews_collection(title, articleId, url) 
```

## Esempio di ruby {#section_enh_gds_rz}

```
collection = site.build_reviews_collection(title, articleId, url) 
```

