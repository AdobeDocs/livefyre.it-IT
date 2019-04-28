---
description: Installate il pacchetto di autenticazione per abilitare l'autenticazione degli utenti in modo che gli utenti possano interagire con le vostre app.
seo-description: Installate il pacchetto di autenticazione per abilitare l'autenticazione degli utenti in modo che gli utenti possano interagire con le vostre app.
seo-title: Pacchetto di autenticazione
solution: Experience Manager
title: Pacchetto di autenticazione
uuid: 4 eec 30 cf -66 b 6-408 d -985 d -3 e 23 b 8 b 70 d 01
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Pacchetto di autenticazione{#authentication-package}

Installate il pacchetto di autenticazione per abilitare l&#39;autenticazione degli utenti in modo che gli utenti possano interagire con le vostre app.

Livefyre Apps utilizza il pacchetto di autenticazione globale per associare gli utenti alle azioni app. Il pacchetto di autenticazione è `Livefyre.require`disponibile.

Per abilitare l&#39;autenticazione sulla pagina, aggiungete `Livefyre.js` innanzitutto all&#39; `<head>` elemento della pagina Web o del modello di sito Web.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

L&#39;utilizzo di Livefyre. require per abilitare l&#39;autenticazione è simile a quello richiesto per richiamare altri pacchetti. Il codice di integrazione per richiedere l&#39;autenticazione è simile al seguente:

```
Livefyre.require(['auth'], function (auth) {  
// Perform action... 
});
```

## Metodi {#section_ojx_1lz_fz}

Una volta incluso come descritto sopra, `Livefyre.require`il modulo Autenticazione espone i metodi seguenti che puoi chiamare per inviare ad altre app sulla pagina gli eventi relativi all&#39;autenticazione.

| Metodo | Descrizione |
|--- |--- |
| `.login(callback)` | Attiva il flusso di accesso implementato dall&#39;authdelegate registrato. In genere, solo le app abilitate all&#39;autenticazione chiameranno questa e non la pagina host stessa. |
| `.logout(callback)` | Notifica all&#39;utente che l&#39;utente finale ha disconnesso alcuni mezzi esterni e che tutte le app assegnano il proprio stato di autenticazione al successivo login. Ciò cancella la sessione interna gestita da Autenticazione. |
| `.authenticate(credentials)` | Notifica all&#39;autenticazione che un utente è stato autenticato con alcuni mezzi esterni e un token di autenticazione Livefyre è stato ottenuto per l&#39;utente finale. Utilizzate questa azione se impostate un cookie con il token Livefyre, oppure disponete di un token per l&#39;utente e desiderate registrare esplicitamente l&#39;utente in. Ad esempio: <br>`auth.authenticate({&nbsp;livefyre:&nbsp;`<br>`'<insert&nbsp;lftoken&nbsp;string&nbsp;for&nbsp;newly&nbsp;logged-in&nbsp;user>'&nbsp;});` |
| `.delegate(authDelegate)` | Delega i dettagli di implementazione dell&#39;autenticazione (ad esempio, il flusso di autenticazione personalizzato) a un oggetto definito dall&#39;utente. Questo deve essere invocato dalla pagina ospitante per abilitare le funzionalità interattive di Livefyre Apps. |

