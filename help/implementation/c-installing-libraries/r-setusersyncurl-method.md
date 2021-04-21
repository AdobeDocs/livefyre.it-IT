---
description: Informa Livefyre ad aggiornare l’URL di sincronizzazione utente della rete a quello fornito. Restituisce un valore Boolean.
title: setUserSyncUrl, metodo di rete
exl-id: 8124ac0f-013f-4943-a33c-6cf8fe696f95
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 4%

---

# setUserSyncUrl Network Method{#setusersyncurl-network-method}

Informa Livefyre ad aggiornare l’URL di sincronizzazione utente della rete a quello fornito. Restituisce un valore Boolean.

| Variabile | Tipo | Descrizione |
|--- |--- |--- |
| urlTemplate | Stringa | URL da registrare con Livefyre per la sincronizzazione degli ID utente. Richiede &quot;`{id}`&quot; per far parte della stringa URL fornita. |

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

## Esempio di pitone {#section_dwg_gds_rz}

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
