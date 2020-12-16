---
description: Consentite agli utenti di fare clic sulle raccolte da un singolo layout di pagina e URL.
seo-description: Consentite agli utenti di fare clic sulle raccolte da un singolo layout di pagina e URL.
seo-title: Cambia raccolta
solution: Experience Manager
title: Cambia raccolta
uuid: 81c8a554-375f-4659-9e25-5b3618824633
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# Cambia raccolta {#change-collection}

Consentite agli utenti di fare clic sulle raccolte da un singolo layout di pagina e URL.

Utilizzate Change Collection Delegate (Modifica delegato raccolta) per modificare la raccolta mostrata in una pagina, senza modificare l&#39;URL, mentre un&#39;app Livefyre è già caricata. Utilizzate questa funzione per visualizzare gallerie di foto o video o altre app in cui la raccolta visualizzata dovrebbe cambiare dopo un&#39;azione dell&#39;utente.

Ad esempio, facendo clic su un video o una foto in una galleria, verrà caricata una raccolta specifica per tale selezione, mentre l&#39;URL della pagina non verrà modificato.

Per [caricare una delle tre raccolte da una singola pagina](../c-advanced-topics/t-display-comment-count.md#t_display_comment_count):

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
