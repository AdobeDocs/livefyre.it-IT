---
description: Consentite agli utenti di fare clic sulle raccolte da un layout di pagina
  singolo e dall'URL.
seo-description: Consentite agli utenti di fare clic sulle raccolte da un layout di
  pagina singolo e dall'URL.
seo-title: Modifica raccolta
solution: Experience Manager
title: Modifica raccolta
uuid: 81 c 8 a 554-375 f -4659-9 e 25-5 b 3618824633
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Modifica raccolta {#change-collection}

Consentite agli utenti di fare clic sulle raccolte da un layout di pagina singolo e dall'URL.

Utilizzate Change Collection Delegate per modificare la raccolta visualizzata in una pagina, senza modificarne l'URL, mentre un'app Livefyre è già caricata. Utilizzate questa funzione per visualizzare gallerie di foto o video, o altre app in cui la raccolta visualizzata deve cambiare dopo l'azione dell'utente.

Ad esempio, facendo clic su un video o una foto in una galleria, si carica una raccolta specifica per tale selezione, mentre l'URL della pagina non cambia.

[Per caricare una di tre raccolte da una singola pagina](../c-advanced-topics/t-display-comment-count.md#t_display_comment_count):

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
