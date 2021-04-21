---
description: Integra un’app Sidenotes seguendo un processo simile alle applicazioni core.
title: Integrazione di Sidenote
exl-id: 368951b1-fef2-46d8-b89c-68c46962e937
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 1%

---

# Integrazione Sidenote{#sidenotes-integration}

Integra un’app Sidenotes seguendo un processo simile alle applicazioni core.

Come regola generale, se l&#39;integrazione dell&#39;applicazione core è completa, il codice scritto per generare l&#39;oggetto `collectionMeta` può essere riutilizzato per le note.

Puoi anche riutilizzare i delegati esistenti `auth` fornendo un delegato `auth` creato con `fyre.conv` alle note nel campo (facoltativo) `authDelegate` .

>[!NOTE]
>
>Le note consentono di includere `network`, `siteId` e `articleId` in un singolo oggetto, anziché trasmetterli separatamente in altre parti del costruttore.

```
<!DOCTYPE html> 
<html> 
<head> 
<!-- First add Livefyre.js to the page --> 
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
</head> 
<body> 
<script type="text/javascript"> 
var convConfig = { 
 network: 'client-solutions.fyre.co', 
 selectors:'span.lyrics-sidenote', 
 siteId: '356373', 
 articleId: 'sidenotes-sample', 
 collectionMeta: 'eyJhbGciOiAiSFMyNTYiLCAidHlwIjogIkpXVCJ9.eyJ1cmwiOiAiaHR0cDovL3d3dy5zaWRlbm90ZXMtZGVtby5jb20vbHlyaWNzIiwgInNpdGVJZCI6ICIzMDQwNTkiLCAidHlwZSI6ICJzaWRlbm90ZXMiLCAiYXJ0aWNsZUlkIjogInNpZGVub3Rlc19zYW1wbGUiLCAidGl0bGUiOiAiQ2xpZW50IFNvbHV0aW9ucyBTaWRlbm90ZXMifQ.2gxnsM0TS8dfp-Jokb5uW1kuMl-DqIlqfJSCBwJgf1k' 
}; 
  
Livefyre.require(['sidenotes#1', 'auth'], function (Sidenotes, Auth) { 
 new Sidenotes(convConfig); 
 Auth.delegate({ 
 login: function (callback) { 
 callback(null,{livefyre:'<userauthtoken>'}); 
 } 
 }); 
 }); 
</script> 
</body> 
</html>
```

Come indicato nella sezione Generazione `collectionMeta` , `collectionMeta` è un oggetto JSON codificato. Nell’esempio precedente, l’oggetto JSON assume il formato seguente prima della codifica JWT.

```
{ 
"title":"Client Solutions Sidenotes", 
"url":"http:\/\/www.livefyre.com\/sidenotes", 
"articleId":"sidenotes_sample", 
"siteId":"304059", 
"type":"sidenotes" 
}
```

Per ulteriori informazioni, consulta il token `collectionMeta` .

## Configurazione mobile

Note a video è stato ottimizzato per l’utilizzo su dispositivi mobili. Per risultati migliori con le versioni mobili dell’app Livefyre, imposta l’opzione scalabile dall’utente su no. Ad esempio:

```
<meta name="viewport" content="width=device-width, user-scalable=no">
```
