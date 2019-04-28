---
description: Informa Livefyre per aggiornare l'URL di sincronizzazione utente della rete a quello fornito. Restituisce un valore booleano.
seo-description: Informa Livefyre per aggiornare l'URL di sincronizzazione utente della rete a quello fornito. Restituisce un valore booleano.
seo-title: Metodo di rete setusersyncurl
solution: Experience Manager
title: Metodo di rete setusersyncurl
uuid: cd 067 e 90-a 2 da -4 e 3 d -8 e 60-7 eabfd 86 fc 7 f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Metodo di rete setusersyncurl{#setusersyncurl-network-method}

Informa Livefyre per aggiornare l&#39;URL di sincronizzazione utente della rete a quello fornito. Restituisce un valore booleano.

| Variabile | Tipo | Descrizione |
|--- |--- |--- |
| Urltemplate | Stringa | L&#39;URL per registrarsi con Livefyre per sincronizzare gli ID utente. Richiede «`{id}`» per far parte della stringa URL fornita. |

## Esempio Java {#section_nyl_ycs_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

Output di esempio:

```
true
```

## Esempio nodejs {#section_xkd_gds_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

Output di esempio:

```
true
```

## PHP Example {#section_ghf_gds_rz}

```
$network->setUserSyncUrl(urlTemplate); 
```

Output di esempio:

```
true
```

## Esempio Python {#section_dwg_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

Output di esempio:

```
True
```

## Esempio Ruby {#section_enh_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

Output di esempio:

```
True
```
