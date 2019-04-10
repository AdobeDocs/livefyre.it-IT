---
description: Limita il tipo di supporto che arriva nel flusso app.
seo-description: Limita il tipo di supporto che arriva nel flusso app.
seo-title: Limita file multimediali
solution: Experience Manager
title: Limita file multimediali
uuid: c 470 c 985-d 221-4 f 39-8 bd 4-4 e 44 ec 14 db 95
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Limita file multimediali{#restrict-media}

Limita il tipo di supporto che arriva nel flusso app.

Per impostazione predefinita, tutti gli allegati multimediali possono essere incorporati in App. Livefyre consente di modificare questa opzione per impedire agli utenti di pubblicare tipi di allegati selezionati nelle app.

>[!NOTE]
>
>Livefyre partners with Embedly for media integration. Per ulteriori informazioni, consultate Integrazione dei contenuti > Integrazione con i contenuti. Contattate l'Account Manager tecnico per domande sull'espansione dei collegamenti o sulle origini.

Questo esempio blocca YouTube e Vimeo incorpora dal flusso dei commenti:

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

Quando si carica la conversazione:

```
networkConfig["attachmentDelegate"] = attachmentDelegate; 
fyre.conv.load(networkConfig, [convConfig]);
```

