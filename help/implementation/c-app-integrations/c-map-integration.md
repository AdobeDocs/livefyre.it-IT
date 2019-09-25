---
description: Tracciare il contenuto dell'utente su una mappa interattiva.
seo-description: Tracciare il contenuto dell'utente su una mappa interattiva.
seo-title: Mappa
solution: Experience Manager
title: Mappa
uuid: 1c3e399d-a610-4b80-a3b2-a5502b31480d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Mappa{#map}

Tracciare il contenuto dell'utente su una mappa interattiva.

La mappa consente di trasmettere in streaming contenuti con geotagged su una mappa del mondo, per individuare il social brusio intorno alle notizie più importanti o a un evento in diretta. Viene visualizzato tutto il contenuto applicabile, inclusi testo, commenti, foto e tweet.

>[!NOTE]
>
>Le mappe sono alimentate da [©OpenStreetMap](https://www.openstreetmap.org/copyright), che fornisce i dati utilizzati da Livefyre per il rendering delle sue mappe.

## Integrazione {#section_w2m_db2_d1b}

Il modo più rapido per utilizzare Mappa consiste nell’utilizzare la versione incorporata ospitata sulla CDN di Livefyre.

Innanzitutto, aggiungete [Livefyre.js](https://github.com/Livefyre/Livefyre.js) alla pagina.

```
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
```

Quindi, posizionate l'elemento in cui apparirà l'app mappa.

```
<div id="map" style="height: 500px;"></div>
```

Infine, utilizzate Livefyre.request per creare la mappa e fate in modo che una raccolta venga implementata da streaming-sdk. Tenete presente che Mappa può mostrare solo il contenuto con metadati con tag. Twitter e Instagram Curate supportano questa funzione. Per garantire prestazioni ottimali, includete un filtro di geolocalizzazione su tutte le regole di cura per la raccolta.

```
<script> 
Livefyre.require(['streamhub-map#1', 'streamhub-sdk#2'], 
function (Map, SDK) { 
    var map = new Map({ 
        el: document.getElementById('map') 
    }); 
    var collection = new SDK.Collection({ 
        network: 'strategy-prod.fyre.co', 
        siteId: 340628, 
        articleId: 'custom-1389845009515' 
    }); 
    collection.pipe(map); 
}); 
</script>
```

Guardate questo [esempio](https://codepen.io/cheung31/pen/wkmbF)live.

## Configurazione {#section_jc5_gxb_c1b}

`initial`

Il numero iniziale di elementi da caricare dalla raccolta e visualizzare sulla mappa. Una volta caricato questo numero, gli utenti possono fare clic su un pulsante per visualizzarne di più. (Facoltativo. Il valore predefinito è 50.)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    initial: 100 
});
```

`leafletMapOptions`

Opzioni per passare alla mappa [Opuscolo](https://leafletjs.com/) sottostante, utilizzata dalla mappa per il rendering. Usate questa opzione per impostare le opzioni [Mappa](https://leafletjs.com/reference.html#map-options)opuscolo, compreso il punto centrale iniziale della mappa, e i livelli di zoom iniziali e massimi. (Facoltativo.)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    leafletMapOptions: { 
        center: [37.774, -122.4], 
        zoom: 15 
    } 
});
```

