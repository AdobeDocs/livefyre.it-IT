---
description: Restituisce un nuovo oggetto Site.
title: getSite, metodo di rete
exl-id: 88782da9-88c6-4e60-9a23-e46d68675d59
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '54'
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

## Esempio di pitone {#section_dwg_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

## Esempio di ruby {#section_enh_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```
