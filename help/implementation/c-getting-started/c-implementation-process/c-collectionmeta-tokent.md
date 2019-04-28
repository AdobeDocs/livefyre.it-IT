---
description: Create un token univoco sul server che identifica tutte le raccolte create.
seo-description: Create un token univoco sul server che identifica tutte le raccolte create.
seo-title: Token collectionmeta
solution: Experience Manager
title: Token collectionmeta
uuid: d 5 db 0 b 0 f -2807-4392-874 a -94 ac 3 c 1 e 7550
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Token collectionmeta{#collectionmeta-token}

Create un token univoco sul server che identifica tutte le raccolte create.

Livefyre assegna un identificatore univoco a ogni raccolta creata. Livefyre assegna un titolo, un URL e altri parametri, tra cui:

## Parametri token collectionmeta

| Parametro | Tipo | Descrizione |
|--- |--- |--- |
| Networkname | Stringa (facoltativa) | Il nome della rete Livefyre (disponibile da {! UICONTROL Studio &gt; Settings &gt; Integration Settings &gt; Credentials]). Questo è facoltativo quando si utilizza la libreria per creare un token collectionmeta. |
| Networkkey | Stringa (facoltativa) | La chiave segreta per la rete specifica (disponibile da Studio &gt; Impostazioni &gt; Impostazioni integrazione &gt; Credenziali). Questo è facoltativo quando si utilizza la libreria per creare un token collectionmeta. |
| Siteid | Stringa (facoltativa) | ID del sito (disponibile da [!UICONTROL Studio > Settings > Integration Settings > Credentials] ). Facoltativo quando si utilizza la libreria per creare un token collectionmeta. |
| Sitekey | Stringa (facoltativa) | La chiave segreta del sito (disponibile da {! UICONTROL Studio &gt; Settings &gt; Integration Settings &gt; Credentials]). |
| Articleid | Stringa (facoltativa) | ID univoco per la raccolta. |
| title | Stringa (facoltativa) | Titolo da applicare alla raccolta. Generalmente corrisponde al titolo della pagina che visualizza l&#39;app. <br>Ad esempio: «Integrazione è molto divertente! »» <br>Nota: La lunghezza massima del carattere per il titolo è 255 caratteri. Il campo Titolo non supporta le entità HTML. Codificate caratteri speciali utilizzando UTF -8. |
| url | Stringa (facoltativa) | L&#39;URL assoluto canonico che desiderate allegare a questa raccolta. Questo URL verrà utilizzato per generare collegamenti all&#39;app dal contenuto condiviso su Facebook e Twitter, notifiche e-mail e Livefyre Studio. <br>Nota: Se esegui il test localmente, usa un dominio URL di base valido (ad esempio: valid: `https://customer.com`; invalid: `https://localhost:5995`). |
| tag | Stringa (facoltativa) | Un elenco separato da virgole di parole chiave o frasi. Cerca raccolte in base ai tag che utilizzano Studio. </br>Nota: I tag non possono contenere spazi. Usate i caratteri di sottolineatura per visualizzare uno spazio nell&#39;interfaccia utente. |
| extensions | JSON (facoltativo) | Un set di parametri formattato JSON da passare alla raccolta. |

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

## Nodejs {#section_kpk_44n_sz}

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

>[!NOTE] {importance = &quot;high&quot;}
>
>Livefyre riceve il token collectionmeta che create e determina l&#39;univocità combinando siteid (Livefyre fornito) e articleid (specificato dal cliente).

