---
description: Aggiungi azioni personalizzate alle tue app Livefyre.
seo-description: Aggiungi azioni personalizzate alle tue app Livefyre.
seo-title: Aggiungi pulsanti personalizzati
solution: Experience Manager
title: Aggiungi pulsanti personalizzati
uuid: 27d24c21-d83f-49df-9b3f-15d7abbd2bd7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---


# Aggiungi pulsanti personalizzati{#add-custom-buttons}

Aggiungi azioni personalizzate alle tue app Livefyre.

Livefyre consente di aggiungere pulsanti personalizzati accanto ai pulsanti di azione esistenti (come **[!UICONTROL Share]** e **[!UICONTROL Flag]**) su un contenuto.

Utilizzare l&#39;argomento mobile per definire se il pulsante verrà visualizzato o meno sui dispositivi mobili.

Ad esempio, per aggiungere un pulsante di azione personalizzato all’interfaccia del dispositivo mobile:

```
var convConfig = {...}; // Should have siteId, articleId, etc. 
convConfig.actionButtons = [ 
   { 
      mobile: true,  
      // (optional) sets whether the button will appear on mobile devices 
      key: 'Do Something', 
      callback: function(contentInfo) { 
         console.log('Author of content is ' + contentInfo.authorId); 
         console.log('id of content is ' + contentInfo.contentId); 
      } 
   }, 
    ... 
]; 
  
fyre.conv.load(networkConfig, [convConfig]);
```

1. Passa un argomento aggiuntivo nell’oggetto ConvConfig denominato actionButtons, contenente un array di oggetti che descrivono ciascun pulsante da aggiungere.
1. Definire un tasto per il testo da visualizzare per ciascun pulsante.
1. Aggiungete un callback che verrà richiamato in un evento click per ciascun pulsante.

Il callback viene richiamato con un oggetto con due chiavi: `authorId` e `contentId`.
