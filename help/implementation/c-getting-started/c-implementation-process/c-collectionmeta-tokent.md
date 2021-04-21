---
description: Crea un token univoco sul server che identifica ogni raccolta creata.
title: Token CollectionMeta
exl-id: 52edfe75-5ce6-40c9-9afe-c34a3812f1e7
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 2%

---

# CollectionMeta Token{#collectionmeta-token}

Crea un token univoco sul server che identifica ogni raccolta creata.

Livefyre assegna un identificatore univoco a ogni raccolta creata. Livefyre assegna un titolo, un URL e altri parametri, tra cui:

## parametri collectionMeta Token

| Parametro | Tipo | Descrizione |
|--- |--- |--- |
| networkName | Stringa (facoltativo) | Nome della rete Livefyre (disponibile da [!UICONTROL Studio] > [!UICONTROL Settings] > [!UICONTROL Integration Settings] > [!UICONTROL Credentials] ). Questo è facoltativo quando si utilizza la libreria per creare un token collectionMeta. |
| networkKey | Stringa (facoltativo) | Chiave segreta per la rete specifica (disponibile da Studio > Impostazioni > Impostazioni integrazione > Credenziali ). Questo è facoltativo quando si utilizza la libreria per creare un token collectionMeta. |
| siteId | Stringa (facoltativo) | L&#39;ID del sito (disponibile da [!UICONTROL Studio > Settings > Integration Settings > Credentials] ). Facoltativo quando si utilizza la libreria per creare un token collectionMeta. |
| siteKey | Stringa (facoltativo) | Chiave segreta per il sito (disponibile da [!UICONTROL Studio > Settings > Integration Settings > Credentials] ). |
| articleId | Stringa (facoltativo) | Un ID univoco per la raccolta. |
| title | Stringa (facoltativo) | Titolo da applicare alla Raccolta. Di solito corrisponde al titolo della pagina che visualizza l’app. <br>Ad esempio: &quot;L&#39;integrazione è così divertente!&quot; <br>Nota: La lunghezza massima dei caratteri per il titolo è di 255 caratteri. Il campo titolo non supporta le entità HTML. Codifica caratteri speciali utilizzando UTF-8. |
| url | Stringa (facoltativo) | URL assoluto canonico da allegare a questa raccolta. Questo URL verrà utilizzato per generare collegamenti all’app dal contenuto condiviso su Facebook e Twitter, dalle notifiche e-mail e da Livefyre Studio. <br>Nota: Se esegui il test localmente, utilizza un dominio URL di base valido (ad esempio: valido:  `https://customer.com`; non valido:  `https://localhost:5995`). |
| tag | Stringa (facoltativo) | Elenco separato da virgole di singole parole chiave o frasi. Ricerca raccolte per tag utilizzando Studio.  </br>Nota: I tag non possono contenere spazi. Utilizza i caratteri di sottolineatura se desideri che uno spazio venga visualizzato nell’interfaccia utente. |
| estensioni | JSON (facoltativo) | Un set di parametri formattati JSON da passare alla raccolta. |

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
>Livefyre riceve il token collectionMeta che crei e determina l’univocità combinando siteId (Livefyre fornito) e articleId (cliente specificato).
