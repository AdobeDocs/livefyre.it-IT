---
description: I clienti che utilizzano Janrain Capture e Backplane possono utilizzare Livefyre Auth per l’accesso single sign on (SSO), consentendo agli utenti di interagire immediatamente con le app Livefyre quando accedono al tuo sito.
title: Janrain Capture/Backplane
exl-id: c7e6cfef-7570-4f9c-9d2c-79f890ee5c49
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '926'
ht-degree: 1%

---

# Janrain Capture/Backplane{#janrain-capture-backplane}

I clienti che utilizzano Janrain Capture e Backplane possono utilizzare Livefyre Auth per l’accesso single sign on (SSO), consentendo agli utenti di interagire immediatamente con le app Livefyre quando accedono al tuo sito.

Per beneficiare di questa integrazione incorporata Capture/Backplane, è necessario apportare modifiche alla configurazione sia dell’app Capture che dell’integrazione con Livefyre.js.

>[!NOTE]
>
>Ignora questa sezione se non utilizzi Janrain Capture.

Per ulteriori informazioni, consulta la documentazione sul backplane di [Janrain&#39;s](https://developers.janrain.com/how-to/integrations/self-serve-integrations-and-tools/backplane-1-2/).

1. [Impostare Capture.](#c_janrain_capture_backplane/section_r2f_kxt_bbb)
1. (Facoltativo) [Aggiungi Livefyre Defaults alla tua app di acquisizione](#c_janrain_capture_backplane/section_z2s_txt_bbb).
1. [Creare l&#39;oggetto AuthDelegate.](#c_janrain_capture_backplane/section_asv_vyt_bbb)
1. [Sincronizza con Livefyre con Ping per Pull.](#c_janrain_capture_backplane/section_ilv_bzt_bbb)

## Passaggio 1: Imposta acquisizione {#section_r2f_kxt_bbb}

Livefyre ha bisogno di alcune credenziali dalla tua app Janrain Capture.

1. Imposta l’app Janrain Capture.
1. Raccogliere le seguenti informazioni per Livefyre:

   * Accedere all&#39;istanza di acquisizione Janrain.
   * Accedi al tuo dashboard di Janrain Engage.
   * Le impostazioni e le credenziali di acquisizione.
   * Le credenziali di coinvolgimento.
   * URL di identità.

>[!NOTE]
>
>Livefyre riceve i dati direttamente dal CNAME; pertanto, questo URL di identità non può essere un record CNAME (un CNAME URL personalizzato) che viene risolto nel CNAME effettivo di Janrain Capture.

## Passaggio 2: (Facoltativo) Aggiungi Livefyre Defaults alla tua app di acquisizione {#section_z2s_txt_bbb}

Aggiungi Livefyre per impostazione predefinita agli utenti memorizzati nella tua app Capture per consentirti di inviare notifiche e-mail agli utenti o di consentire loro di seguire automaticamente le conversazioni sulle quali gli utenti commentano.

1. Completa [Passaggio 1: Imposta Capture](#c_janrain_capture_backplane/section_r2f_kxt_bbb).
1. Aggiungi i seguenti campi predefiniti di Livefyre. Tutti i campi sono facoltativi.

| Parametro | Tipo | Descrizione |
|---|---|---|
| **[!UICONTROL livefyre_comments]** | Stringa | Notifica all’utente quando un utente commenta un articolo che sta seguendo. Può essere immediatamente, spesso o mai. |
| **[!UICONTROL livefyre_likes]** | Stringa | Notifica all&#39;utente quando uno dei suoi post piace a qualcuno. Può essere immediatamente, spesso o mai. |
| **[!UICONTROL livefyre_replies]** | Stringa | Informa l&#39;utente quando risponde a uno dei suoi post.Può essere immediatamente, spesso o mai. |
| **[!UICONTROL livefyre_moderator_comments]** | Stringa | Notifica al moderatore quando qualcuno commenta una conversazione che sta moderando.Può essere immediatamente, spesso o mai. |
| **[!UICONTROL livefyre_moderator_flags]** | Stringa | Notifica al moderatore quando qualcuno contrassegna un post su una conversazione che sta moderando.Può essere immediatamente, spesso o mai. |
| **[!UICONTROL livefyre_autofollow_conversations]** | Booleano | Chiedi all&#39;utente di seguire automaticamente una conversazione quando esce da un post. Può essere true o false. |

## Passaggio 3: Creare l&#39;oggetto AuthDelegate per l&#39;integrazione di Janrain {#section_asv_vyt_bbb}

Livefyre.require fornisce un plug-in che consente ad auth di ascoltare il bus Janrain Backplane.

### Login {#login}

Quando un messaggio di identità/accesso viene trasmesso sul canale Backplane, auth.authenticate() verrà chiamato con il token di autenticazione Livefyre dell’utente. Devi ancora implementare un AuthDelegate.

```
Livefyre.require(['auth', 'backplane-auth-plugin#0'], function(auth, backplanePluginFactory) { 
   auth.plugin(backplanePluginFactory('network.fyre.co')); 
   auth.delegate({ 
      login: function (finishLogin) { 
         loginWithCapture(finishLogin); 
      } 
   }); 
});
```

>[!NOTE]
>
>L&#39;oggetto window.Backplane deve essere definito sulla pagina prima di richiamare auth.plugin con il plug-in Backplane Livefyre. Per assicurarti che l&#39;oggetto Backplane sia disponibile, chiama il codice di creazione dell&#39;istanza Livefyre da un callback onReady . Consultare il contatto Janrain per determinare quando altre applicazioni possono utilizzare l&#39;oggetto Backplane.



>[!NOTE]
>
>Il tuo delegato di autenticazione varierà a seconda della tua istanza Janrain.

Di seguito sono riportati alcuni esempi di come un delegato di autenticazione può cercare un&#39;integrazione di Janrain Capture.

* `errback`: Il callback passato al metodo di login del tuo delegato di autenticazione
* `janrain`: Il riferimento alla variabile di acquisizione Janrain.
* `window.Backplane`: Riferimento all&#39;oggetto Backplane.

```
/** 
* Login function 
* In this case, opens a login modal and triggers Backplane to start listening 
* for login messages 
*/ 
authDelegate.login = function(finishLogin) { 
   var successCallback = function() { 
      // These need to be replaced with the actions that correspond to successful login  
      // and when the Janrain modal is closed. 
      janrain.events.onCaptureLoginSuccess.removeHandler(successCallback); 
      janrain.events.onModalClose.removeHandler(failureCallback); 
      finishLogin(); 
   }; 
  
   var failureCallback = function(e) { 
      janrain.events.onModalClose.removeHandler(failureCallback); 
      janrain.events.onCaptureLoginSuccess.removeHandler(successCallback); 
      finishLogin(e || new Error("Error logging in with Janrain Capture")); 
   }; 
  
   // Open the modal to log a user in 
   janrain.capture.ui.renderScreen('signIn'); 
   // Send a backplane message 
   window.Backplane.expectMessages('identity/login'); 
   // Add handlers to specific janrain events 
   janrain.events.onCaptureLoginSuccess.addHandler(successCallback); 
   janrain.events.onModalClose.addHandler(failureCallback); 
};
```

### Logout {#logout}

* `finishLogout`: Il callback passato al metodo di login del tuo delegato di autenticazione.

* `window.Backplane`: Riferimento all&#39;oggetto Backplane.

```
/** 
* Logout function 
* In this case, invalidates the session and removes the cookie. 
* Also reloads the page to change state. In order to do this without a reload, 
* it would be necessary to also update the UI. 
*/ 
authDelegate.logout = function(finishLogout) { 
   Backplane.resetCookieChannel(); 
   janrain.capture.ui.endCaptureSession(); 
   finishLogout(); 
}; 
```

### Modifica profilo {#editprofile}

Questo può essere collegato a qualsiasi parte del sito che desideri che gli utenti visitano per visualizzare la propria pagina del profilo. In questo esempio viene semplicemente stampato l&#39;oggetto autore passato.

```
/** 
* Edit profile function 
* @param user - User who would like to edit their profile 
*/ 
authDelegate.editProfile = function(user) { 
   console.log(user); 
}; 
```

### Visualizza profilo {#viewprofile}

Come Modifica profilo, questo deve essere collegato a una pagina di un utente diversa dall’utente attualmente connesso. Questo può essere implementato come lo ritieni opportuno. In questo esempio il parametro autore viene semplicemente registrato nella console.

```
/** 
* View profile function 
* @param user - User or userId whose profile should be displayed 
*/ 
authDelegate.viewProfile = function(user) { 
   console.log(author); 
};
```

## Passaggio 4: Sincronizzazione con Livefyre con Ping per l&#39;integrazione con Janrain {#section_ilv_bzt_bbb}

Mantenere i profili remoti Livefyre sincronizzati con il sistema di gestione degli utenti Capture comporta una serie di passaggi denominati Ping for Pull. Questo processo richiede che venga ottenuto un token di accesso valido da Janrain, quindi lo si passi a un endpoint specificato al punto 3, qui sotto.

1. Ottieni un codice di accesso da Janrain.

   Per ottenere il codice di accesso, fornisci le credenziali necessarie, specifica user_type come &quot;user&quot; e l’uuid come uuid dell’utente corrente da aggiornare. Per ulteriori informazioni, consulta [https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/](https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/).

1. Scambiare il codice di accesso per un token di accesso. Immetti le credenziali necessarie, il codice di accesso ricevuto dal passaggio 1 e specifica il tipo_sovvenzione come &quot;codice_autorizzazione&quot;.

   Per ulteriori informazioni, consulta [https://developers.janrain.com/rest-api/methods/authentication/oauth/token/](https://developers.janrain.com/rest-api/methods/authentication/oauth/token/).

1. Colpire l’endpoint &quot;Ping to Pull Capture&quot; di Livefyre.

   URL endpoint: [!DNL https://{networkName}/api/v1.1/private/capture/profile_updated/?jrtoken={token}] dove ***{networkName}*** è il nome di rete fornito da Livefyre e il jrtoken è il token ricevuto da Janrain al passaggio 2.

   Una volta raggiunto questo endpoint, si riceve una risposta 202 e Livefyre inizia un processo asincrono.

## Come funziona tutto {#concept_mty_f31_2cb}

Per usufruire di questa integrazione incorporata Capture/Backplane, è necessario apportare alcune modifiche alla configurazione sia dell’app Capture che dell’integrazione con Livefyre.js.

Janrain invia messaggi di login/logout riusciti tramite il bus Backplane, sul quale viene ascoltata l’app Livefyre, se configurata correttamente. Questi messaggi contengono tutte le informazioni necessarie per mostrare agli utenti dell&#39;app come connessi o disconnessi. Gli sviluppatori possono visualizzare i messaggi degli autobus Backplane controllando la scheda Rete nella console per sviluppatori del browser.

## Esempio di codice di accesso {#section_ftt_tvp_mz}

Richiesta:

```
https://backplane1.janrainbackplane.com//bus/{CUSTOMER_NAME}/channel/{CHANNEL}?callback=Backplane.response&rnd=0.15930617856793106
```

Risposta:

```
Backplane.response([{ 
  "id": "2014-05-06T22:51:55.406Z-eZp1HB1F7B", 
  "channel_name": "{CHANNEL_NAME}", 
  "message": { 
    "source": "https://{CUSTOMER_DOMAIN}", 
    "type": "identity/login", 
    "sticky": true, 
    "payload": { 
      "context": "https://{CUSTOMER_DOMAIN}", 
      "identities": { 
        "startIndex": 0, 
        "itemsPerPage": 1, 
        "totalResults": 1, 
        "entry": { 
          "id": "https://{CUSTOMER}.janraincapture.com/oauth/public_profile?uuid={UNIQUE_USER_ID}", 
          "displayName": "{USER_DISPLAY_NAME}", 
          "accounts": [ 
            { 
              "username": "{USER_DISPLAY_NAME}", 
              "identityUrl": "https://{CUSTOMER}.janraincapture.com/oauth/public_profile?uuid={UNIQUE_USER_ID}", 
              "photos": [ 
                { 
                  "id": 48570146, 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "other" 
                }, 
                { 
                  "id": 48570147, 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "original" 
                }, 
                { 
                  "id": 48570148, 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "large" 
                }, 
                { 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "avatar" 
                } 
              ] 
            }, 
            { 
              "identityUrl": "{USER_PROFILE_LINK}" 
            } 
          ] 
        } 
      } 
    } 
  } 
} 
]);
```

Risposta vuota:

```
Backplane.response([]);
```

## Esempio di codice di disconnessione {#section_t52_svp_mz}

Richiesta:

```
https://backplane1.janrainbackplane.com/v1.2/bus/{CUSTOMER}/channel/new?callback=Backplane.finishInit&amp;rnd=0.1057701709214598
```

Risposta:

```
Backplane.finishInit("{CHANNEL}");
```

Se questi messaggi non compaiono nelle richieste di rete, Livefyre non sarà a conoscenza dei tentativi di accesso/logout e, pertanto, Livefyre non sarà in grado di integrare l’utente nell’app.
