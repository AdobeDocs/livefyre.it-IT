---
description: Indirizzare il contenuto utente a una mappa interattiva.
seo-description: Indirizzare il contenuto utente a una mappa interattiva.
seo-title: Mappa
solution: Experience Manager
title: Mappa
uuid: 1 c 3 e 399 d-a 610-4 b 80-a 3 b 2-a 5502 b 31480 d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Mappa{#map}

Indirizzare il contenuto utente a una mappa interattiva.

Mappa consente di trasmettere il contenuto con tag su una mappa mondiale, consentendoti di individuare il social buzz intorno a notizie più spesse o a un evento in diretta. Verrà visualizzato tutto il contenuto applicabile, compresi testo, commenti, foto e Tweet.

>[!NOTE]
>
>Le mappe sono basate su [© openstreetmap](https://www.openstreetmap.org/copyright), che fornisce i dati utilizzati da Livefyre per il rendering delle mappe.

## Integrazione {#section_w2m_db2_d1b}

Il modo più rapido per utilizzare Mappa consiste nell&#39;usare la versione integrata nella CDN di Livefyre.

Innanzitutto, aggiungete [Livefyre. js](https://github.com/Livefyre/Livefyre.js) alla pagina.

```
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
```

Quindi, posizionate l&#39;elemento in cui verrà visualizzata l&#39;app mappa.

```
<div id="map" style="height: 500px;"></div>
```

Infine, utilizzate Livefyre. need per creare la mappa e ottenere una raccolta in cui far fluire il flusso da streamer-sdk. Tenete presente che Mappa può mostrare solo Contenuto con metadati con geottag. Twitter e Instagram Curate supportano questa funzione. Per ottenere prestazioni ottimali, includete un filtro di geolocalizzazione su tutte le Regole cura per la raccolta.

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

Controllate questo [esempio live](https://codepen.io/cheung31/pen/wkmbF).

## Configurazione {#section_jc5_gxb_c1b}

`initial`

Il numero iniziale di elementi da caricare dalla raccolta e visualizzati sulla mappa. Una volta caricato questo numero, gli utenti possono fare clic su un pulsante per visualizzarne altri. (Facoltativo. Il valore predefinito è 50.)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    initial: 100 
});
```

`leafletMapOptions`

Opzioni da passare alla mappa [Leaflet](https://leafletjs.com/) sottostante, che Mappa utilizza per il rendering. Usate questa opzione per impostare [le opzioni Mappa dei leaflet](https://leafletjs.com/reference.html#map-options), compreso il punto iniziale iniziale della mappa, nonché i livelli di zoom iniziali e massimi. (Facoltativo)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    leafletMapOptions: { 
        center: [37.774, -122.4], 
        zoom: 15 
    } 
});
```

