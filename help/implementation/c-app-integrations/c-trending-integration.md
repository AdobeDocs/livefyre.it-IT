---
description: Mostrare le raccolte più attive sul sito o sulla rete.
seo-description: Mostrare le raccolte più attive sul sito o sulla rete.
seo-title: Tendenza
solution: Experience Manager
title: Tendenza
uuid: 3031523 d-b 487-4 eea-bba 6-5 d 8 f 9971874 f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Tendenza{#trending}

Mostrare le raccolte più attive sul sito o sulla rete.

Utilizzate Trending per mostrare le raccolte con l&#39;attività più recente nel sito o nella rete.

## Integrazione {#section_wtz_whb_c1b}

Il modo più rapido per effettuare l&#39;integrazione con Trending consiste nell&#39;usare la versione integrata nella CDN di Livefyre.

Innanzitutto, aggiungete [Livefyre. js](https://github.com/Livefyre/Livefyre.js) alla pagina.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

Quindi, posizionate l&#39;elemento in cui verrà visualizzata l&#39;app.

```
<div id="trending"></div>
```

Infine, utilizzate `Livefyre.require` per creare il componente.

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

Ora hai un&#39;app di tendenza! Consultate questa sezione in [questo esempio](https://codepen.io/gobengo/pen/GijEy).

## Configurazione {#section_k5k_qhb_c1b}

`network`

La rete in cui verranno richiamate le raccolte. (Obbligatorio.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com' 
});
```

`siteId`

Fornite l&#39;ID del sito per visualizzare le raccolte solo da un singolo sito all&#39;interno della rete. (Facoltativo)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4 
});
```

`tag`

Fornite un tag raccolta singola per mostrare solo le raccolte con quel tag. (Facoltativo)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4, 
   tag: 'basketball' 
});
```

