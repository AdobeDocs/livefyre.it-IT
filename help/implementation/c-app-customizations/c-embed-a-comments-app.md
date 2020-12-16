---
description: L'incorporazione dell'app dei commenti segue il processo di incorporazione di un'app di base.
seo-description: L'incorporazione dell'app dei commenti segue il processo di incorporazione di un'app di base.
seo-title: Incorpora un'app commenti
solution: Experience Manager
title: Incorpora un'app commenti
uuid: e4982ad3-cab1-4805-a55c-594cca3b7203
translation-type: tm+mt
source-git-commit: 268dc91369d346a254b7120706264eb91da8257e
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 1%

---


# Incorpora un&#39;app commenti{#embed-a-comments-app}

L&#39;incorporazione dell&#39;app dei commenti segue il processo di incorporazione di un&#39;app di base.

L&#39;incorporazione dell&#39;app dei commenti segue il processo di incorporazione di un&#39;app di base descritto in [Incorpora un&#39;app](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)

## Esempio 

```
<html> 
  <head> 
    <script src="//cdn.livefyre.com/Livefyre.js"> 
    </script> 
  </head> 
<body> 
    <script type="text/javascript"> 
    var networkConfig = { 
      network: 'domainName' 
    }; 
    var convConfig = { 
      siteId: 'siteId', 
      articleId: 'articleId', 
      el: 'livefyre', 
      collectionMeta: 'collectionMeta', 
      checksum: 'checksum' 
    }; 
    
    Livefyre.require(['fyre.conv#3', 'auth'], function(Conv, auth) { 
        new Conv(networkConfig, [convConfig], function(commentsWidget) {}); 
        auth.delegate({ 
            login: function (callback) { 
                callback(null,{livefyre:'<userauthtoken>'}); 
            }, 
        }); 
    }); 
  
    </script> 
    <div id="livefyre"> 
    </div> 
   </body> 
</html>
```

Come indicato nella sezione Building CollectionMeta, CollectionMeta è un oggetto JSON codificato. Nell&#39;esempio precedente, l&#39;oggetto JSON ha il formato seguente prima che sia codificato JWT:

```
{ 
"url": "articleUrl",  
"articleId": "articleId",  
"type": "livecomments",  
"title": "articleTitle" 
}
```

