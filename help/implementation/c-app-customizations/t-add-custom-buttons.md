---
description: Aggiungi azioni personalizzate alle app Livefyre.
title: Aggiungi pulsanti personalizzati
exl-id: a62d8605-59c2-4214-af26-805c1989aca1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---

# Aggiungi pulsanti personalizzati{#add-custom-buttons}

Aggiungi azioni personalizzate alle app Livefyre.

Livefyre consente di aggiungere pulsanti personalizzati accanto ai pulsanti di azione esistenti (come **[!UICONTROL Share]** e **[!UICONTROL Flag]**) su un contenuto.

Utilizza l’argomento mobile per definire se il pulsante verrà visualizzato sui dispositivi mobili.

Ad esempio, per aggiungere un pulsante di azione personalizzato per l’interfaccia del dispositivo mobile:

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

1. Passa un argomento aggiuntivo nell&#39;oggetto ConvConfig denominato actionButtons, contenente una matrice di oggetti che descrivono ogni pulsante che si desidera aggiungere.
1. Definire una chiave per il testo da visualizzare per ciascun pulsante.
1. Aggiungi un callback che verrà richiamato su un evento click per ogni pulsante.

Il callback viene richiamato con un oggetto con due chiavi: `authorId` e `contentId`.
