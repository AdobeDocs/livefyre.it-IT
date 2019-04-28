---
description: Utilizzate eventi Javascript per ascoltare eventi che si verificano in un Media Wall e inviarli allo strumento di analisi desiderato.
seo-description: Utilizzate eventi Javascript per ascoltare eventi che si verificano in un Media Wall e inviarli allo strumento di analisi desiderato.
seo-title: Eventi Javascript per Media Wall
solution: Experience Manager
title: Eventi Javascript per Media Wall
uuid: 8 afc 0529-4640-476 a-b 207-91 b 2 c 70101 f 0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Eventi Javascript per Media Wall{#javascript-events-for-media-wall}

Utilizzate eventi Javascript per ascoltare eventi che si verificano in un Media Wall e inviarli allo strumento di analisi desiderato.

Livefyre fornisce eventi javascript per tenere traccia dell&#39;attività utente nelle app di Livefyre. Ad esempio, potrebbe essere utile aggiornare la pagina quando gli utenti hanno o condividono contenuti su Twitter o Facebook oppure quando si pubblicano nuovi contenuti.

Esempio di come ricevere gli eventi. Sostituisci `console.log` con il tuo codice per mappare e inviare l&#39;evento all&#39;integrazione di Analytics (Gestione tag dinamica, Adobe Analytics JS, Google Analytics, ecc.):

```
document.body.addEventListener('insights', function (data) { 
 console.log('Received:', data.detail.type, data); 
});
```

Elenco degli eventi di Media Wall supportati:

## Eventi per contenuti multimediali

| Evento | Definizione |
|---|---|
| `Init` | Quando una Media Wall è inclusa in una pagina. |
| `Load` | Quando Media Wall è stato caricato su una pagina, a prescindere dalla posizione. |
| `PostButtonClick` | Quando un utente fa clic su un pulsante di caricamento su un Media Wall. |
| `RequestMore` | Quando l&#39;utente carica più contenuto in un Media Wall. |
| `TwitterReplyClick` | Quando un utente fa clic sul pulsante di risposta Twitter da Media Wall. |
| `TwitterRetweetClick` | Quando un utente fa clic sul pulsante Twitter Retweet dal Media Wall. |
| `TwitterLikeClick` | Quando un utente fa clic sul pulsante su Twitter o Preferito da Media Wall. |
| `ModalView` | Quando l&#39;utente fa clic per visualizzare il contenuto di Media Wall in una finestra modale più grande. |
| `Like` | Quando un utente fa clic sul pulsante Like (Simili) da Media Wall. |
| `ShareButtonClick` | Ogni volta che un utente fa clic sul pulsante condiviso su una scheda Media Wall. |
| `ShareURL` | Quando l&#39;area di testo Condividi su URL è selezionata o copiata da Media Wall. |
| `ShareFacebook` | Quando viene fatto clic su Condividi su Facebook, dal Media Wall. |
| `ShareTwitter` | Quando viene fatto clic su Condividi su Twitter, dal Media Wall. |
