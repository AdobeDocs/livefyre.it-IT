---
description: Riposizionate il logo Livefyre sulla pagina.
seo-description: Riposizionate il logo Livefyre sulla pagina.
seo-title: Spostare il logo Livefyre
solution: Experience Manager
title: Spostare il logo Livefyre
uuid: 807304 ae -6070-4505-87 db -169 a 925 f 714 c
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Spostare il logo Livefyre{#move-the-livefyre-logo}

Riposizionate il logo Livefyre sulla pagina.

Se l&#39;accordo con Livefyre lo consente, potete spostare il logo Livefyre dalla parte superiore del flusso di contenuto verso il basso.

Ad esempio, aggiungete il seguente HTML alla pagina immediatamente dopo l&#39;elemento che contiene l&#39;app Livefyre:

```
<div id="powered_by_livefyre_new"><a href="https://livefyre.com" target="_blank">Powered by Livefyre</a></div>
```

Quindi, aggiungere quanto segue al foglio di stile della pagina:

```
/* Hide the top logo */ 
.fyre-widget .fyre-logo-drop, .fyre-widget .fyre-logo-help, .fyre-widget .fyre-help { 
    display:none !important; 
} 
  
/* Style the bottom logo */ 
#powered_by_livefyre_new a {    background: url(https://cdn.livefyre.com/libs/fyre.conv/v3.0.0/images/poweredbylivefyre.png) no-repeat left top; 
    display: block; 
    height: 24px; 
    font: 13px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
    text-decoration: none; 
    color: #404040; 
    padding-left: 28px; 
    padding-top: 4px; 
} 
#powered_by_livefyre_new a:hover { 
    text-decoration: underline; 
}
```

