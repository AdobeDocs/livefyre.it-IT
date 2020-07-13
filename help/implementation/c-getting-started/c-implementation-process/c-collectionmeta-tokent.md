---
description: Create un token univoco sul server che identifichi ogni raccolta creata.
seo-description: Create un token univoco sul server che identifichi ogni raccolta creata.
seo-title: CollectionMeta Token
solution: Experience Manager
title: CollectionMeta Token
uuid: d5db0b0f-2807-4392-874a-94ac3c1e7550
translation-type: tm+mt
source-git-commit: acba83da6abd919062025322beeced500a3db662
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 1%

---


# CollectionMeta Token{#collectionmeta-token}

Create un token univoco sul server che identifichi ogni raccolta creata.

Livefyre assegna un identificatore univoco a ogni raccolta creata. Livefyre assegna un titolo, un URL e altri parametri, tra cui:

## collectionMeta Token Parameters

| Parametro | Tipo | Descrizione |
|--- |--- |--- |
| networkName | String (facoltativo) | Il nome della rete Livefyre (disponibile da {!UICONTROL Studio > Settings > Integration Settings > Credentials]). Questo è facoltativo quando si utilizza la libreria per creare un token collectionMeta. |
| networkKey | String (facoltativo) | La chiave segreta per la rete specifica (disponibile da Studio > Impostazioni > Impostazioni integrazione > Credenziali ). Questo è facoltativo quando si utilizza la libreria per creare un token collectionMeta. |
| siteId | String (facoltativo) | L’ID del sito (disponibile da [!UICONTROL Studio > Settings > Integration Settings > Credentials] ). Facoltativo quando si utilizza la libreria per creare un token collectionMeta. |
| siteKey | String (facoltativo) | La chiave segreta per il sito (disponibile da {!UICONTROL Studio > Impostazioni > Impostazioni integrazione > Credenziali]). |
| articleId | String (facoltativo) | Un ID univoco per la raccolta. |
| title | String (facoltativo) | Titolo da applicare alla raccolta. In genere corrisponde al titolo della pagina in cui è visualizzata l&#39;app. <br>Ad esempio: &quot;L&#39;integrazione è così divertente!&quot; <br>Nota:  La lunghezza massima dei caratteri per il titolo è di 255 caratteri. Il campo title non supporta le entità HTML. Codificare caratteri speciali utilizzando UTF-8. |
| url | String (facoltativo) | L&#39;URL assoluto canonico che si desidera allegare a questa raccolta. Questo URL verrà utilizzato per generare i collegamenti all&#39;app dal contenuto condiviso su Facebook e Twitter, dalle notifiche e-mail e da Livefyre Studio. <br>Nota:  Se esegui il test localmente, usa un dominio URL di base valido (ad esempio: valid: `https://customer.com`; non valido: `https://localhost:5995`). |
| tags | String (facoltativo) | Elenco separato da virgole di parole chiave singole o di frasi. Cercare le raccolte in base ai tag utilizzando Studio.  </br>Nota:  I tag non possono contenere spazi. Utilizzate i caratteri di sottolineatura per visualizzare uno spazio nell’interfaccia utente. |
| extensions | JSON (facoltativo) | Un set di param formattati JSON da passare alla raccolta. |

## Java {#section_orz_m4n_sz}

```
import com.livefyre.Livefyre; 
import com.livefyre.core.Network; 
import com.livefyre.core.Site; 
import com.livefyre.core.Collection; 
  
Network network = Livefyre.getNetwork("networkName", "networkKey"); 
Site site = network.getSite("siteId", "siteKey"); 
Collection collection = site.buildCommentsCollection("title", "articleId", "https://www.example.com"); 
collection.getData().setTags("tags"); 
  
String collectionMetaToken = collection.buildCollectionMetaToken();
```

## NodeJS {#section_kpk_44n_sz}

```
var livefyre = require('livefyre'); 
  
var network = livefyre.getNetwork('networkName', 'networkKey'); 
var site = network.getSite('siteId', 'siteKey'); 
var collection = site.buildCommentsCollection('title', 'articleId', 'https://www.example.com'); 
collection.data.tags = 'tags'; 
  
var collectionMetaToken = collection.buildCollectionMetaToken(); 
```

## PHP {#section_zmd_zbj_tz}

```
$network = Livefyre::getNetwork("networkName", "networkKey"); 
$site = $network->getSite("siteId", "siteKey"); 
$collection = $site->buildCommentsCollection("title", "articleId", "https://www.example.com"); 
$collection->getData()->setTags("tags"); 
  
$collectionMetaToken = $collection->buildCollectionMetaToken();
```

## Python {#section_rdm_prj_tz}

```
from livefyre import Livefyre 
  
network = Livefyre.get_network('networkName', 'networkKey') 
site = network.get_site('siteId', 'siteKey') 
collection = site.build_comments_collection('title', 'articleId', 'https://www.example.com') 
collection.data.tags = 'tags' 
  
collection_meta_token = collection.build_collection_meta_token()
```

## Ruby {#section_l5n_qrj_tz}

```
require 'livefyre' 
  
network = Livefyre.get_network('networkName', 'networkKey') 
site = network.get_site('siteId', 'siteKey') 
collection = site.build_comments_collection('title', 'articleId', 'https://www.example.com') 
collection.data.tags = 'tags' 
  
collection_meta_token = collection.build_collection_meta_token 
```

>[!NOTE]
>
>Livefyre riceve il token collectionMeta generato e determina l’univocità combinando siteId (Livefyre fornito) e articleId (cliente specificato).
