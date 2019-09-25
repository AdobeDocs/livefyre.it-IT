---
description: Utilizzate gli eventi Javascript per ascoltare gli eventi che si verificano in un Media Wall e inviarli allo strumento di analisi di vostra scelta.
seo-description: Utilizzate gli eventi Javascript per ascoltare gli eventi che si verificano in un Media Wall e inviarli allo strumento di analisi di vostra scelta.
seo-title: Eventi JavaScript per Media Wall
solution: Experience Manager
title: Eventi JavaScript per Media Wall
uuid: 8afc0529-4640-476a-b207-91b2c70101f0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Eventi JavaScript per Media Wall{#javascript-events-for-media-wall}

Utilizzate gli eventi Javascript per ascoltare gli eventi che si verificano in un Media Wall e inviarli allo strumento di analisi di vostra scelta.

Livefyre fornisce eventi JavaScript per monitorare l'attività degli utenti nelle app Livefyre. Ad esempio, potete decidere di aggiornare la pagina quando gli utenti desiderano o condividono contenuti su Twitter o Facebook, oppure quando vengono pubblicati nuovi contenuti.

Di seguito è riportato un esempio di come ricevere gli eventi. Sostituisci `console.log` con il codice per mappare e inviare l’evento alla tua integrazione con Analytics (Gestione tag dinamica, Adobe Analytics JS, Google Analytics, ecc.):

```
document.body.addEventListener('insights', function (data) { 
 console.log('Received:', data.detail.type, data); 
});
```

Elenco degli eventi Media Wall supportati:

## Eventi di Media Wall

| Evento | Definizione |
|---|---|
| `Init` | Quando una Media Wall è inclusa in una pagina. |
| `Load` | Quando Media Wall è stato caricato su una pagina, indipendentemente dalla posizione. |
| `PostButtonClick` | Quando un utente fa clic su un pulsante di caricamento su una bacheca multimediale. |
| `RequestMore` | Quando un utente carica più contenuto in una Media Wall. |
| `TwitterReplyClick` | Quando un utente fa clic sul pulsante Rispondi su Twitter dal Media Wall. |
| `TwitterRetweetClick` | Quando un utente fa clic sul pulsante Retweet di Twitter dal Media Wall. |
| `TwitterLikeClick` | Quando un utente fa clic sul pulsante Mi piace/Preferito di Twitter nella Media Wall. |
| `ModalView` | Quando l'utente fa clic per visualizzare il contenuto di Media Wall in una finestra modale più grande. |
| `Like` | Quando un utente fa clic sul pulsante Mi piace da Media Wall. |
| `ShareButtonClick` | Ogni volta che un utente fa clic sul pulsante Condividi su una scheda Media Wall. |
| `ShareURL` | Quando l’opzione Condividi su area di testo URL è selezionata/copiata da Media Wall. |
| `ShareFacebook` | Quando si fa clic su Condividi su Facebook dal Media Wall. |
| `ShareTwitter` | Quando si fa clic su Condividi su Twitter dal Media Wall. |
