---
description: Tracciare il contenuto dell’utente in una mappa interattiva.
title: Mappa
exl-id: 836b475e-0ec6-49f8-b89f-3af3209cf1f2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 2%

---

# Mappa{#map}

Tracciare il contenuto dell’utente in una mappa interattiva.

La mappa consente di inviare i contenuti con tag in una mappa del mondo, consentendoti di individuare il social buzz intorno a notizie aggiornate o a un evento live. Verranno visualizzati tutti i contenuti applicabili, compresi testo, commenti, foto e tweet.

>[!NOTE]
>
>Le mappe sono alimentate da [ ©OpenStreetMap](https://www.openstreetmap.org/copyright), che fornisce i dati utilizzati da Livefyre per il rendering delle sue mappe.

## Integrazione {#section_w2m_db2_d1b}

Il modo più rapido per utilizzare Map è utilizzare la versione incorporata ospitata sulla CDN di Livefyre.

Innanzitutto, aggiungi [Livefyre.js](https://github.com/Livefyre/Livefyre.js) alla pagina.

```
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
```

Quindi, posiziona l’elemento in cui apparirà l’app mappa.

```
<div id="map" style="height: 500px;"></div>
```

Infine, utilizza Livefyre.need per costruire la mappa, e ottenere una raccolta da tubo in da sdk-sdk. Tieni presente che la mappa può mostrare solo il contenuto con metadati geotagged. Questa funzione è supportata da twitter e Instagram Curate. Per garantire le migliori prestazioni, includi un filtro di geolocalizzazione su tutte le regole di cura per la raccolta.

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

Consulta questo [esempio live](https://codepen.io/cheung31/pen/wkmbF).

## Configurazione {#section_jc5_gxb_c1b}

`initial`

Il numero iniziale di elementi da caricare dalla raccolta e visualizzare sulla mappa. Una volta caricato questo numero, gli utenti possono fare clic su un pulsante per visualizzare di più. (Facoltativo. Il valore predefinito è 50.)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    initial: 100 
});
```

`leafletMapOptions`

Opzioni da passare alla mappa sottostante [Foglietto illustrativo](https://leafletjs.com/), che la mappa utilizza per il rendering. Utilizzare questa opzione per impostare le [opzioni mappa foglia](https://leafletjs.com/reference.html#map-options), compreso il punto centrale iniziale della mappa e i livelli di zoom iniziali e massimi. (Facoltativo.)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    leafletMapOptions: { 
        center: [37.774, -122.4], 
        zoom: 15 
    } 
});
```
