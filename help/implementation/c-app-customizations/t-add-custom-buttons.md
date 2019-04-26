---
description: Aggiungete azioni personalizzate alle vostre app Livefyre.
seo-description: Aggiungete azioni personalizzate alle vostre app Livefyre.
seo-title: Aggiungere pulsanti personalizzati
solution: Experience Manager
title: Aggiungere pulsanti personalizzati
uuid: 27 d 24 c 21-d 83 f -49 df -9 b 3 f -15 d 7 abbd 2 bd 7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Aggiungere pulsanti personalizzati{#add-custom-buttons}

Aggiungete azioni personalizzate alle vostre app Livefyre.

Livefyre consente di aggiungere pulsanti personalizzati accanto ai pulsanti di azione esistenti (come **[!UICONTROL Share]**e **[!UICONTROL Flag]**) su una parte del contenuto.

Utilizzate l'argomento mobile per definire se il pulsante verrà visualizzato sui dispositivi mobili.

Ad esempio, per aggiungere un pulsante di azione personalizzato per l'interfaccia del dispositivo mobile:

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

1. Trasmettere un argomento aggiuntivo nell'oggetto convconfig denominato actionbuttons, contenente un array di oggetti che descrive ciascun pulsante da aggiungere.
1. Definire una chiave per il testo da visualizzare per ogni pulsante.
1. Aggiungete una callback che verrà richiamata su un evento click per ciascun pulsante.

Il callback viene richiamato con un oggetto con due chiavi: `authorId` e `contentId`.
