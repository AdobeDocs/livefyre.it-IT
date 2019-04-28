---
description: Restituisce un oggetto Collection creata come tipo Chat. Eseguite create_ or_ update () dall'oggetto Collection per completare il processo di creazione.
seo-description: Restituisce un oggetto Collection creata come tipo Chat. Eseguite create_ or_ update () dall'oggetto Collection per completare il processo di creazione.
seo-title: Metodo Site Buildchatcollection
solution: Experience Manager
title: Metodo Site Buildchatcollection
uuid: 39 ee 32 d 0-29 c 9-47 a 8-a 458-a 3 cf 7 a 96 db 30
translation-type: tm+mt
source-git-commit: 2908c6988c706a49c391f0e607bb641bce3a7f0d

---


# Metodo Site Buildchatcollection{#buildchatcollection-site-method}

Restituisce un oggetto Collection creata come tipo Chat. Eseguite create_ or_ update () dall&#39;oggetto Collection per completare il processo di creazione.

| Variabile | Tipo | Descrizione |
|--- |--- |--- |
| title | Stringa | Titolo della raccolta. |
| Articleid | Stringa | Un ID articolo univoco che avete scelto di identificare una raccolta all&#39;interno del sito. |
| url | Stringa | L&#39;URL assoluto canonico per questa raccolta. |

## Esempio Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildChatCollection(title, articleId, url); 
```

## Esempio nodejs {#section_xkd_gds_rz}

```
var collection = site.buildChatCollection(title, articleId, url); 
```

## PHP Example {#section_ghf_gds_rz}

```
$collection = site->buildChatCollection(title, articleId, url); 
```

## Esempio Python {#section_dwg_gds_rz}

```
collection = site.build_chat_collection(title, articleId, url) 
```

## Esempio Ruby {#section_enh_gds_rz}

```
collection = site.build_chat_collection(title, articleId, url)
```
