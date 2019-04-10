---
description: Integrare un'app Sidenotes seguendo un processo simile alle applicazioni
  core.
seo-description: Integrare un'app Sidenotes seguendo un processo simile alle applicazioni
  core.
seo-title: Integrazione Sidenotes
solution: Experience Manager
title: Integrazione Sidenotes
uuid: 4 aa 14 ada -402 a -482 d-b 43 e -96 f 37 afa 6 c 53
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Integrazione Sidenotes{#sidenotes-integration}

Integrare un'app Sidenotes seguendo un processo simile alle applicazioni core.

Come regola generale, se l'integrazione di base Applicazione è completa, il codice scritto per generare l' `collectionMeta` oggetto può essere riutilizzato per Sidenotes.

Potete anche riutilizzare `auth` i delegati esistenti fornendo un `auth` delegato creato `fyre.conv` con Sidenotes nel `authDelegate` campo (facoltativo).

>[!NOTE]
>
>Sidenotes consente di includere `network`, `siteId`e `articleId` in un unico oggetto, piuttosto di passare separatamente in altre parti della costruttore.

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

Come indicato nella `collectionMeta` sezione Creazione, `collectionMeta` è un oggetto JSON codificato. Nell'esempio precedente, l'oggetto JSON prende il formato seguente prima che sia codificato.

```
{ 
"title":"Client Solutions Sidenotes", 
"url":"http:\/\/www.livefyre.com\/sidenotes", 
"articleId":"sidenotes_sample", 
"siteId":"304059", 
"type":"sidenotes" 
}
```

Per ulteriori informazioni, consulta `collectionMeta` il token.

## Impostazione mobile

Sidenotes è stato ottimizzato per l'utilizzo nei dispositivi mobili. Per risultati ottimali con le versioni mobili della vostra app Livefyre, impostate l'opzione ridimensionamento dell'utente su No. Ad esempio:

```
<meta name="viewport" content="width=device-width, user-scalable=no">
```
