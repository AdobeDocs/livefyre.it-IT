---
description: Consentite agli utenti di fare clic sulle raccolte da un singolo layout di pagina e URL.
seo-description: Consentite agli utenti di fare clic sulle raccolte da un singolo layout di pagina e URL.
seo-title: Cambia raccolta
solution: Experience Manager
title: Cambia raccolta
uuid: 69bafcc7-c55e-47d6-bc79-b0db80fdf138
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Cambia raccolta{#change-collection}

Consentite agli utenti di fare clic sulle raccolte da un singolo layout di pagina e URL.

Utilizzate Change Collection Delegate (Modifica delegato raccolta) per modificare la raccolta visualizzata su una pagina, senza modificare l'URL, mentre un'app Livefyre è già caricata. Utilizzate questa funzione per visualizzare gallerie di foto o video o altre app in cui la raccolta visualizzata dovrebbe cambiare dopo un'azione dell'utente.

Ad esempio, facendo clic su un video o una foto in una galleria, verrà caricata una raccolta specifica per tale selezione, mentre l'URL della pagina non verrà modificato.

Per caricare una delle tre raccolte da una singola pagina di conteggio dei [commenti](/help/implementation/c-advanced-topics/t-display-comment-count.md) :

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

