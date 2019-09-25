---
description: I clienti che utilizzano Janrain Capture e Backplane possono utilizzare Livefyre Auth per Single Sign On (SSO), consentendo agli utenti di interagire immediatamente con le app Livefyre al momento dell'accesso al sito.
seo-description: I clienti che utilizzano Janrain Capture e Backplane possono utilizzare Livefyre Auth per Single Sign On (SSO), consentendo agli utenti di interagire immediatamente con le app Livefyre al momento dell'accesso al sito.
seo-title: Janrain Capture/Backplane
solution: Experience Manager
title: Janrain Capture/Backplane
uuid: 776e9626-db04-4c34-adfe-681a71b552c5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Janrain Capture/Backplane{#janrain-capture-backplane}

I clienti che utilizzano Janrain Capture e Backplane possono utilizzare Livefyre Auth per Single Sign On (SSO), consentendo agli utenti di interagire immediatamente con le app Livefyre al momento dell'accesso al sito.

Per trarre vantaggio da questa integrazione incorporata Capture/Backplane, è necessario apportare modifiche alla configurazione sia dell'app Capture che dell'integrazione Livefyre.js.

>[!NOTE]
>
>Ignora questa sezione se non utilizzi Janrain Capture.

Per ulteriori informazioni, consulta la documentazione [di](https://developers.janrain.com/how-to/integrations/self-serve-integrations-and-tools/backplane-1-2/)Janrain sul piano posteriore.

1. [Configurare Capture.](#c_janrain_capture_backplane/section_r2f_kxt_bbb)
1. (Facoltativo) [Aggiungi Livefyre predefinito all’app](#c_janrain_capture_backplane/section_z2s_txt_bbb)di acquisizione.
1. [Creare l'oggetto AuthDelegate.](#c_janrain_capture_backplane/section_asv_vyt_bbb)
1. [Sincronizza con Livefyre con Ping per pull.](#c_janrain_capture_backplane/section_ilv_bzt_bbb)

## Passaggio 1: Imposta acquisizione {#section_r2f_kxt_bbb}

Livefyre necessita di alcune credenziali dall’app Janrain Capture.

1. Configurate l’app Janrain Capture.
1. Raccogliete le seguenti informazioni per Livefyre:

   * Accesso all'istanza di Janrain Capture.
   * Accesso al dashboard di Janrain Engage.
   * Le impostazioni e le credenziali di acquisizione.
   * Le tue credenziali di coinvolgimento.
   * L’URL dell’identità.

>[!NOTE]
>
>Livefyre riceve i dati direttamente dal CNAME; pertanto, questo URL di identità non può essere un record CNAMEd (un CNAME URL personalizzato) che viene risolto nel CNAME effettivo di Janrain Capture.

## Passaggio 2: (Facoltativo) Aggiungi Livefyre predefinito all’app di acquisizione {#section_z2s_txt_bbb}

Per impostazione predefinita, Aggiungi Livefyre agli utenti memorizzati nella tua app Capture consente di inviare agli utenti notifiche e-mail o di seguire automaticamente le conversazioni alle quali gli utenti possono aggiungere commenti.

1. Completa [il passaggio 1: Configurare Capture](#c_janrain_capture_backplane/section_r2f_kxt_bbb).
1. Aggiungete i seguenti campi predefiniti di Livefyre. Tutti i campi sono facoltativi.

| Parametro | Tipo | Descrizione |
|---|---|---|
| **[!UICONTROL livefyre_comments]** | Stringa | Informate l'utente quando un utente commenta un articolo che sta seguendo. Può essere immediatamente, spesso o mai. |
| **[!UICONTROL livefyre_likes]** | Stringa | Informare l'utente quando a qualcuno piace uno dei suoi post. Può essere immediatamente, spesso o mai. |
| **[!UICONTROL livefyre_replies]** | Stringa | Informare l'utente quando un utente risponde a uno dei suoi post.Può essere immediatamente, spesso o mai. |
| **[!UICONTROL livefyre_moderator_comments]** | Stringa | Informare il moderatore quando qualcuno commenta una conversazione che sta moderando.Può essere immediatamente, spesso o mai. |
| **[!UICONTROL livefyre_moderator_flags]** | Stringa | Informare il moderatore quando qualcuno contrassegna un post in una conversazione che sta moderando.Può essere immediatamente, spesso o mai. |
| **[!UICONTROL livefyre_autofollow_conversations]** | Booleano | Chiedi all’utente di seguire automaticamente una conversazione quando abbandona un post. Può essere vero o falso. |

## Passaggio 3: Creare l'oggetto AuthDelegate per l'integrazione di Janrain {#section_asv_vyt_bbb}

Livefyre.request fornisce un plugin che consente all'auth di ascoltare il bus Janrain Backplane.

### Login {#login}

Quando un messaggio di identità/login viene trasmesso sul canale Backplane, auth.authenticate() verrà chiamato con il token di autenticazione Livefyre dell'utente. Devi ancora implementare un AuthDelegate.

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
>L'oggetto window.Backplane deve essere definito sulla pagina prima di chiamare auth.plugin con il plug-in Livefyre Backplane. Per essere certi che l'oggetto Backplane sia disponibile, chiamate il codice di creazione dell'istanza Livefyre da un callback onReady. Consultate il contatto di Janrain per determinare quando altre applicazioni possono utilizzare l'oggetto Backplane.



>[!NOTE]
>
>Il delegato di autenticazione varia a seconda dell’istanza di Janrain.

Di seguito sono riportati alcuni esempi di come un delegato audio potrebbe cercare un'integrazione di Janrain Capture.

* `errback`: Callback passato al metodo di login del delegato di autenticazione
* `janrain`: Il riferimento alla variabile di acquisizione Janrain.
* `window.Backplane`: Riferimento all'oggetto Backplane.

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

* `finishLogout`: Il callback passato al metodo di login del delegato dell’autenticazione.

* `window.Backplane`: Riferimento all'oggetto Backplane.

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

Questo può essere collegato a qualsiasi parte del sito che desideri che gli utenti visitino per visualizzare la propria pagina del profilo. In questo esempio viene semplicemente stampato l'oggetto autore passato.

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

Come Edit Profile (Modifica profilo), questo collegamento deve essere collegato a una pagina dell'utente diversa dall'utente attualmente connesso. Questa funzione può essere implementata a seconda delle esigenze. In questo esempio il parametro author viene semplicemente registrato nella console.

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

Mantenere sincronizzati i profili remoti Livefyre con il sistema di gestione degli utenti Capture richiede una serie di passaggi definiti come Ping for Pull. Questo processo richiede che venga ottenuto un token di accesso valido da Janrain, quindi che tale token venga passato a un endpoint specificato al punto 3, di seguito.

1. Ricevi un codice di accesso da Janrain.

   Per ottenere il codice di accesso, fornite le credenziali necessarie, specificate user_type come "user" e l'uuuid come ID dell'utente corrente da aggiornare. Per ulteriori informazioni, consultate [https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/](https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/).

1. Scambiare il codice di accesso per un token di accesso. Fornire le credenziali necessarie, il codice di accesso ricevuto dal passaggio 1 e specificare il tipo di sovvenzione come "authorized_code".

   Per ulteriori informazioni, consultate [https://developers.janrain.com/rest-api/methods/authentication/oauth/token/](https://developers.janrain.com/rest-api/methods/authentication/oauth/token/).

1. Premete l’endpoint "Ping to Pull Capture" di Livefyre.

   URL endpoint: [!DNL https://{networkName}/api/v1.1/private/capture/profile_updated/?jrtoken={token}] dove ***{networkName}*** è il nome di rete fornito da Livefyre, e il token jrtoken è il token ricevuto da Janrain nel passaggio 2.

   Una volta raggiunto questo endpoint, riceverete una risposta di 202 e Livefyre avvia un processo asincrono.

## How It All Works {#concept_mty_f31_2cb}

Per trarre vantaggio da questa integrazione incorporata Capture/Backplane, è necessario apportare alcune modifiche alla configurazione sia dell'app Capture che dell'integrazione Livefyre.js.

Janrain invia messaggi di login/logout con esito positivo tramite il bus Backplane, sul quale l'app Livefyre, se configurata correttamente, ascolta. Questi messaggi contengono tutte le informazioni necessarie per mostrare agli utenti dell'app l'accesso o la disconnessione. Gli sviluppatori possono visualizzare i messaggi del bus Backplane controllando la scheda Rete nella console sviluppatore del browser.

## Esempio di codice di login {#section_ftt_tvp_mz}

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

Se questi messaggi non vengono visualizzati nelle richieste di rete, Livefyre non sarà a conoscenza dei tentativi di login/logout e pertanto Livefyre non sarà in grado di integrare l'utente nell'app.
