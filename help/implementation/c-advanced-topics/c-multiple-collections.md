---
description: Presentazione di più raccolte su una singola pagina.
seo-description: Presentazione di più raccolte su una singola pagina.
seo-title: Raccolte multiple
solution: Experience Manager
title: Raccolte multiple
uuid: 9675 ffd 7-1 a 59-42 a 1-b 3 ba -40 af 1744 cfd 1
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e

---


# Raccolte multiple {#multiple-collections}

Presentazione di più raccolte su una singola pagina.

Potete includere più raccolte su una singola pagina sul sito. Ad esempio, per pubblicare un evento, durante l'evento potrebbe essere presente una discussione sul blog live o chat con un'app separata sul lato della pagina, visualizzando i contenuti curati correlati direttamente dal Web social network. Oppure, potete includere un'App commenti sotto un articolo, con una chat a lato.

Per ottenere più conversazioni su una pagina, aggiungete una o più configurazioni in un array e passate l'array alla chiamata di caricamento. Ad esempio.

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
