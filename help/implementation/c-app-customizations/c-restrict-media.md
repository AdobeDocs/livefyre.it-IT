---
description: Limita il tipo di file multimediali che accede allo streaming dell'app.
seo-description: Limita il tipo di file multimediali che accede allo streaming dell'app.
seo-title: Limita file multimediali
solution: Experience Manager
title: Limita file multimediali
uuid: c470c985-d221-4f39-8bd4-4e44ec14db95
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Limita file multimediali{#restrict-media}

Limita il tipo di file multimediali che accede allo streaming dell'app.

Per impostazione predefinita, tutti gli allegati multimediali possono essere incorporati nelle app. Livefyre consente di modificare questa opzione per impedire agli utenti di inviare i tipi di allegati selezionati alle app.

>[!NOTE]
>
>Livefyre collabora con Embedded per l'integrazione con i media. Per ulteriori informazioni, vedere Integrazione dei contenuti &gt; Integrazione incorporata. Per domande sull'espansione dei collegamenti o sulle origini, contattate l'Account Manager tecnico.

In questo esempio YouTube e Vimeo vengono bloccati dal flusso di commenti:

```
var attachmentDelegate = function(embedObj) { 
   var providersToBlock = ['youtube', 'vimeo']; 
   for (var i=0, len=providersToBlock.length; i<len; i++) { 
      if (embedObj.provider_url.indexOf(providersToBlock[i]) > -1) { 
         return false; 
      } 
   } 
   return true; 
};
```

Durante il caricamento della conversazione:

```
networkConfig["attachmentDelegate"] = attachmentDelegate; 
fyre.conv.load(networkConfig, [convConfig]);
```

