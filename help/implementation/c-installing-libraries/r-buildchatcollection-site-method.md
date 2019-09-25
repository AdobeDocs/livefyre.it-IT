---
description: Restituisce un oggetto Collection istanziato come tipo Chat. Eseguire create_or_update() dall'oggetto Collection per completare il processo di compilazione.
seo-description: Restituisce un oggetto Collection istanziato come tipo Chat. Eseguire create_or_update() dall'oggetto Collection per completare il processo di compilazione.
seo-title: Metodo del sito buildChatCollection
solution: Experience Manager
title: Metodo del sito buildChatCollection
uuid: 39ee32d0-29c9-47a8-a458-a3cf7a96db30
translation-type: tm+mt
source-git-commit: 2908c6988c706a49c391f0e607bb641bce3a7f0d

---


# Metodo del sito buildChatCollection{#buildchatcollection-site-method}

Restituisce un oggetto Collection istanziato come tipo Chat. Eseguire create_or_update() dall'oggetto Collection per completare il processo di compilazione.

| Variabile | Tipo | Descrizione |
|--- |--- |--- |
| title | Stringa | Titolo della raccolta. |
| articleId | Stringa | Un ID articolo univoco scelto per identificare una raccolta all'interno del sito. |
| url | Stringa | L'URL assoluto canonico per questa raccolta. |

## Esempio Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildChatCollection(title, articleId, url); 
```

## Esempio NodeJS {#section_xkd_gds_rz}

```
var collection = site.buildChatCollection(title, articleId, url); 
```

## Esempio PHP {#section_ghf_gds_rz}

```
$collection = site->buildChatCollection(title, articleId, url); 
```

## Esempio di Python {#section_dwg_gds_rz}

```
collection = site.build_chat_collection(title, articleId, url) 
```

## Esempio di ruby {#section_enh_gds_rz}

```
collection = site.build_chat_collection(title, articleId, url)
```
