---
description: Restituisce un nuovo oggetto Site.
seo-description: Restituisce un nuovo oggetto Site.
seo-title: getSite, metodo di rete
solution: Experience Manager
title: getSite, metodo di rete
uuid: 67de781e-5240-4be5-9e93-c614828e0bb5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 0%

---


# getSite Network Method{#getsite-network-method}

Restituisce un nuovo oggetto Site.
|Variabile|Tipo|Descrizione|
| | | |
|siteId|String|L&#39;ID Livefyre fornito per il sito Web o l&#39;applicazione a cui appartiene la raccolta. Ad esempio: 303617.  |
|siteKey|String|La chiave segreta fornita da Livefyre per siteId.  |

## Esempio Java {#section_nyl_ycs_rz}

```
Site site = network.getSite(siteId, siteKey); 
```

## Esempio NodeJS {#section_xkd_gds_rz}

```
var site = network.getSite(siteId, siteKey); 
```

## Esempio PHP {#section_ghf_gds_rz}

```
$site = $network->getSite(siteId, siteKey);
```

## Esempio Python {#section_dwg_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

## Esempio di ruby {#section_enh_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

