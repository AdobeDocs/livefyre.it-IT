---
description: Installate il pacchetto di autenticazione per abilitare l'autenticazione utente in modo che gli utenti possano interagire con le vostre app.
seo-description: Installate il pacchetto di autenticazione per abilitare l'autenticazione utente in modo che gli utenti possano interagire con le vostre app.
seo-title: Pacchetto di autenticazione
solution: Experience Manager
title: Pacchetto di autenticazione
uuid: 4eec30cf-66b6-408d-985d-3e23b8b70d01
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Pacchetto di autenticazione{#authentication-package}

Installate il pacchetto di autenticazione per abilitare l'autenticazione utente in modo che gli utenti possano interagire con le vostre app.

Le app Livefyre utilizzano il pacchetto di autenticazione globale per associare gli utenti alle azioni dell'app. Il pacchetto di autenticazione è disponibile tramite `Livefyre.require`.

Per abilitare l’autenticazione sulla pagina, aggiungete prima `Livefyre.js` l’ `<head>` elemento della pagina Web o del modello di sito Web.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

L'utilizzo di Livefyre.request per abilitare l'autenticazione è simile all'utilizzo dell'obbligo di chiamare altri pacchetti. Il codice di integrazione necessario per l’autenticazione è simile al seguente:

```
Livefyre.require(['auth'], function (auth) {  
// Perform action... 
});
```

## Metodi {#section_ojx_1lz_fz}

Una volta incluso come sopra `Livefyre.require`, il modulo Auth espone i seguenti metodi che potete chiamare per notificare ad altre app sulla pagina gli eventi correlati all'autenticazione.

| Metodo | Descrizione |
|--- |--- |
| `.login(callback)` | Attiva il flusso di login come implementato dal AuthDelegate registrato. Generalmente solo le app abilitate all'autenticazione lo chiameranno, e non la pagina host stessa. |
| `.logout(callback)` | Notifica all'utente finale che ha eseguito il logout con alcuni mezzi esterni e che tutte le app attendibili devono cancellare il proprio stato di autenticazione fino al login successivo. In questo modo verrà cancellata la sessione interna gestita da Auth. |
| `.authenticate(credentials)` | Notifica all'autenticazione che un utente è stato autenticato con mezzi esterni e che è stato acquistato un token di autenticazione Livefyre per l'utente finale. Utilizzate questa opzione se impostate un cookie con il token Livefyre o se disponete di un token per l'utente e desiderate accedere in modo esplicito all'utente. Ad esempio: <br>`auth.authenticate({&nbsp;livefyre:&nbsp;`<br>`'<insert&nbsp;lftoken&nbsp;string&nbsp;for&nbsp;newly&nbsp;logged-in&nbsp;user>'&nbsp;});` |
| `.delegate(authDelegate)` | Delegare i dettagli di implementazione dell'autenticazione (ad esempio, il flusso di autenticazione personalizzato) a un oggetto definito dall'utente. Questo deve essere chiamato dalla pagina host per abilitare le funzionalità interattive delle app Livefyre. |

