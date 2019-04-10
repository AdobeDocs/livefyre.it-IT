---
description: Restituisce un oggetto Collection creata come tipo di blog. Eseguite
  create_ or_ update () dall'oggetto Collection per completare il processo di creazione.
seo-description: Restituisce un oggetto Collection creata come tipo di blog. Eseguite
  create_ or_ update () dall'oggetto Collection per completare il processo di creazione.
seo-title: Metodo Site Buildblogcollection
solution: Experience Manager
title: Metodo Site Buildblogcollection
uuid: 6 a 5 ec 6 b 9-bc 32-467 a-abe 6-a 57 c 6 defe 067
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Metodo Site Buildblogcollection{#buildblogcollection-site-method}

Restituisce un oggetto Collection creata come tipo di blog. Eseguite create_ or_ update () dall'oggetto Collection per completare il processo di creazione.

| Variabile | Tipo | Descrizione |
|--- |--- |--- |
| title | Stringa | Titolo della raccolta. |
| Articleid | Stringa | Un ID articolo univoco che avete scelto di identificare una raccolta all'interno del sito. |
| url | Stringa | L'URL assoluto canonico per questa raccolta. |

## Esempio Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildBlogCollection(title, articleId, url); 
```

## Esempio nodejs {#section_xkd_gds_rz}

```
var collection = site.buildBlogCollection(title, articleId, url); 
```

## PHP Example {#section_ghf_gds_rz}

```
$collection = site->buildBlogCollection(title, articleId, url); 
```

## Esempio Python {#section_dwg_gds_rz}

```
collection = site.build_blog_collection(title, articleId, url) 
```

## Esempio Ruby {#section_enh_gds_rz}

```
collection = site.build_blog_collection(title, articleId, url) 
```

