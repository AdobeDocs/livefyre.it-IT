---
description: Registrate l'endpoint dell'URL in modo che Livefyre possa utilizzare
  l'URL per estrarre informazioni aggiornate sul profilo.
seo-description: Registrate l'endpoint dell'URL in modo che Livefyre possa utilizzare
  l'URL per estrarre informazioni aggiornate sul profilo.
seo-title: Registra l'endpoint con Studio
solution: Experience Manager
title: Registra l'endpoint con Studio
uuid: 4 eb 816 ee-d 743-43 bf-bfee-d 9 b 9 fd 98 b 482
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Registra l'endpoint con Studio{#register-the-endpoint-with-studio}

Registrate l'endpoint dell'URL in modo che Livefyre possa utilizzare l'URL per estrarre informazioni aggiornate sul profilo.

Registra il ping per l'URL pull solo una volta per rete. Una volta impostato, questo valore non dovrebbe cambiare a meno che non si verifichi l'endpoint per recuperare i dati del profilo utente dal sistema di gestione degli utenti.

1. Utilizzate Studio per registrare l'endpoint dell'URL con Livefyre.
1. Registrate l'URL dal quale Livefyre recupererà le informazioni aggiornate sul profilo utente, selezionatelo **[!UICONTROL Studio > Settings > Integration Settings > Remote Profiles]**e inseritelo nel **[!UICONTROL Ping for Pull URL]** campo.

   Ad esempio, l'URL può essere: `https://example.yoursite.com/some_path/?id={id}`

