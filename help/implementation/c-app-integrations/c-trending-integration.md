---
description: Mostra le raccolte più attive sul sito o sulla rete.
seo-description: Mostra le raccolte più attive sul sito o sulla rete.
seo-title: Tendenza
solution: Experience Manager
title: Tendenza
uuid: 3031523d-b487-4eea-bba6-5d8f9971874f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Tendenza{#trending}

Mostra le raccolte più attive sul sito o sulla rete.

Utilizzate Trending per mostrare le raccolte con l'attività più recente nel sito o nella rete.

## Integrazione {#section_wtz_whb_c1b}

Il modo più rapido per integrarsi con Trending è utilizzare la versione integrata ospitata sulla rete CDN di Livefyre.

Innanzitutto, aggiungete [Livefyre.js](https://github.com/Livefyre/Livefyre.js) alla pagina.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

Quindi, posizionate l'elemento in cui verrà visualizzata l'app.

```
<div id="trending"></div>
```

Infine, utilizzare `Livefyre.require` per creare il componente.

```
<script> 
Livefyre.require([ 
   'streamhub-hot-collections#0' 
], function(Trending) {     
   var app = new Trending({ 
      el: document.getElementById("trending"), 
      network: 'livefyre.com' 
   }); 
   app.start(); 
}); 
</script>
```

Ora hai un'app di tendenza! Vedete tutto in azione in [questo esempio](https://codepen.io/gobengo/pen/GijEy).

## Configurazione {#section_k5k_qhb_c1b}

`network`

Rete da cui verranno estratte le raccolte. (Obbligatorio.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com' 
});
```

`siteId`

Immettete l'ID sito per visualizzare le raccolte solo da un singolo sito all'interno della rete. (Facoltativo.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4 
});
```

`tag`

Fornite un singolo tag Collection per mostrare solo le raccolte con tale tag. (Facoltativo.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4, 
   tag: 'basketball' 
});
```

