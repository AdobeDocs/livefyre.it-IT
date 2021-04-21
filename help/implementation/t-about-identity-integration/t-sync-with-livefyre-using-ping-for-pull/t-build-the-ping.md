---
description: Crea il ping in modo che la tua pagina faccia ping a Livefyre quando gli utenti aggiornano il loro profilo.
title: Creare il ping
exl-id: 626c200b-eaff-483f-b1eb-7d8993fe5e7c
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---

# Crea il ping{#build-the-ping}

Crea il ping in modo che la tua pagina faccia ping a Livefyre quando gli utenti aggiornano il loro profilo.

Quando Livefyre riceve una notifica di aggiornamento con `networkName` e `user_id`, il sistema invia una richiesta di pull al tuo Ping per l’URL di pull.

>[!NOTE]
>
>403/Not Authorized in risposta al tuo Ping indica un `lftoken` non valido aggiunto alla richiesta Ping. Assicurati che il `lftoken` sia per un `user_id` con privilegi di proprietario della rete o per l&#39;utente del sistema. Se utilizzi librerie Livefyre, utilizza il metodo `buildLivefyreToken` per generare un token di sistema valido per la richiesta.

1. Aggiungi il codice alla tua pagina che invia il ping a Livefyre quando gli utenti aggiornano il loro profilo. Crea l’URL in questo modo:

   ```
   POSThttps://{networkName}.quill.fyre.co/api/v3.0/user/{user_id}/refresh?lftoken={token}
   ```

   * **[!UICONTROL networkName:]** Il nome di rete fornito da Livefyre.
   * **[!UICONTROL user_id:]** L’ID dell’utente.
   * **[!UICONTROL token:]** Token di sistema valido.

1. Recupera la struttura della richiesta.
