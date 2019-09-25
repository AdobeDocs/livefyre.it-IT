---
description: Restituisce un oggetto Collection istanziato come tipo Sidenotes. Eseguire create_or_update() dall'oggetto Collection per completare il processo di compilazione.
seo-description: Restituisce un oggetto Collection istanziato come tipo Sidenotes. Eseguire create_or_update() dall'oggetto Collection per completare il processo di compilazione.
seo-title: Metodo del sito buildSiteNoteCollection
solution: Experience Manager
title: Metodo del sito buildSiteNoteCollection
uuid: 2bfbc032-4c0c-48d2-8ce6-02460b38bd6c
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Metodo del sito buildSiteNoteCollection{#buildsitenotescollection-site-method}

Restituisce un oggetto Collection istanziato come tipo Sidenotes. Eseguire create_or_update() dall'oggetto Collection per completare il processo di compilazione.

| Variabile | Tipo | Descrizione |
|--- |--- |--- |
| title | Stringa | Titolo della raccolta. |
| articleId | Stringa | Un ID articolo univoco scelto per identificare una raccolta all'interno del sito. |
| url | Stringa | L'URL assoluto canonico per questa raccolta. |

## Esempio Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildSidenotesCollection(title, articleId, url); 
```

## Esempio NodeJS {#section_xkd_gds_rz}

```
var collection = site.buildSidenotesCollection(title, articleId, url); 
```

## Esempio PHP {#section_ghf_gds_rz}

```
$collection = site->buildSidenotesCollection(title, articleId, url); 
```

## Esempio di Python {#section_dwg_gds_rz}

```
collection = site.build_sidenotes_collection(title, articleId, url) 
```

## Esempio di ruby {#section_enh_gds_rz}

```
collection = site.build_sidenotes_collection(title, articleId, url) 
```
