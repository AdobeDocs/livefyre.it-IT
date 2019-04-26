---
description: Configurate le credenziali che consentono agli utenti di condividere
  contenuti in diverse reti social.
seo-description: Configurate le credenziali che consentono agli utenti di condividere
  contenuti in diverse reti social.
seo-title: Abilitazione della condivisione per social network
solution: Experience Manager
title: Abilitazione della condivisione per social network
uuid: f 584 a 0 ae -46 c 7-48 c 1-aea 4-36 da 9 f 1 e 259 b
translation-type: tm+mt
source-git-commit: d77b633b9892e3ea4aaec860317887f1fdf66830

---


# Abilitazione della condivisione per social network {#enabling-social-sharing}

Configurate le credenziali che consentono agli utenti di condividere contenuti in diverse reti social.

Per consentire agli utenti di condividere contenuto tra i siti social media, implementate la funzionalità di condivisione social network di Livefyre e create un sistema oauth per fornire l'autenticazione corretta a tali siti. Con questo sistema, Livefyre agisce a nome dell'utente quando sceglie di condividere contenuti tramite social media.

>[!NOTE]
>
>I diversi fornitori hanno requisiti oauth diversi. Consultate i fornitori per acquisire le informazioni associate alla loro implementazione di oauth.

## Credenziali social richieste {#section_gff_cjm_b1b}

Se utilizzate un sistema di identità utente personalizzato, dovete fornire le credenziali social per consentire agli utenti di condividere su Twitter, Facebook o linkedin da un'app Livefyre.

>[!NOTE]
>
>I clienti che usano Janrain Coinvolgono possono fornire solo il proprio dominio di coinvolgimento e coinvolgere la chiave API.

Utilizzate il pannello Impostazioni integrazione di Admin Console per immettere o aggiornare le seguenti credenziali social.

### Credenziali richieste:

* **Reindirizzamento** proxy oauth Client Client ID segreto Facebook
* **Segreto API chiave** API linkedin
* **Segreto API segreto API segreto di Twitter** Access API Segreto

## Twitter {#section_qp5_1yl_b1b}

Le credenziali Twitter sono disponibili dal dashboard di app Twitter. Per trovare queste credenziali:

* Aprite [l'App Dev Designer di Twitter](https://dev.twitter.com/apps) come titolare dell'app, individuate l'applicazione e fate clic sul titolo.
* Scorrete verso il basso fino a «Token di accesso» e acquisite i valori da «Accesso di accesso» e «Segreto di accesso». »»

Devi:

* Immettete un valore per il campo URL richiamata nell'app Twitter. Anche se questo campo può essere un segnaposto semplice, non può essere lasciato vuoto.
* Impostate Tipo applicazione per disporre di accesso **in lettura** e **scrittura** .
* Confermate che l'URL del sito Web di Twitter sia nello stesso dominio host dell'app di base di Livefyre.

>[!NOTE]
>
>Tutte le applicazioni che visualizzano contenuto Twitter devono soddisfare i requisiti di visualizzazione. Per ulteriori [informazioni, consultare le Linee guida](https://dev.twitter.com/terms/display-requirements) sulla visualizzazione Twitter.

## Linkedin {#section_lfz_zxl_b1b}

Le credenziali linkedin sono disponibili dalla sezione oauth Keys delle chiavi API dell'applicazione linkedin.

* Accedi al tuo account dalla pagina degli sviluppatori di linkedin [https://developer.linkedin.com/](https://developer.linkedin.com/).
* Posiziona il cursore sul nome in alto a destra, quindi seleziona Chiavi API dal menu a discesa.
* Fate clic sul titolo dell'applicazione.
* Acquisire i valori Chiave API e Chiave segreta dalla sezione Oauth Keys

## Facebook {#section_zyb_gpl_b1b}

Le credenziali Facebook sono disponibili dalla pagina App per sviluppatori.

* Aprite [la pagina App Sviluppatore di Facebook](https://developers.facebook.com/apps) come titolare dell'app, individuate l'applicazione e fate clic sul titolo.
* Acquisite i valori per App ID e Segreto app. Per Segreto app, potrebbe essere necessario fare clic sul pulsante Mostra per visualizzarlo.

La condivisione su Facebook richiede che venga impostata una pagina di reindirizzamento per effettuare richieste Facebook e aderire alle pratiche del dominio richieste [da Facebook](https://developers.facebook.com/docs/reference/dialogs/oauth/). La pagina deve essere ospitata sul dominio in modo che Facebook possa verificare che la richiesta sia venuta da un'origine valida.

### Reindirizzamento Facebook

La pagina in hosting deve includere il seguente codice:

### Ruby

Questo è un esempio che utilizza Ruby e Rails per eseguire il reindirizzamento di Facebook oauth.

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

### Python

Questo è un esempio che utilizza Python e Django per eseguire il reindirizzamento a Facebook oauth.

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

### Nodejs

Questo è un esempio che utilizza nodejs e Sail/Express per eseguire il reindirizzamento a Facebook oauth.

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

Questo è un esempio che utilizza i controller Java e Spring per eseguire il reindirizzamento di Facebook oauth.

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

## Configurazione di «Post in» Fornitori {#section_rdk_dpl_b1b}

Per impostazione predefinita, le applicazioni di base di Facebook, linkedin e Twitter sono visualizzate nelle applicazioni di base di Livefyre. Utilizzate il parametro posttobuttons per configurare i fornitori che verranno visualizzati durante l'incorporazione dell'app Livefyre.

```
var convConfig = {}; // Ignoring other options for this example 
convConfig.postToButtons = ['tw', 'fb', 'li']; // Or any subset of these 
fyre.conv.load(networkConfig, [convConfig], function() {}); 
```

`postToButtons` è un array con qualsiasi sottoinsieme delle seguenti opzioni:

* tw: Twitter
* fb: Facebook
* li: Linkedin
