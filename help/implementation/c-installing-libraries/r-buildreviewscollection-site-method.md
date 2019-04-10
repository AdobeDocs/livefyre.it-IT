---
description: Restituisce un oggetto Collection creata come tipo recensioni. Eseguite
  create_ or_ update () dall'oggetto Collection per completare il processo di creazione.
seo-description: Restituisce un oggetto Collection creata come tipo recensioni. Eseguite
  create_ or_ update () dall'oggetto Collection per completare il processo di creazione.
seo-title: Metodo Sitdreviewscollection Site
solution: Experience Manager
title: Metodo Sitdreviewscollection Site
uuid: 88 af 4 c 68-57 de -4 ae 9-9394-550 c 94 ede 48 f
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Metodo Sitdreviewscollection Site{#buildreviewscollection-site-method}

Restituisce un oggetto Collection creata come tipo recensioni. Eseguite create_ or_ update () dall'oggetto Collection per completare il processo di creazione.

| Variabile | Tipo | Descrizione |
|--- |--- |--- |
| title | Stringa | Titolo della raccolta. |
| Articleid | Stringa | Un ID articolo univoco che avete scelto di identificare una raccolta all'interno del sito. |
| url | Stringa | L'URL assoluto canonico per questa raccolta. |


## Esempio Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildReviewsCollection(title, articleId, url); 
```

## Esempio nodejs {#section_xkd_gds_rz}

```
var collection = site.buildReviewsCollection(title, articleId, url); 
```

## PHP Example {#section_ghf_gds_rz}

```
$collection = site->buildReviewsCollection(title, articleId, url); 
```

## Esempio Python {#section_dwg_gds_rz}

```
collection = site.build_reviews_collection(title, articleId, url) 
```

## Esempio Ruby {#section_enh_gds_rz}

```
collection = site.build_reviews_collection(title, articleId, url) 
```

