---
description: Configurate le credenziali che consentono agli utenti di condividere i contenuti su vari social network.
seo-description: Configurate le credenziali che consentono agli utenti di condividere i contenuti su vari social network.
seo-title: Abilitazione della condivisione per social network
solution: Experience Manager
title: Abilitazione della condivisione per social network
uuid: f584a0ae-46c7-48c1-aea4-36da9f1e259b
translation-type: tm+mt
source-git-commit: d77b633b9892e3ea4aaec860317887f1fdf66830
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 0%

---


# Abilitazione della condivisione per social network {#enabling-social-sharing}

Configurate le credenziali che consentono agli utenti di condividere i contenuti su vari social network.

Per consentire agli utenti di condividere contenuti tra siti di social media, implementate la funzione di condivisione per social network di Livefyre e create un sistema OAuth per fornire l&#39;autenticazione corretta a tali siti. Con questo sistema, Livefyre agisce per conto dell’utente quando questi sceglie di condividere contenuti tramite social media.

>[!NOTE]
>
>Diversi provider hanno requisiti OAuth diversi. Consultate i vostri fornitori per acquisire le informazioni associate alla loro implementazione di OAuth.

## Credenziali necessarie {#section_gff_cjm_b1b}

Se utilizzate un sistema di identità utente personalizzato, dovete fornire le vostre credenziali social per consentire agli utenti di condividere su Twitter, Facebook o LinkedIn da un&#39;app Livefyre.

>[!NOTE]
>
>I clienti che utilizzano Janrain Engage devono fornire solo il proprio Engage Domain (Dominio di coinvolgimento) e la chiave API Engage (Chiave API di coinvolgimento).

Usate il pannello Impostazioni integrazione del Admin Console di  per immettere o aggiornare le seguenti credenziali per social network.

### Credenziali richieste:

* **Reindirizzamento proxy OAuth segreto client ID** FacebookClient
* **Segreto API chiave** LinkedInAPI
* **Segreto API segreto di accesso token di** TwitterAccess

## Twitter {#section_qp5_1yl_b1b}

Le credenziali Twitter sono disponibili dal dashboard di Twitter App. Per trovare le credenziali seguenti:

* Apri [pagina sviluppatore app di Twitter](https://dev.twitter.com/apps) come proprietario dell&#39;app, trova l&#39;applicazione e fai clic sul titolo.
* Scorrete verso il basso fino a &quot;Token di accesso&quot; e acquisite i valori da &quot;Token di accesso&quot; e &quot;Segreto token di accesso&quot;.

È necessario:

* Immettete un valore per il campo URL per il callback nell’app Twitter. Anche se questo campo può essere un semplice segnaposto, non può essere lasciato vuoto.
* Impostate il tipo di applicazione in modo che sia possibile accedere **read** e **write**.
* Confermate che l&#39;URL del sito Web dell&#39;app Twitter sia nello stesso dominio host dell&#39;app Livefyre Core.

>[!NOTE]
>
>Tutte le applicazioni che visualizzano contenuto Twitter sono necessarie per soddisfare i requisiti di visualizzazione. Per ulteriori informazioni, vedere le [Linee guida per la visualizzazione su Twitter](https://dev.twitter.com/terms/display-requirements).

## LinkedIn {#section_lfz_zxl_b1b}

Le credenziali LinkedIn sono disponibili dalla sezione Chiavi OAuth delle chiavi API dell&#39;applicazione LinkedIn.

* Accedi al tuo account dalla pagina degli sviluppatori di LinkedIn [https://developer.linkedin.com/](https://developer.linkedin.com/).
* Passa il mouse sul tuo nome in alto a destra, quindi seleziona Chiavi API dal menu a discesa.
* Fate clic sul titolo Applicazione.
* Acquisite i valori Chiave API e Chiave segreta dalla sezione Chiavi OAuth

## Facebook {#section_zyb_gpl_b1b}

Le credenziali Facebook sono disponibili dalla pagina App per sviluppatori.

* Aprite la pagina delle app per sviluppatori di [Facebook](https://developers.facebook.com/apps) come proprietario dell&#39;app, individuate l&#39;applicazione e fate clic sul titolo.
* Acquisite i valori per ID app e Segreto app. Per Segreto app, potrebbe essere necessario fare clic sul pulsante Mostra per visualizzarlo.

La condivisione su Facebook richiede l&#39;impostazione di una pagina di reindirizzamento per soddisfare le richieste di Facebook e le pratiche di dominio richieste da [Facebook](https://developers.facebook.com/docs/reference/dialogs/oauth/). La pagina deve essere ospitata nel tuo dominio in modo che Facebook possa verificare che la richiesta provenga da un&#39;origine legittima.

### Reindirizzamento Facebook

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

### Python

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

Per impostazione predefinita, i pulsanti Facebook, LinkedIn e &quot;Post to&quot; di Twitter sono visualizzati nelle applicazioni Livefyre Core. Utilizzate il parametro postToButtons per configurare quali fornitori verranno visualizzati quando si incorpora l&#39;app Livefyre.

```
var convConfig = {}; // Ignoring other options for this example 
convConfig.postToButtons = ['tw', 'fb', 'li']; // Or any subset of these 
fyre.conv.load(networkConfig, [convConfig], function() {}); 
```

`postToButtons` è un array con qualsiasi sottoinsieme delle seguenti opzioni:

* tw: Twitter
* fb: Facebook
* li: LinkedIn
