---
description: Registra l’endpoint URL in modo che Livefyre possa usare l’URL per richiamare le informazioni di profilo aggiornate.
seo-description: Registra l’endpoint URL in modo che Livefyre possa usare l’URL per richiamare le informazioni di profilo aggiornate.
seo-title: Registra l'endpoint con Studio
solution: Experience Manager
title: Registra l'endpoint con Studio
uuid: 4eb816ee-d743-43bf-bfee-d9b9fd98b482
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Registra l'endpoint con Studio{#register-the-endpoint-with-studio}

Registra l’endpoint URL in modo che Livefyre possa usare l’URL per richiamare le informazioni di profilo aggiornate.

Registra il ping per l’URL pull una sola volta per rete. Una volta impostato, questo valore non deve essere modificato a meno che l'endpoint per il recupero dei dati del profilo utente dal sistema di gestione utenti non venga modificato.

1. Utilizzate Studio per registrare l'endpoint URL con Livefyre.
1. Registra l'URL dal quale Livefyre recupererà le informazioni aggiornate sul profilo utente, passa a **[!UICONTROL Studio > Settings > Integration Settings > Remote Profiles]** e immetti il campo nel **[!UICONTROL Ping for Pull URL]** .

   Ad esempio, l’URL può essere: `https://example.yoursite.com/some_path/?id={id}`

