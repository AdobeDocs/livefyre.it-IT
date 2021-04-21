---
description: Creare un oggetto Network.
title: Metodi delle classi di rete
exl-id: 5a011120-05d0-4768-9038-6a312e8c5dd1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 14%

---

# Metodi delle classi di rete{#network-class-methods}

Creare un oggetto Network.

Una volta creato un oggetto di rete, il resto della pagina presuppone che nella sessione sia presente un oggetto di rete con istanza.

## Oggetto di rete

| Parametro | Tipo | Descrizione |
|---|---|---|
| *`network`* | Stringa | La tua rete Livefyre. Ad esempio: “`labs.fyre.co`”. |
| *`networkKey`* | Stringa | La chiave segreta fornita da Livefyre per la rete. |

## Java {#section_myk_dzs_kbb}

```
import com.livefyre.Livefyre; 
  
Network network = Livefyre.getNetwork(network, networkKey); 
```

## NodeJS {#section_nyk_dzs_kbb}

```
var livefyre = require('livefyre'); 
  
var network = livefyre.getNetwork(network, networkKey); 
```

## PHP {#section_oyk_dzs_kbb}

```
use Livefyre\Livefyre; 
  
$network = Livefyre::getNetwork(network, networkKey); 
```

## Python {#section_pyk_dzs_kbb}

```
from livefyre import Livefyre 
  
network = Livefyre.get_network(network, networkKey) 
```

## Ruby {#section_qyk_dzs_kbb}

```
require 'livefyre' 
  
network = Livefyre.get_network(network, networkKey) 
```
