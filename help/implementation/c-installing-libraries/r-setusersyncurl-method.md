---
description: Informa Livefyre ad aggiornare l'URL di sincronizzazione degli utenti della rete a quello fornito. Restituisce un valore Boolean.
seo-description: Informa Livefyre ad aggiornare l'URL di sincronizzazione degli utenti della rete a quello fornito. Restituisce un valore Boolean.
seo-title: setUserSyncUrl, metodo di rete
solution: Experience Manager
title: setUserSyncUrl, metodo di rete
uuid: cd067e90-a2da-4e3d-8e60-7eabfd86fc7f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---


# setUserSyncUrl, metodo di rete{#setusersyncurl-network-method}

Informa Livefyre ad aggiornare l&#39;URL di sincronizzazione degli utenti della rete a quello fornito. Restituisce un valore Boolean.

| Variabile | Tipo | Descrizione |
|--- |--- |--- |
| urlTemplate | Stringa | URL per la registrazione con Livefyre per la sincronizzazione degli ID utente. Richiede &quot;`{id}`&quot; per far parte della stringa URL fornita. |

## Esempio Java {#section_nyl_ycs_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

Output campione:

```
true
```

## Esempio NodeJS {#section_xkd_gds_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

Output campione:

```
true
```

## Esempio PHP {#section_ghf_gds_rz}

```
$network->setUserSyncUrl(urlTemplate); 
```

Output campione:

```
true
```

## Esempio Python {#section_dwg_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

Output campione:

```
True
```

## Esempio di ruby {#section_enh_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

Output campione:

```
True
```
