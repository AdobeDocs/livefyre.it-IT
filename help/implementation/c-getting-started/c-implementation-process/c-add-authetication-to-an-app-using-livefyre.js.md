---
description: Utilizza Livefyre.js per aggiungere l’autenticazione a livello di pagina per le tue app Livefyre.
title: Aggiungere l’autenticazione a un’app tramite Livefyre.js
exl-id: 6246a2bc-e7ff-4f86-a63a-36261c71d460
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Aggiungere l&#39;autenticazione a un&#39;app utilizzando Livefyre.js{#add-authetication-to-an-app-using-livefyre-js}

Utilizza Livefyre.js per aggiungere l’autenticazione a livello di pagina per le tue app Livefyre.

`Livefyre.js Aut`h è un pacchetto JavaScript sviluppato da Livefyre che consente a tutte le app sul tuo sito web di condividere un&#39;unica integrazione di autenticazione. Auth consente di definire le modalità di registrazione, accesso e disconnessione degli utenti delegando questi flussi a un oggetto AuthDelegate definito dall’utente.

## Passaggio 1: Abilita autenticazione per una pagina {#section_pgp_jtt_bbb}

Utilizza `Livefyre.js` per abilitare l’autenticazione per una pagina al fine di consentire agli utenti di accedere e interagire con le app utilizzando il tuo sistema di autenticazione esistente.

1. Per abilitare l’autenticazione su una pagina, aggiungi `Livefyre.js` all’elemento *&lt;head>* della pagina web o del modello di sito web.

   ```
   <script src="//cdn.livefyre.com/Livefyre.js"></script>
   ```

1. Utilizza `Livefyre.require` per abilitare l’autenticazione. L&#39;utilizzo di `Livefyre.require` è simile all&#39;utilizzo di need per chiamare altri pacchetti. Il codice di integrazione per richiedere l’autenticazione si presenta così:

   ```
   Livefyre.require(['auth'], function (auth) { // Do authy things...});
   ```

## Passaggio 2: Registra un delegato Auth {#section_oqm_15t_bbb}

Per abilitare l&#39;autenticazione, crea un `AuthDelegate` e passalo all&#39;autenticazione `Livefyre.js`.

Un `AuthDelegate` è un oggetto definito che determina il modo in cui gli utenti effettueranno l’accesso, disconteranno e visualizzeranno i profili.

1. Crea un `AuthDelegate`. Il modo in cui si crea un `AuthDelegate` dipende dal provider di identità. Per istruzioni più dettagliate, consulta Integrazione di identità .

1. Passa l&#39;autenticazione `AuthDelegate` a `Livefyre.js`. Il `AuthDelegate` più semplice registra lo stesso utente in ogni volta che un utente ha attivato il metodo di login delegato da un&#39;app:

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

Sincronizza le informazioni sul profilo utente tra Livefyre e il provider di identità.

Devi sincronizzare le informazioni sul tuo profilo utente tra Livefyre e il tuo provider di identità. Per ulteriori informazioni, consulta [Integrazione di acquisizione Janrain](/help/implementation/c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md).
