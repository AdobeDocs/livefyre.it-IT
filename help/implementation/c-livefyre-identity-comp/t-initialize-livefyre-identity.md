---
description: Il pacchetto Livefyre.js Auth assicura che tutti i componenti social sulla pagina possano scoprire una singola integrazione di autenticazione.
title: Inizializza identità Livefyre
exl-id: 9990d284-a21e-49fb-932c-62906b41484a
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# Inizializza Livefyre Identity{#initialize-livefyre-identity}

Il pacchetto Livefyre.js Auth assicura che tutti i componenti social sulla pagina possano scoprire una singola integrazione di autenticazione.

Livefyre fornisce un pacchetto `lfep-auth-delegate` che renderà un delegato di autenticazione appropriato per te. È necessario fornire all&#39;autenticazione un oggetto AuthDelegate che sappia come eseguire azioni di autenticazione, come accesso e logout.

1. Aggiungi Livefyre.js alla tua pagina web.
1. Per dire ad Auth di delegare queste azioni a Livefyre Identity, aggiungi quanto segue:

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
