---
description: Imposta le credenziali che consentono agli utenti di condividere i contenuti in vari social network.
title: Abilitazione della condivisione social
exl-id: 08ac9766-52ea-432f-8b4f-bf68cb8b62bc
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 0%

---

# Abilitazione della condivisione social network {#enabling-social-sharing}

Imposta le credenziali che consentono agli utenti di condividere i contenuti in vari social network.

Per consentire agli utenti di condividere contenuti tra siti di social media, implementa la funzione di condivisione social network di Livefyre e crea un sistema OAuth per fornire un’autenticazione adeguata a questi siti. Con questo sistema, Livefyre agisce per conto dell’utente quando sceglie di condividere contenuti tramite i social media.

>[!NOTE]
>
>Diversi provider hanno requisiti OAuth diversi. Consulta i tuoi provider per acquisire le informazioni associate alla loro implementazione di OAuth.

## Credenziali necessarie {#section_gff_cjm_b1b}

Se utilizzi un sistema di identità utente personalizzato, devi fornire le tue credenziali social per consentire agli utenti di condividere con Twitter, Facebook o LinkedIn da un’app Livefyre.

>[!NOTE]
>
>I clienti che utilizzano Janrain Engage devono solo fornire il proprio Engage Domain e Engage API Key.

Utilizza il pannello Impostazioni integrazione di Admin Console per immettere o aggiornare le seguenti credenziali social.

### Credenziali richieste:

* **** Reindirizzamento del proxy OAuth segreto client ID FacebookClient
* **Segreto API chiave** LinkedInAPI
* **** Segreto API chiave segreto dell’API per token di accesso token di TwitterAccess

## Twitter {#section_qp5_1yl_b1b}

Le credenziali twitter sono disponibili dal dashboard dell&#39;app Twitter. Per trovare queste credenziali:

* Apri [Twitter&#39;s App Dev Page](https://dev.twitter.com/apps) come proprietario dell&#39;app, trova l&#39;applicazione e fai clic sul titolo.
* Scorri verso il basso fino a &quot;Il tuo token di accesso&quot; e acquisisci i valori da &quot;Access token&quot; e &quot;Access token secret&quot;.

Devi:

* Immetti un valore per il campo URL di callback nell’app Twitter. Anche se questo campo può essere un segnaposto semplice, non può essere lasciato vuoto.
* Imposta il tipo di applicazione in modo che sia possibile accedere a **read** e **write**.
* Conferma che l’URL del sito web Twitter App si trovi sullo stesso dominio host dell’app Livefyre Core.

>[!NOTE]
>
>Tutte le applicazioni che visualizzano contenuti Twitter devono soddisfare i propri requisiti di visualizzazione. Per ulteriori informazioni, consulta le [Linee guida per la visualizzazione di Twitter](https://dev.twitter.com/terms/display-requirements) .

## LinkedIn {#section_lfz_zxl_b1b}

Le credenziali linkedIn sono disponibili nella sezione Chiavi OAuth delle chiavi API dell’applicazione LinkedIn.

* Accedi al tuo account dalla pagina Sviluppatori di LinkedIn [https://developer.linkedin.com/](https://developer.linkedin.com/).
* Passa il puntatore del mouse sul nome in alto a destra e seleziona Chiavi API dal menu a discesa.
* Fare clic sul titolo dell&#39;applicazione.
* Acquisisci i valori della chiave API e della chiave segreta dalla sezione Chiavi OAuth

## Facebook {#section_zyb_gpl_b1b}

Le credenziali facebook sono disponibili nella pagina App per sviluppatori .

* Apri la pagina [App per sviluppatori di Facebook](https://developers.facebook.com/apps) come proprietario dell&#39;app, trova l&#39;applicazione e fai clic sul titolo.
* Acquisisci i valori per App ID e App Secret. Per Segreto app, potrebbe essere necessario fare clic sul pulsante Mostra per visualizzarlo.

Per condividere con Facebook è necessario impostare una pagina di reindirizzamento per soddisfare le richieste Facebook e le pratiche di dominio richieste da [Facebook](https://developers.facebook.com/docs/reference/dialogs/oauth/). La pagina deve essere ospitata sul tuo dominio in modo che Facebook possa verificare che la richiesta provenga da un’origine legittima.

### Reindirizzamento facebook

La pagina in hosting deve includere il seguente codice:

### Ruby

Questo è un esempio che utilizza Ruby e Rails per eseguire il reindirizzamento OAuth di Facebook.

```ruby
require "base64" 
  
class Controller < ActionController::Base 
   def base64url_decode(str) 
      str.gsub! '-_', '+/' 
      Base64.decode64(str.ljust(str.length+str.length%4, '=')) 
   end 
  
   def index 
      lfoauth = params[:lfoauth] 
      if not lfoauth 
         render :status => :forbidden, :text => 'Missing lfoauth.' 
      end 
  
      redirect = base64url_decode lfoauth 
  
      match = /^(http:\/\/|https:\/\/)?([^\/?]+)/i.match(redirect) 
      host = match[2] 
  
         if not host.include? 'fyre.co' 
      render :status => :forbidden, :text => 'Invalid host.' 
         end 
  
         sep = (redirect.include? '?') ? '&' : '?' 
      params.delete :lfoauth 
  
         rdir = redirect + sep + params.to_query 
      redirect_to rdir 
   end 
end
```

### Pitone

Questo è un esempio che utilizza Python e Django per eseguire il reindirizzamento OAuth di Facebook.

```python
import base64, re 
from django.views.decorators.http import require_GET 
from django.http.response import HttpResponseRedirect, HttpResponseBadRequest 
  
def base64url_decode(st): 
    return base64.b64decode(re.sub("-_","+/", st).ljust(len(st)+len(st)%4, '=')) 
  
@require_GET 
def handle_lfoauth(request): 
    lfoauth = request.GET.get('lfoauth', None) 
    import pdb; pdb.set_trace() 
    if not lfoauth: 
        return HttpResponseBadRequest('Missing lfoauth.') 
     
    redirect = base64url_decode(lfoauth) 
     
    match = re.match(r"^(http:\/\/|https:\/\/)?([^\/?]+)", redirect, re.IGNORECASE) 
    host = match.group(2) 
     
    # validate the destination to secure this proxy 
    if not 'fyre.co' in host: 
        return HttpResponseBadRequest('Invalid host.') 
     
    # if params were included in the uri already, append with &, otherwise ? 
    sep = '&' if '?' in redirect else '?' 
     
    # remove lfoauth from query param 
    dict_ = request.GET.copy() 
    dict_.pop('lfoauth') 
  
    # attach remaining param to redirect 
    rdir = redirect + sep + dict_.urlencode() 
  
    # this does the actual redirection 
    return HttpResponseRedirect(rdir)
```

### NodeJS

Questo è un esempio che utilizza NodeJS e Sail/Express per eseguire il reindirizzamento OAuth di Facebook.

```nodejs
/* 
 * 
 */ 
var S = require('string'), 
     querystring = require('querystring'); 
  
var base64UrlDecode = function(str) { 
     var temp = S(str.replace('-_', '+/')).padRight(str.length+(str.length%4), '=').s 
     return new Buffer(temp, 'base64').toString('utf8'); 
} 
  
module.exports = { 
  index: function(req, res) { 
     var lfoauth = req.param('lfoauth'); 
  
     if (typeof lfoauth === 'undefined') { 
        res.send(400, 'Missing lfoauth.'); 
     } 
  
     var redirect = base64UrlDecode(lfoauth); 
  
     var match = redirect.match(/^(http:\/\/|https:\/\/)?([^\/?]+)/i); 
     var host = match[2] 
  
     if (host.indexOf('fyre.co') <= -1) { 
        res.send(400, 'Invalid host.'); 
     } 
  
     var sep = redirect.indexOf('?') > -1 ? '&' : '?'; 
  
     delete req.query['lfoauth']; 
     var rdir = redirect + sep + querystring.stringify(req.query); 
  
     res.redirect(rdir); 
  }, 
  
  _config: {} 
};
```

### Java

Questo è un esempio che utilizza i controller Java e Spring per eseguire il reindirizzamento OAuth di Facebook.

```java
/* 
 *  
 */ 
import java.util.Collection; 
import java.util.HashMap; 
import java.util.Map; 
import java.util.regex.Matcher; 
import java.util.regex.Pattern; 
  
import org.apache.commons.codec.binary.Base64; 
import org.apache.commons.lang.StringUtils; 
import org.jboss.resteasy.spi.BadRequestException; 
import org.springframework.stereotype.Controller; 
import org.springframework.web.bind.annotation.RequestMapping; 
import org.springframework.web.bind.annotation.RequestParam; 
import org.springframework.web.servlet.View; 
import org.springframework.web.servlet.view.RedirectView; 
  
@Controller 
public class RedirectController { 
    @RequestMapping("/fbredirect") 
    public View facebook(@RequestParam Map<string,object> allRequestParams) { 
        if (!allRequestParams.containsKey("lfoauth")) { 
            throw new BadRequestException("Missing lfoauth."); 
        } 
             
        String redirect = base64UrlDecode((String) allRequestParams.get("lfoauth")); 
  
        Pattern p = Pattern.compile("^(http:\\/\\/|https:\\/\\/)?([^\\/?]+)", Pattern.CASE_INSENSITIVE); 
        Matcher m = p.matcher(redirect); 
        if (!m.find() || !m.group(2).contains("fyre.co")) { 
            throw new BadRequestException("Invalid host."); 
        } 
         
        Map<string, object=""> params = new HashMap<string, object="">(allRequestParams); 
        params.remove("lfoauth"); 
        String rdir = redirect + (redirect.contains("?") ? '&' : '?') + mapToQueryString(params); 
         
        return new RedirectView(rdir); 
    } 
     
    private String base64UrlDecode(String str) { 
        return new String(Base64.decodeBase64(StringUtils.rightPad(str.replaceAll("-_", "+/"), str.length()+(str.length()%4), '='))); 
    } 
     
    private String mapToQueryString(Map<string, object=""> map) { 
        String queryparam = ""; 
        for (String key : map.keySet()) { 
            if (map.get(key) instanceof Collection) { 
                for (Object item : (Collection) map.get(key)) { 
                    queryparam = queryparam.concat(String.format("%1$s=%2$s&", key, item.toString())); 
                } 
            } else { 
                queryparam = queryparam.concat(String.format("%1$s=%2$s&", key, map.get(key).toString())); 
            } 
        } 
        return StringUtils.removeEnd(queryparam, "&"); 
    } 
}
```

### PHP

```php
<?php 
/* 
Purpose: Provide a landing page for the last step of successful oAuth 
         that is on the correct (Facebook approved) domain. 
  
Location: This file should be hosted on the same domain as your  
          Facebook App's "site url". 
  
Input Parameters:  
    - (GET) lfoauth: This should be a url-safe base64-encoded URL that  
      is the "real" final redirection URL. Livefyre sets this. 
  
      For testing purposes, this can be set to a url-safe base64-encoded  
      URL of your choosing, but the domain name must end in .fyre.co in  
      order to be considered valid. 
  
    - (GET) [all other parameters]: Any other parameters should simply  
      be passed thru on the redirection URL. If the decoded URL from "lfoauth"  
      includes querystring parameters, then the additional parameters included  
      with the initial request should be appended with "&..." 
  
Output: The response should indicate that the browser redirect (302) to the  
        "real" URL which is encoded in the "lfoauth" parameter. 
  
*/ 
  
function base64url_decode($data) { 
  return base64_decode(str_pad(strtr($data, '-_', '+/'), strlen($data) % 4, '=', STR_PAD_RIGHT)); 
} 
  
if (isset($_GET['lfoauth'])) { 
    // Warning: If implemented with non-PHP, b64 may fail because we have  
    // stripped padding (trailing ='s), to comply with Facebook parameters.   
    // The decode needs to be non-strict in this sense. 
  
    $rdir = base64url_decode($_GET['lfoauth']); 
  
    // validate the destination to secure this proxy 
    preg_match("/^(https?:\/\/)?([^\/?]+)/i", $rdir, $domain_only);    
    $host = $domain_only[2]; 
    if (!strstr($host,'fyre.co')) { 
        echo "Error - this redirection is not allowed! ".$host; 
        exit; 
    } 
  
    // if params were included in the uri already, append with &, otherwise ? 
    $sep = strstr($rdir,'?') ? '&' : '?'; 
  
    // don't include this in the params we add to the redirect url 
    unset($_GET['lfoauth']); 
  
    // assemble a new querystring from the remaining inbound GET params 
    $rdir = $rdir.$sep.http_build_query($_GET); 
  
    // this does the actual redirection, PHP's implementation is weird 
    header('Location: '.$rdir); 
} 
?>
```

## Configurazione dei provider &quot;Post to&quot; {#section_rdk_dpl_b1b}

Per impostazione predefinita, i pulsanti &quot;Post to&quot; di Facebook, LinkedIn e Twitter sono visualizzati sulle applicazioni core di Livefyre. Usa il parametro postToButtons per configurare quali provider verranno visualizzati durante l&#39;incorporazione dell&#39;app Livefyre.

```
var convConfig = {}; // Ignoring other options for this example 
convConfig.postToButtons = ['tw', 'fb', 'li']; // Or any subset of these 
fyre.conv.load(networkConfig, [convConfig], function() {}); 
```

`postToButtons` è una matrice con qualsiasi sottoinsieme delle seguenti opzioni:

* tw: Twitter
* f ter: Facebook
* li: linkedIn
