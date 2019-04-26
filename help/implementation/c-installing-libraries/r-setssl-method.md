---
description: Imposta SSL affinché le chiamate API siano attivate o disattivate.
seo-description: Imposta SSL affinché le chiamate API siano attivate o disattivate.
seo-title: Metodo di rete setssl
solution: Experience Manager
title: Metodo di rete setssl
uuid: 8 d 989 e 63-c 859-456 a -99 ca -8 d 87933913 ba
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Metodo di rete setssl{#setssl-network-method}

Imposta SSL affinché le chiamate API siano attivate o disattivate.

| Variabile | Tipo | Descrizione |
|--- |--- |--- |
| ssl | Booleano | Il valore predefinito è true. Se desiderate SSL, false in caso contrario. <br><ul><li>True - SSL attivato </li><li>Falso - SSL disattivato</li></ul> |

## Esempio Java {#section_nyl_ycs_rz}

```
network.setSsl(ssl); 
```

## Esempio nodejs {#section_xkd_gds_rz}

```
network.ssl = false; 
```

## PHP Example {#section_ghf_gds_rz}

```
$network->setSsl(false); 
```

## Esempio Python {#section_dwg_gds_rz}

```
network.ssl = False 
```

## Esempio Ruby {#section_enh_gds_rz}

```
network.ssl = false 
```
