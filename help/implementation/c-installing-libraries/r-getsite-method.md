---
description: Restituisce un nuovo oggetto Site.
seo-description: Restituisce un nuovo oggetto Site.
seo-title: Metodo di rete getsite
solution: Experience Manager
title: Metodo di rete getsite
uuid: 67 de 781 e -5240-4 be 5-9 e 93-c 614828 e 0 bb 5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Metodo di rete getsite{#getsite-network-method}

Restituisce un nuovo oggetto Site.
| Variabile | Tipo | Descrizione|
|— |— |— |
| Siteid | Stringa | ID di Livefyre fornito per il sito Web o l'applicazione a cui appartiene la raccolta. Ad esempio: 303617. |
| Sitekey | String | The Chiave segreta di Livefyre per siteid. |

## Esempio Java {#section_nyl_ycs_rz}

```
Site site = network.getSite(siteId, siteKey); 
```

## Esempio nodejs {#section_xkd_gds_rz}

```
var site = network.getSite(siteId, siteKey); 
```

## PHP Example {#section_ghf_gds_rz}

```
$site = $network->getSite(siteId, siteKey);
```

## Esempio Python {#section_dwg_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

## Esempio Ruby {#section_enh_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

