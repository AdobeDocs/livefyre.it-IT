---
description: Utilizzate Livefyre.js per aggiungere l'autenticazione a livello di pagina per le app Livefyre.
seo-description: Utilizzate Livefyre.js per aggiungere l'autenticazione a livello di pagina per le app Livefyre.
seo-title: Aggiungere l'autenticazione a un'app tramite Livefyre.js
solution: Experience Manager
title: Aggiungere l'autenticazione a un'app tramite Livefyre.js
uuid: b7c61e07-e341-45d7-9112-c50155e38f1d
translation-type: tm+mt
source-git-commit: a6aebcc14325632cab0415e4aa4a24fda8a19bfc
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---


# Aggiunta dell&#39;autenticazione a un&#39;app tramite Livefyre.js{#add-authetication-to-an-app-using-livefyre-js}

Utilizzate Livefyre.js per aggiungere l&#39;autenticazione a livello di pagina per le app Livefyre.

`Livefyre.js Aut`h è un pacchetto JavaScript sviluppato da Livefyre che consente a tutte le app del sito Web di condividere un&#39;unica integrazione di autenticazione. Auth consente di definire il modo in cui gli utenti devono registrarsi, effettuare l’accesso e disconnettersi delegando questi flussi a un oggetto AuthDelegate definito dall’utente.

## Passaggio 1: Abilita autenticazione per una pagina {#section_pgp_jtt_bbb}

Utilizzate `Livefyre.js` per abilitare l&#39;autenticazione per una pagina al fine di consentire agli utenti di accedere e interagire con le app utilizzando il sistema di autenticazione esistente.

1. Per abilitare l&#39;autenticazione su una pagina, aggiungere `Livefyre.js` all&#39;elemento *&lt;head>* della pagina Web o del modello di sito Web.

   ```
   <script src="//cdn.livefyre.com/Livefyre.js"></script>
   ```

1. Utilizzate `Livefyre.require` per abilitare l&#39;autenticazione. L&#39;utilizzo di `Livefyre.require` è simile all&#39;utilizzo dell&#39;opzione Richiedi di chiamare altri pacchetti. Il codice di integrazione necessario per l’autenticazione è simile al seguente:

   ```
   Livefyre.require(['auth'], function (auth) { // Do authy things...});
   ```

## Passaggio 2: Registra un delegato di autenticazione {#section_oqm_15t_bbb}

Per abilitare l&#39;autenticazione, creare un `AuthDelegate` e passarlo all&#39;autenticazione `Livefyre.js`.

Un `AuthDelegate` è un oggetto definito che determina in che modo gli utenti accederanno, disconnetteranno e visualizzeranno i profili.

1. Crea un `AuthDelegate`. Il modo in cui si crea un `AuthDelegate` dipende dal provider di identità. Consulta Integrazione identità per istruzioni più dettagliate.

1. Passa l&#39;autenticazione `AuthDelegate` a `Livefyre.js`. La `AuthDelegate` più semplice registra lo stesso utente ogni volta che un utente ha attivato il metodo di login delegato da un&#39;app:

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

Sincronizzate le informazioni sul profilo utente tra Livefyre e il vostro provider di identità.

Dovete sincronizzare le informazioni del vostro profilo utente tra Livefyre e il vostro provider di identità. Per ulteriori informazioni, vedere [Integrazione acquisizione protetta](/help/implementation/c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md).
