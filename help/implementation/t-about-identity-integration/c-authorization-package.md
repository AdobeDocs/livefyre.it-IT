---
description: Installa il pacchetto di autenticazione per abilitare l'autenticazione degli utenti in modo che gli utenti possano interagire con le tue app.
title: Pacchetto di autenticazione
exl-id: 639032ee-ed7d-4cb0-83ba-f11d3dc607b6
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 1%

---

# Pacchetto di autenticazione{#authentication-package}

Installa il pacchetto di autenticazione per abilitare l&#39;autenticazione degli utenti in modo che gli utenti possano interagire con le tue app.

Le app Livefyre utilizzano il pacchetto di autenticazione globale per associare gli utenti alle azioni App. Il pacchetto di autenticazione è disponibile tramite `Livefyre.require`.

Per abilitare l’autenticazione sulla pagina, aggiungi prima `Livefyre.js` all’elemento `<head>` della pagina web o del modello di sito web.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

L&#39;utilizzo di Livefyre.require per abilitare auth è simile all&#39;utilizzo di need per chiamare altri pacchetti. Il codice di integrazione per richiedere l’autenticazione si presenta così:

```
Livefyre.require(['auth'], function (auth) {  
// Perform action... 
});
```

## Metodi {#section_ojx_1lz_fz}

Una volta incluso come sopra utilizzando `Livefyre.require`, il modulo Auth espone i seguenti metodi che è possibile chiamare per notificare ad altre app sulla pagina gli eventi relativi all&#39;autenticazione.

| Metodo | Descrizione |
|--- |--- |
| `.login(callback)` | Attiva il flusso di accesso come implementato da AuthDelegate registrato. Di solito solo le app abilitate per l&#39;autenticazione lo chiameranno e non la pagina host stessa. |
| `.logout(callback)` | Comunica all’utente finale che si è disconnesso con alcuni mezzi esterni e che tutte le app fidelizzate devono cancellare il loro stato di autenticazione fino al successivo accesso. Questo eliminerà la sessione interna gestita da Auth. |
| `.authenticate(credentials)` | Notifica ad Auth che un utente ha eseguito l’autenticazione con alcuni mezzi esterni e che per l’utente finale è stato acquistato un token di autenticazione Livefyre. Utilizza questa opzione se imposti un cookie con il token Livefyre o se disponi di un token per l’utente e desideri accedere in modo esplicito all’utente. Ad esempio: <br>`auth.authenticate({&nbsp;livefyre:&nbsp;`<br>`'<insert&nbsp;lftoken&nbsp;string&nbsp;for&nbsp;newly&nbsp;logged-in&nbsp;user>'&nbsp;});` |
| `.delegate(authDelegate)` | Delega i dettagli di implementazione dell’autenticazione (ad esempio, il flusso di autenticazione personalizzato) a un oggetto definito dall’utente. Questo deve essere chiamato dalla pagina host per abilitare le funzionalità interattive delle app Livefyre. |
