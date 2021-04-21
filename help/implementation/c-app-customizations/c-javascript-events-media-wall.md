---
description: Utilizza gli eventi JavaScript per ascoltare gli eventi che si verificano in una bacheca di contenuti multimediali e inviarli allo strumento di analisi desiderato.
title: Eventi JavaScript per Media Wall
exl-id: 3fe76467-65e2-4f8b-bd75-5a2ffc3e7e15
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---

# Eventi JavaScript per Media Wall{#javascript-events-for-media-wall}

Utilizza gli eventi JavaScript per ascoltare gli eventi che si verificano in una bacheca di contenuti multimediali e inviarli allo strumento di analisi desiderato.

Livefyre fornisce eventi JavaScript per monitorare l’attività dell’utente nelle app Livefyre. Ad esempio, puoi aggiornare la pagina quando gli utenti amano o condividono contenuti su Twitter o Facebook o quando vengono pubblicati nuovi contenuti.

Ecco un esempio di come ricevere gli eventi. Sostituisci `console.log` con il codice per mappare e inviare l’evento alla tua integrazione di analytics (Dynamic Tag Management, Adobe Analytics JS, Google Analytics, ecc.):

```
document.body.addEventListener('insights', function (data) { 
 console.log('Received:', data.detail.type, data); 
});
```

Elenco degli eventi Media Wall supportati:

## Eventi muri multimediali

| Evento | Definizione |
|---|---|
| `Init` | Quando una Media Wall è inclusa in una pagina. |
| `Load` | Quando Media Wall è stato caricato su una pagina indipendentemente dalla posizione. |
| `PostButtonClick` | Quando un utente fa clic su un pulsante Carica su una parete di supporto. |
| `RequestMore` | Quando l&#39;utente carica più contenuto in una Media Wall. |
| `TwitterReplyClick` | Quando un utente fa clic sul pulsante Risposta di Twitter dalla Media Wall. |
| `TwitterRetweetClick` | Quando un utente fa clic sul pulsante Twitter Retweet dalla Media Wall. |
| `TwitterLikeClick` | Quando un utente fa clic sul pulsante Mi piace/Preferito di Twitter dalla Media Wall. |
| `ModalView` | Quando l&#39;utente fa clic per visualizzare il contenuto di Media Wall in una finestra modale più grande. |
| `Like` | Quando un utente fa clic sul pulsante Mi piace dalla Media Wall. |
| `ShareButtonClick` | Ogni volta che un utente fa clic sul pulsante di condivisione su una scheda Media Wall. |
| `ShareURL` | Quando Share to URL text area (Condividi su area di testo URL) viene selezionato/copiato dalla Media Wall. |
| `ShareFacebook` | Quando si fa clic su Condividi su Facebook da Media Wall. |
| `ShareTwitter` | Quando si fa clic su Condividi su Twitter da Media Wall. |
