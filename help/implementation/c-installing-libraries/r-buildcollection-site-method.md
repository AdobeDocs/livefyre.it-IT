---
description: nulle
seo-description: nulle
seo-title: Metodo Site Buildcollection
solution: Experience Manager
title: Metodo Site Buildcollection
uuid: 52 abc 42 a -9506-4492-b 219-f 2 e 05 eb 79 c 5 f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Metodo Site Buildcollection{#buildcollection-site-method}

| Variabile | Tipo | Descrizione |
|--- |--- |--- |
| type | Collectiontype | Il tipo di raccolta. |
| title | Stringa | Titolo della raccolta. |
| Articleid | Stringa | Un ID articolo univoco che avete scelto di identificare una raccolta all&#39;interno del sito. |
| url | Stringa | L&#39;URL assoluto canonico per questa raccolta. |

## Esempio Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildCollection(type, title, articleId, url); 
```

## Esempio nodejs {#section_xkd_gds_rz}

```
var collection = site.buildCollection(type, title, articleId, url); 
```

## PHP Example {#section_ghf_gds_rz}

```
$collection = site->buildCollection(type, title, articleId, url); 
```

## Esempio Python {#section_dwg_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```

## Esempio Ruby {#section_enh_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```
