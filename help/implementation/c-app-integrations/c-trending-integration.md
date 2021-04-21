---
description: Mostra le raccolte più attive sul sito o sulla rete.
title: Tendenza
exl-id: a3129e95-90e7-4107-bfd9-ed3b0dce20aa
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 3%

---

# Tendenza{#trending}

Mostra le raccolte più attive sul sito o sulla rete.

Utilizza Tendenza per mostrare le raccolte con l’attività più recente nel sito o nella rete.

## Integrazione {#section_wtz_whb_c1b}

Il modo più rapido per integrare con Trending è quello di utilizzare la versione incorporata ospitata sulla rete CDN di Livefyre.

Innanzitutto, aggiungi [Livefyre.js](https://github.com/Livefyre/Livefyre.js) alla pagina.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

Quindi, posiziona l’elemento in cui verrà visualizzata l’app.

```
<div id="trending"></div>
```

Infine, utilizza `Livefyre.require` per creare il componente.

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

Ora hai un’app di tendenza! Vedi tutto in azione in [questo esempio](https://codepen.io/gobengo/pen/GijEy).

## Configurazione {#section_k5k_qhb_c1b}

`network`

Rete da cui verranno richiamate le raccolte. (Obbligatorio.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com' 
});
```

`siteId`

Fornisci l’ID del sito per mostrare le raccolte solo da un singolo sito all’interno della rete. (Facoltativo.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4 
});
```

`tag`

Specifica un singolo tag Collection per mostrare solo le raccolte con tale tag. (Facoltativo.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4, 
   tag: 'basketball' 
});
```
