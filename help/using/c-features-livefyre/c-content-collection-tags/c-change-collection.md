---
description: Consente agli utenti di fare clic sulle raccolte da un layout di pagina e da un URL singoli.
title: Modifica raccolta
exl-id: 5cfae2c6-e328-4d2c-b08b-709be94e4c54
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# Modifica raccolta{#change-collection}

Consente agli utenti di fare clic sulle raccolte da un layout di pagina e da un URL singoli.

Utilizza il delegato Change Collection per modificare la raccolta mostrata in una pagina senza modificare l’URL, mentre un’app Livefyre è già caricata. Utilizza questa funzione per visualizzare gallerie di foto o video o altre app in cui la raccolta visualizzata dovrebbe cambiare dopo un&#39;azione dell&#39;utente.

Ad esempio, facendo clic su un video o una foto in una galleria si carica una raccolta specifica per tale selezione, mentre l’URL della pagina non verrà modificato.

Per caricare una delle tre raccolte da una singola pagina [conteggio commenti](/help/implementation/c-advanced-topics/t-display-comment-count.md):

```
<html> 
<head> 
<script src='//cdn.livefyre.com/Livefyre.js'></script> 
</head> 
<body> 
<script type="text/javascript"> 
convConfig1 = {"collectionMeta": <COLLECTION META 1>, 
             "checksum": <CHECKSUM 1>, 
             "siteId": <SITE ID>, 
             "articleId":"1", 
             "el":"livefyre"}; 
convConfig2 = {"collectionMeta": <COLLECTION META 2>, 
             "checksum": <CHECKSUM 2>, 
             "siteId": <SITE ID>, 
             "articleId":"2", 
             "el":"livefyre"}; 
convConfig3 = {"collectionMeta": <COLLECTION META 3>, 
             "checksum": <CHECKSUM 3>, 
             "siteId": <SITE ID>, 
             "articleId":"3", 
             "el":"livefyre"}; 
  
Livefyre.require(['fyre.conv#prod'],function(Conv) { 
    new Conv({"network": "<NETWORK NAME>"}, 
    [convConfig1], 
    function(app) {  
        window.changeConv = app.changeCollection; 
    } 
    ); 
}); 
</script> 
  
<div id="livefyre"></div> 
<button onclick="window.changeConv(convConfig1);">Conv 1</button> 
<button onclick="window.changeConv(convConfig2);">Conv 2</button> 
<button onclick="window.changeConv(convConfig3);">Conv 3</button> 
</body> 
</html>
```
