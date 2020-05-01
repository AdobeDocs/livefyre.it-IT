---
description: Crea il ping in modo che la tua pagina possa scorrere Livefyre quando gli utenti aggiornano il loro profilo.
seo-description: Crea il ping in modo che la tua pagina possa scorrere Livefyre quando gli utenti aggiornano il loro profilo.
seo-title: Creare il ping
solution: Experience Manager
title: Creare il ping
uuid: cb8cc043-9ea5-407c-b70f-3f1e37accdae
translation-type: tm+mt
source-git-commit: f76dcd31e58b94856bf551009c2ac50c3233e516

---


# Creare il ping{#build-the-ping}

Crea il ping in modo che la tua pagina possa scorrere Livefyre quando gli utenti aggiornano il loro profilo.

Quando Livefyre riceve una notifica di aggiornamento con `networkName` e, `user_id`il sistema invia una richiesta pull al Ping per l’URL pull.

>[!NOTE]
>
>403/Non autorizzato in risposta al Ping indica che alla richiesta Ping è `lftoken` stato aggiunto un valore non valido. Assicurarsi che `lftoken` sia per un utente `user_id` con privilegi di proprietario della rete o l&#39;utente del sistema. Se utilizzate le librerie Livefyre, utilizzate il `buildLivefyreToken` metodo per generare un token di sistema valido per la richiesta.

1. Aggiungete alla pagina del codice che collega Livefyre quando gli utenti aggiornano il loro profilo. Create l’URL in questo modo:

   ```
   POSThttps://{networkName}.quill.fyre.co/api/v3.0/user/{user_id}/refresh?lftoken={token}
   ```

   * **[!UICONTROL networkName:]** Il nome di rete fornito da Livefyre.
   * **[!UICONTROL user_id:]** L’ID dell’utente.
   * **[!UICONTROL token:]** Token di sistema valido.

1. Estrarre la struttura della richiesta.
