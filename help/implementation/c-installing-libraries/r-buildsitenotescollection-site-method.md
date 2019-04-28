---
description: Restituisce un oggetto Collection creata come tipo Sidenotes. Eseguite create_ or_ update () dall'oggetto Collection per completare il processo di creazione.
seo-description: Restituisce un oggetto Collection creata come tipo Sidenotes. Eseguite create_ or_ update () dall'oggetto Collection per completare il processo di creazione.
seo-title: Metodo Sitdsitenotescollection Site
solution: Experience Manager
title: Metodo Sitdsitenotescollection Site
uuid: 2 bfbc 032-4 c 0 c -48 d 2-8 ce 6-02460 b 38 bd 6 c
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Metodo Sitdsitenotescollection Site{#buildsitenotescollection-site-method}

Restituisce un oggetto Collection creata come tipo Sidenotes. Eseguite create_ or_ update () dall&#39;oggetto Collection per completare il processo di creazione.

| Variabile | Tipo | Descrizione |
|--- |--- |--- |
| title | Stringa | Titolo della raccolta. |
| Articleid | Stringa | Un ID articolo univoco che avete scelto di identificare una raccolta all&#39;interno del sito. |
| url | Stringa | L&#39;URL assoluto canonico per questa raccolta. |

## Esempio Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildSidenotesCollection(title, articleId, url); 
```

## Esempio nodejs {#section_xkd_gds_rz}

```
var collection = site.buildSidenotesCollection(title, articleId, url); 
```

## PHP Example {#section_ghf_gds_rz}

```
$collection = site->buildSidenotesCollection(title, articleId, url); 
```

## Esempio Python {#section_dwg_gds_rz}

```
collection = site.build_sidenotes_collection(title, articleId, url) 
```

## Esempio Ruby {#section_enh_gds_rz}

```
collection = site.build_sidenotes_collection(title, articleId, url) 
```
