---
description: I clienti che usano Janrain Capture e Backplane possono utilizzare l'autenticazione
  Livefyre (SSO) per consentire agli utenti di coinvolgere immediatamente Livefyre
  Apps quando accedono al tuo sito.
seo-description: I clienti che usano Janrain Capture e Backplane possono utilizzare
  l'autenticazione Livefyre (SSO) per consentire agli utenti di coinvolgere immediatamente
  Livefyre Apps quando accedono al tuo sito.
seo-title: Janrain Capture/Backplane
solution: Experience Manager
title: Janrain Capture/Backplane
uuid: 776 e 9626-db 04-4 c 34-adfe -681 a 71 b 552 c 5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Janrain Capture/Backplane{#janrain-capture-backplane}

I clienti che usano Janrain Capture e Backplane possono utilizzare l'autenticazione Livefyre (SSO) per consentire agli utenti di coinvolgere immediatamente Livefyre Apps quando accedono al tuo sito.

Per sfruttare l'integrazione incorporata di Capture/Backplane, dovete apportare modifiche alla configurazione sia all'app Capture che alla vostra integrazione di Livefyre. js.

>[!NOTE]
>
>Ignorate questa sezione se non state utilizzando Janrain Capture.

Per ulteriori informazioni, consulta [la documentazione di Backplane di Janrain](https://developers.janrain.com/how-to/integrations/self-serve-integrations-and-tools/backplane-1-2/).

1. [Configurare Capture.](#c_janrain_capture_backplane/section_r2f_kxt_bbb)
1. (Facoltativo) [Aggiungi Livefyre Defaults all'app Capture](#c_janrain_capture_backplane/section_z2s_txt_bbb).
1. [Creare l'oggetto authdelegate.](#c_janrain_capture_backplane/section_asv_vyt_bbb)
1. [Sincronizza in Livefyre con Ping per Pull.](#c_janrain_capture_backplane/section_ilv_bzt_bbb)

## Passaggio 1: Impostazione acquisizione {#section_r2f_kxt_bbb}

Livefyre richiede determinate credenziali dall'app Janrain Capture.

1. Configurare l'app Janrain Capture.
1. Raccolte di Livefyre:

   * Accesso all'istanza di Janrain Capture.
   * Accesso al dashboard Partecipazione ad Janrain.
   * Le impostazioni di acquisizione e le credenziali.
   * Your Engagement credentials.
   * L'URL dell'identità.

>[!NOTE]
>
>Livefyre riceve i dati direttamente dal CNAME; pertanto, questo URL identità non può essere un record cname (CNAME personalizzato personalizzato) che viene risolto nel CNAME reale di Janrain Capture.

## Passaggio 2: (Facoltativo) Aggiungi Livefyre Defaults all'app Capture {#section_z2s_txt_bbb}

Aggiungete Livefyre per impostazione predefinita agli utenti memorizzati nell'app Capture per consentire agli utenti di inviare notifiche e-mail o di seguire automaticamente le conversazioni su cui gli utenti hanno fatto riferimento.

1. Completamento [1: Configurare Capture](#c_janrain_capture_backplane/section_r2f_kxt_bbb).
1. Aggiungete i seguenti campi predefiniti di Livefyre. Tutti i campi sono facoltativi.

| Parametro | Tipo | Descrizione |
|---|---|---|
| **[!UICONTROL livefyre_comments]** | Stringa | Informare l'utente quando un utente commenta un articolo in cui si trovano. Può essere immediatamente, spesso o mai. |
| **[!UICONTROL livefyre_likes]** | Stringa | Informate l'utente quando qualcuno ama uno dei loro post. Può essere immediatamente, spesso o mai. |
| **[!UICONTROL livefyre_replies]** | Stringa | Informare l'utente quando qualcuno risponde a uno dei suoi post. Può essere immediatamente, spesso o mai. |
| **[!UICONTROL livefyre_moderator_comments]** | Stringa | Informate moderatore quando qualcuno commenta una conversazione che stanno moderando. Può essere immediatamente, spesso o mai. |
| **[!UICONTROL livefyre_moderator_flags]** | Stringa | Informate moderatore quando un utente contrassegna un post su una conversazione che stanno moderando. Può essere immediato, spesso o mai. |
| **[!UICONTROL livefyre_autofollow_conversations]** | Booleano | Chiedete all'utente di seguire una conversazione quando lasciate un post. Può essere true o false. |

## Passaggio 3: Creare l'oggetto authdelegate per l'integrazione con Janrain {#section_asv_vyt_bbb}

Livefyre. require fornisce un plug-plugin che consente all'autenticazione di ascoltare l'autobus Janrain Backplane.

### Login {#login}

Quando viene trasmesso un messaggio di identità/login sul canale Backplane, auth. authenticate () verrà chiamato con il token di autenticazione Livefyre dell'utente. Dovete comunque implementare un authdelegate.

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
>L'oggetto window. Backplane deve essere definito sulla pagina prima della chiamata di autenticazione. plugin con il plug-plugin di Livefyre Backplane. Per verificare che l'oggetto Backplane sia disponibile, chiamate il codice di istanza di Livefyre da una callback onready. Rivolgersi al contatto Janrain per determinare quando altre applicazioni possono utilizzare l'oggetto Backplane.



>[!NOTE]
>
>Il delegato di autenticazione varia a seconda dell'istanza Janrain.

Di seguito sono riportati alcuni esempi di come un delegato di autenticazione potrebbe cercare un'integrazione Janrain Capture.

* `errback`: Callback passato al metodo di login di autenticazione dell'autenticazione
* `janrain`: Riferimento alla variabile di acquisizione Janrain.
* `window.Backplane`: Un riferimento all'oggetto Backplane.

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

### Disconnessione {#logout}

* `finishLogout`: Callback passato al metodo di login di autenticazione dell'autenticazione.

* `window.Backplane`: Un riferimento all'oggetto Backplane.

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

Questo collegamento può essere collegato a qualsiasi parte del sito che desiderate venga visitata dagli utenti per visualizzare la propria pagina del profilo. Questo esempio stampa semplicemente l'oggetto di authoring trasmesso.

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

Come Edit Profile (Modifica profilo), questo collegamento deve essere collegato alla pagina di un utente diversa da quella attualmente registrata. Questo può essere implementato in base alle esigenze. Questo esempio collega semplicemente il parametro autore alla console.

```
/** 
* View profile function 
* @param user - User or userId whose profile should be displayed 
*/ 
authDelegate.viewProfile = function(user) { 
   console.log(author); 
};
```

## Passaggio 4: Sincronizzazione con Livefyre con Ping for Pull for Janrain Integration {#section_ilv_bzt_bbb}

Mantenere i profili remoti Livefyre sincronizzati con il sistema di gestione degli utenti di acquisizione implica una serie di passaggi denominata Ping per Pull. Questo processo richiede che venga ottenuto un token di accesso valido da Janrain, quindi passalo a un endpoint specificato al punto 3, di seguito.

1. Ottenete un codice di accesso da Janrain.

   Per ottenere il codice di accesso, fornite le credenziali necessarie, specificate l'utente_ type come «utente» e il uuid come uuid dell'utente corrente da aggiornare. Per ulteriori informazioni, consultate [https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/](https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/).

1. Trade the access code for an access token. Fornite le credenziali necessarie, il codice di accesso ricevuto dal passaggio 1, quindi specificate grant_ type come «permission_ code».

   Per ulteriori informazioni, consultate [https://developers.janrain.com/rest-api/methods/authentication/oauth/token/](https://developers.janrain.com/rest-api/methods/authentication/oauth/token/).

1. Attiva l'endpoint di Livefyre «Ping to Pull Capture».

   URL endpoint: [!DNL https://{networkName}/api/v1.1/private/capture/profile_updated/?jrtoken={token}] dove ***{networkname}*** è il nome di rete fornito da Livefyre, e il token è il token ricevuto da Janrain al passaggio 2.

   Una volta raggiunto questo endpoint, riceverete una risposta 202 e Livefyre inizia un processo asincrono.

## Come funziona tutto {#concept_mty_f31_2cb}

Per sfruttare l'integrazione incorporata di Capture/Backplane, dovete apportare alcune modifiche alla configurazione sia all'app Capture che alla vostra integrazione di Livefyre. js.

Janrain invia i messaggi di accesso/disconnessione mediante il bus Backplane, su cui l'app Livefyre, se configurata correttamente, ascolta. Questi messaggi contengono tutte le informazioni necessarie per mostrare o disconnettersi dagli utenti dell'app. Gli sviluppatori possono visualizzare i messaggi bus Backplane esaminando la scheda Rete nella console per sviluppatori del browser.

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

## Esempio di codice di logout {#section_t52_svp_mz}

Richiesta:

```
https://backplane1.janrainbackplane.com/v1.2/bus/{CUSTOMER}/channel/new?callback=Backplane.finishInit&amp;rnd=0.1057701709214598
```

Risposta:

```
Backplane.finishInit("{CHANNEL}");
```

Se tali messaggi non vengono visualizzati nelle richieste di rete, Livefyre non sarà a conoscenza dei tentativi di login/logout e quindi Livefyre non sarà in grado di integrare l'utente nell'app.
