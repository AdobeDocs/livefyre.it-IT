---
description: Integrare un'app Sidenotes seguendo un processo simile alle applicazioni di base.
seo-description: Integrare un'app Sidenotes seguendo un processo simile alle applicazioni di base.
seo-title: Integrazione Sidenotes
solution: Experience Manager
title: Integrazione Sidenotes
uuid: 4aa14ada-402a-482d-b43e-96f37afa6c53
translation-type: tm+mt
source-git-commit: fcee9dc152e7f8284e64248fdcc5bf81d39618ff

---


# Integrazione Sidenotes{#sidenotes-integration}

Integrare un'app Sidenotes seguendo un processo simile alle applicazioni di base.

Come regola generale, se l'integrazione dell'applicazione di base è completa, il codice scritto per generare l' `collectionMeta` oggetto può essere riutilizzato per le note.

Potete anche riutilizzare i `auth` delegati esistenti fornendo un `auth` delegato creato con `fyre.conv` i Sidenotes nel campo (facoltativo) `authDelegate` .

>[!NOTE]
>
>Le note consentono di includere `network`, `siteId`e `articleId` in un singolo oggetto, anziché trasmetterle separatamente in altre parti del costruttore.

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

Come indicato nella `collectionMeta` sezione Building, `collectionMeta` è un oggetto JSON codificato. Nell'esempio precedente, l'oggetto JSON ha il formato seguente prima che sia codificato JWT.

```
{ 
"title":"Client Solutions Sidenotes", 
"url":"http:\/\/www.livefyre.com\/sidenotes", 
"articleId":"sidenotes_sample", 
"siteId":"304059", 
"type":"sidenotes" 
}
```

Per ulteriori informazioni, vedete il `collectionMeta` token.

## Configurazione mobile

Le note sono state ottimizzate per l’uso nei dispositivi mobili. Per risultati ottimali con le versioni per dispositivi mobili dell’app Livefyre, impostate l’opzione scalabile utente su no. Ad esempio:

```
<meta name="viewport" content="width=device-width, user-scalable=no">
```
