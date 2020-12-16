---
description: Visualizzate più raccolte su una singola pagina.
seo-description: Visualizzate più raccolte su una singola pagina.
seo-title: Raccolte multiple
solution: Experience Manager
title: Raccolte multiple
uuid: 9675ffd7-1a59-42a1-b3ba-40af1744cfd1
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 1%

---


# Raccolte multiple {#multiple-collections}

Visualizzate più raccolte su una singola pagina.

Potete includere più raccolte in una singola pagina del sito. Ad esempio, per pubblicare un evento, potete tenere una discussione Live Blog o Chat durante l&#39;evento, con un&#39;app separata sul lato della pagina, che mostra il contenuto curato correlato da tutto il social Web. Oppure, potete includere un&#39;app dei commenti sotto un articolo, con una chat a lato.

Per ottenere più conversazioni su una pagina, aggiungi una o più configurazioni in un array e passa l’array alla chiamata di caricamento. Ad esempio.

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
