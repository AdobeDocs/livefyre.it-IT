---
description: Il pacchetto Auth di Livefyre. js garantisce che tutti i componenti social presenti nella pagina rilevino un'integrazione con l'autenticazione singola.
seo-description: Il pacchetto Auth di Livefyre. js garantisce che tutti i componenti social presenti nella pagina rilevino un'integrazione con l'autenticazione singola.
seo-title: Inizializza Livefyre Identity
title: Inizializza Livefyre Identity
uuid: 9365 d 827-2734-4 a 84-bfe 7-9 be 573 b 2 b 03 e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Inizializza Livefyre Identity{#initialize-livefyre-identity}

Il pacchetto Auth di Livefyre. js garantisce che tutti i componenti social presenti nella pagina rilevino un&#39;integrazione con l&#39;autenticazione singola.

Livefyre fornisce un `lfep-auth-delegate` pacchetto che farà riferimento a un&#39;autenticazione appropriata. All&#39;autenticazione deve essere fornito un oggetto authdelegate che sappia come eseguire azioni di autenticazione, come login e logout.

1. Aggiungete Livefyre. js alla vostra pagina Web.
1. Per dire all&#39;autenticazione di delegare queste azioni a Livefyre Identity, aggiungere quanto segue:

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
