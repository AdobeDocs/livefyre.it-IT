---
description: Utilizzate Livefyre. js per aggiungere l'autenticazione a livello di pagina alle app Livefyre.
seo-description: Utilizzate Livefyre. js per aggiungere l'autenticazione a livello di pagina alle app Livefyre.
seo-title: Aggiungere Authetication a un'app utilizzando Livefyre. js
solution: Experience Manager
title: Aggiungere Authetication a un'app utilizzando Livefyre. js
uuid: b 7 c 61 e 07-e 341-45 d 7-9112-c 50155 e 38 f 1 d
translation-type: tm+mt
source-git-commit: a6aebcc14325632cab0415e4aa4a24fda8a19bfc

---


# Aggiungere autenticazione a un&#39;app utilizzando Livefyre. js{#add-authetication-to-an-app-using-livefyre-js}

Utilizzate Livefyre. js per aggiungere l&#39;autenticazione a livello di pagina alle app Livefyre.

`Livefyre.js Aut`h è un pacchetto javascript sviluppato da Livefyre che consente a tutte le app del sito Web di condividere una singola integrazione dell&#39;autenticazione. L&#39;autenticazione consente di definire il modo in cui gli utenti devono registrarsi, eseguire il login ed uscire delegando questi flussi a un oggetto authdelegate definito dall&#39;utente.

## Passaggio 1: Abilita autenticazione per una pagina {#section_pgp_jtt_bbb}

Utilizzate `Livefyre.js` per abilitare l&#39;autenticazione per una pagina per consentire agli utenti di accedere e interagire con le app utilizzando il sistema di autenticazione esistente.

1. Per abilitare l&#39;autenticazione su una pagina, aggiungete `Livefyre.js` all&#39;elemento *&lt; head &gt;* del modello Web o della pagina Web.

   ```
   <script src="//cdn.livefyre.com/Livefyre.js"></script>
   ```

1. Utilizzate `Livefyre.require` per abilitare l&#39;autenticazione. L&#39;utilizzo è `Livefyre.require` simile all&#39;utilizzo di richieste per richiamare altri pacchetti. Il codice di integrazione per richiedere l&#39;autenticazione è simile al seguente:

   ```
   Livefyre.require(['auth'], function (auth) { // Do authy things...});
   ```

## Passaggio 2: Registrare un authdelegate {#section_oqm_15t_bbb}

Per abilitare l&#39;autenticazione, create un e `AuthDelegate` passatelo all `Livefyre.js` &#39;autenticazione.

Un `AuthDelegate` oggetto è un oggetto definito che determina in che modo gli utenti possono accedere, disconnettersi e visualizzare i profili.

1. Creare un `AuthDelegate`. La modalità di creazione dipende `AuthDelegate` dal provider di identità. Consultate Integrazione identità per istruzioni più dettagliate.

1. Passa l&#39; `AuthDelegate``Livefyre.js` autenticazione. Più semplice `AuthDelegate` accede allo stesso utente quando un utente attiva il metodo di accesso delegato da un&#39;app:

   ```
   Livefyre.require(['auth'], function (auth) { 
      auth.delegate({ 
         login: function (errback) { 
            errback(null, { livefyre: '<userAuthToken>' }); 
         }    
      });  
   });
   ```

## Passaggio 3: Sincronizza dati utente {#section_u4m_j5t_bbb}

Sincronizzate le informazioni sul profilo utente tra Livefyre e il provider di identità.

Dovete sincronizzare le informazioni sul profilo utente tra Livefyre e il provider di identità. Per ulteriori informazioni, consultate [Integrazione con Janrain Capture](/help/implementation/c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md).
