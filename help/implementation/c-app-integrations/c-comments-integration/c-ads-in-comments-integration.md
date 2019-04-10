---
description: Inserire annunci nel flusso Commenti.
seo-description: Inserire annunci nel flusso Commenti.
seo-title: Annunci nei commenti
solution: Experience Manager
title: Annunci nei commenti
uuid: f 8 d 6372 f -4468-4884-a 384-116180 b 4 c 748
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Annunci nei commenti{#ads-in-comments}

Inserire annunci nel flusso Commenti.

## Annunci nei commenti {#topic_CDD2ACF16AED4DE782725EE90089C04E}

Inserire annunci nel flusso Commenti.

La funzione Livefyre Ads in Comments (Annunci) consente di inserire annunci pubblicitari nel flusso dei commenti, definire la frequenza con cui verranno visualizzati gli annunci nel flusso e creare sia i delegati sincroni che asincroni ad iniezione.

Livefyre fornisce il contenitore tramite il quale potete inserire un annuncio tramite il fornitore di gestione annunci pubblicitari.

Per inserire un annuncio, passate due valori di Livefyre:

* Frequenza in cui inserire l'annuncio nel flusso commento
* Funzione che svolge l'annuncio appropriato.

>[!NOTE]
>
>Gli annunci verranno sottoposti a rendering solo quando l'annuncio si trova nel viewport. Gli annunci verranno visualizzati solo dopo i commenti principali (non all'interno dei thread) e gli utenti non potranno commentare questi annunci pubblicitari. Questa API non consente di specificare le dimensioni dell'elemento in cui verranno inseriti gli annunci.

## Integrazione {#concept_C99029E618EC49779E3117D2C303E4F1}

Per utilizzare questa funzione, create un elemento div nella pagina in cui gli annunci verranno inseriti, quindi trasmettete l'HTML dal vostro provider di annunci.

Livefyre fornisce due tipi di posizionamento: sincrona e asincrona. Entrambi i tipi caricano gli annunci solo quando l'utente scorre la pagina in modo che la posizione dell'annuncio sia visualizzata. Entrambi devono inoltre restituire un elemento DOM (iframe o div).

Per ottenere l'annuncio, le chiamate del metodo sincrono a un archivio locale, mentre chiamate asincrone a un servizio esterno.

### Sincrona

Per creare un posizionamento sincrono, includete l'annuncio nel delegate e restituite l'elemento annuncio stesso. Le chiamate del metodo sincrono a un archivio locale, che consentono di gestire la generazione di annunci personalizzati.

### Asincrona

Il metodo asincrono richiede che l'elemento venga inserito nel DOM prima di chiamare l'annuncio. Il fornitore quindi determina quale annuncio inviare e restituisce.

Per implementare annunci asincroni, create un delegato che restituisca un elemento in cui verrà inserito l'annuncio e una callback che eseguirà il posizionamento dell'annuncio. L'elemento restituito nel delegato deve avere un ID univoco per l'annuncio a target. Il callback inserisce l'annuncio nell'elemento fornito dall'ID univoco.

>[!NOTE]
>
>A seconda del provider di annunci, il callback avrà un comportamento diverso.

Quando la pagina viene caricata, Ads in Comments (Annunci) restituirà il delegato, inserisce l'elemento, quindi chiama la callback che aggiorna l'elemento (definito in precedenza) con l'annuncio.

## Parametri {#concept_D7E27B0C21EF405C8EB826083DBB53EC}

I seguenti parametri sono disponibili per la chiamata.

Per l'oggetto annuncio:

* **delay:****(facoltativo) Numero intero** - Imposta il numero di commenti dopo il quale verrà visualizzato il primo annuncio. Il valore predefinito è 10.
* **frequenza: (facoltativo) Numero intero** - Imposta il numero di commenti dopo il quale verrà visualizzato ogni annuncio successivo. Ad esempio: Inserite 2 per visualizzare un annuncio come ogni terzo commento. Il valore predefinito è 10.
* **delegate:*****funzione richiesta*** - La funzione chiamata per inserire annunci nel flusso Commento.

L'oggetto delegate supporta chiamate ad annuncio sincrone e asincrone. Il parametro assegnato alla funzione delegate, i dati, conterrà:

* **title:****stringa** - Il titolo della raccolta.
* **tag:****array** - Un elenco di tag associati alla raccolta.
* **id:****stringa** - L'identificatore articolo della raccolta.
* **url:****stringa** - L'URL della raccolta.
* **Networkid:****stringa** - L'ID di rete per la raccolta.
* **Siteid:****int** - L'ID del sito per la raccolta.

Questi elementi vengono passati tramite l'oggetto convconfig nel nostro esempio e sono descritti più dettagliatamente [nella](/help/implementation/c-app-integrations/c-comments-integration/c-comments-integration.md#section_656AAC97903F485084650269A6C7EBCE) sezione Guida introduttiva.

### Sincrona

Il delegato restituisce un oggetto contenente:

* **elemento:*****elemento* DOM richiesto** - L'elemento contenente l'annuncio da inserire nell'app.

**Asincrona**: Il delegato restituisce un oggetto contenente: Il delegato restituisce un oggetto contenente due proprietà: elemento e callback:

* **elemento:*****elemento* DOM richiesto** - L'elemento contenente l'annuncio da inserire nell'app.
* **callback:*****funzione richiesta*** - callback che gestirà l'inserimento dell'annuncio nell'elemento DOM soprastante.

Per `Conv` l'oggetto, è possibile trasmettere una stringa a denotare il titolo della sezione annuncio:

* **stringhe:****(facoltativo)** - Utilizzato per personalizzare il testo dell'intestazione per i tuoi annunci. «Sponsorizzata» per impostazione predefinita.

## Esempio sincrono {#concept_E733E4431D9948638B8102ADE398735F}

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
<div id="livefyre-app-17"></div> 
<script> 
  
(function() { 
  var nextSlotId = 1; 
  function generateNextSlotName() { 
    var id = nextSlotId++; 
    return 'adslot' + id; 
  } 
  Livefyre.require(['fyre.conv#qa'], function(Conv) { 
    new Conv({ 
      network: 'qa-0.fyre.co', 
        env: 'qa', 
        strings: { 
          'sponsored': 'Sponsored by: Livefyre' 
        } 
      }, [{ 
        app: 'main', 
        siteId: '291206', 
        articleId: '17', 
        el: 'livefyre-app-17', 
        ad: { 
          delay: 5, 
          frequency: 10, 
          delegate: function(data) { 
            var elem = document.createElement('div'); 
            elem.id = generateNextSlotName(); 
            return { 
              element: elem 
            }; 
          } 
        } 
      }], function (widget) { 
        // Initialize or Auth 
      }); 
    }); 
}()); 
</script>
```

## Esempio asincrono {#concept_16B798C7EB20423DAA53ACCC71540051}

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
<div id="livefyre-app-17"></div> 
<script> 
  
(function() { 
  var nextSlotId = 1; 
  function generateNextSlotName() { 
    var id = nextSlotId++; 
    return 'adslot' + id; 
  } 
  function insertSlot(slotName) { 
    var adElem = document.createElement("img"); 
    var ad = "https://your-ad-here.com/great-ad-image.image"; 
    adElem.setAttribute("src", ad); 
    document.getElementById(slotName).appendChild(adElem); 
  } 
  Livefyre.require(['fyre.conv#qa'], function(Conv) { 
    new Conv({ 
      network: 'qa-0.fyre.co', 
        env: 'qa', 
        strings: { 
          'sponsored': 'Sponsored by: Livefyre' 
        } 
      }, [{ 
        app: 'main', 
        siteId: '291206', 
        articleId: '17', 
        el: 'livefyre-app-17', 
        ad: { 
          delay: 5, 
          frequency: 10, 
          delegate: function(data) { 
            var elem = document.createElement('div'); 
            elem.id = generateNextSlotName(); 
            return { 
              element: elem, 
              callback: function() { 
                insertSlot(elem.id); 
              } 
            }; 
          } 
        } 
      }], function (widget) { 
        // Initialize or Auth 
      }); 
    }); 
}()); 
</script>
```
