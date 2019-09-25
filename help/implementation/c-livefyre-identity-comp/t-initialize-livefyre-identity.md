---
description: Il pacchetto Livefyre.js Auth garantisce che tutti i componenti social sulla pagina possano scoprire un'unica integrazione di autenticazione.
seo-description: Il pacchetto Livefyre.js Auth garantisce che tutti i componenti social sulla pagina possano scoprire un'unica integrazione di autenticazione.
seo-title: Inizializza identità Livefyre
title: Inizializza identità Livefyre
uuid: 9365d827-2734-4a84-bfe7-9be573b2b03e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Inizializza identità Livefyre{#initialize-livefyre-identity}

Il pacchetto Livefyre.js Auth garantisce che tutti i componenti social sulla pagina possano scoprire un'unica integrazione di autenticazione.

Livefyre fornisce un `lfep-auth-delegate` pacchetto che renderà un delegato di autenticazione appropriato. All'autenticazione deve essere fornito un oggetto AuthDelegate che sappia come eseguire le azioni di autenticazione, come login e logout.

1. Aggiungi Livefyre.js alla tua pagina Web.
1. Per indicare ad Auth di delegare queste azioni all'identità Livefyre, aggiungi quanto segue:

   ```
   Livefyre.require([ 
     'livefyre-auth', 
     'identity' 
     ], function (auth, Identity) { 
       var identity = new Identity({ 
         app: "https://identity.livefyre.com/{networkName}.fyre.co" 
       }); 
    auth.delegate( identity ); 
    });
   ```
