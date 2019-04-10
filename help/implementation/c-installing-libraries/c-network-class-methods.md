---
description: Creare un oggetto Network.
seo-description: Creare un oggetto Network.
seo-title: Metodi della classe network
solution: Experience Manager
title: Metodi della classe network
uuid: 4130 beda-dd 09-49 ae-aafb-f 6 b 956 e 30 b 51
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Metodi della classe network{#network-class-methods}

Creare un oggetto Network.

Dopo aver creato un oggetto di rete, il resto della pagina presuppone che nella sessione sia presente un oggetto Rete creata.

## Oggetto di rete

| Parametro | Tipo | Descrizione |
|---|---|---|
| *`network`* | Stringa | La rete Livefyre. Ad esempio: «`labs.fyre.co`». |
| *`networkKey`* | Stringa | Chiave segreta di Livefyre per la rete. |

## Java {#section_myk_dzs_kbb}

```
import com.livefyre.Livefyre; 
  
Network network = Livefyre.getNetwork(network, networkKey); 
```

## Nodejs {#section_nyk_dzs_kbb}

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
