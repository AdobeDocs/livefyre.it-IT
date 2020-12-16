---
description: Creare un oggetto Network.
seo-description: Creare un oggetto Network.
seo-title: Metodi delle classi di rete
solution: Experience Manager
title: Metodi delle classi di rete
uuid: 4130beda-dd09-49ae-aafb-f6b956e30b51
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 13%

---


# Metodi di classe di rete{#network-class-methods}

Creare un oggetto Network.

Una volta creato un oggetto di rete, il resto della pagina suppone che nella sessione sia presente un oggetto di rete con un&#39;istanza.

## Oggetto di rete

| Parametro | Tipo | Descrizione |
|---|---|---|
| *`network`* | Stringa | La rete Livefyre. Ad esempio: “`labs.fyre.co`”. |
| *`networkKey`* | Stringa | Chiave segreta Livefyre specificata per la rete. |

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
