---
description: Restituisce un oggetto Collection creata come tipo di conteggio. Eseguite
  create_ or_ update () dall'oggetto Collection per completare il processo di creazione.
seo-description: Restituisce un oggetto Collection creata come tipo di conteggio.
  Eseguite create_ or_ update () dall'oggetto Collection per completare il processo
  di creazione.
seo-title: Metodo Site buildcountingcollection
title: Metodo Site buildcountingcollection
uuid: e 293 d 66 a -0025-4230-997 e -295 ce 4625713
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Metodo Site buildcountingcollection{#buildcountingcollection-site-method}

Restituisce un oggetto Collection creata come tipo di conteggio. Eseguite create_ or_ update () dall'oggetto Collection per completare il processo di creazione.

| Variabile | Tipo | Descrizione |
|--- |--- |--- |
| title | Stringa | Titolo della raccolta. |
| Articleid | Stringa | Un ID articolo univoco che avete scelto di identificare una raccolta all'interno del sito. |
| url | Stringa | L'URL assoluto canonico per questa raccolta. |

## Esempio Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildCountingCollection(title, articleId, url); 
```

## Esempio nodejs {#section_xkd_gds_rz}

```
var collection = site.buildCountingCollection(title, articleId, url); 
```

## PHP Example {#section_ghf_gds_rz}

```
$collection = site->buildCountingCollection(title, articleId, url); 
```

## Esempio Python {#section_dwg_gds_rz}

```
collection = site.build_counting_collection(title, articleId, url) 
```

## Esempio Ruby {#section_enh_gds_rz}

```
collection = site.build_counting_collection(title, articleId, url) 
```

