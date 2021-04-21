---
description: Limita il tipo di file multimediali che accede al flusso dell'app.
title: Limita file multimediali
exl-id: ae09a058-41de-4b63-8654-cc82f5abad14
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---

# Limita contenuto multimediale{#restrict-media}

Limita il tipo di file multimediali che accede al flusso dell&#39;app.

Per impostazione predefinita, tutti gli allegati multimediali possono essere incorporati nelle app. Livefyre consente di modificare questa opzione per impedire agli utenti di inviare tipi di allegati selezionati alle app.

>[!NOTE]
>
>Livefyre collabora con Embedly per l&#39;integrazione dei contenuti multimediali. Per ulteriori informazioni, consulta Integrazione dei contenuti > Integrazione Embedly. Per domande sull&#39;espansione dei collegamenti o sulle origini, contatta il tuo Account Manager tecnico.

Questo esempio blocca l’incorporamento di YouTube e Vimeo dal flusso di commenti:

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

Al caricamento della conversazione:

```
networkConfig["attachmentDelegate"] = attachmentDelegate; 
fyre.conv.load(networkConfig, [convConfig]);
```
