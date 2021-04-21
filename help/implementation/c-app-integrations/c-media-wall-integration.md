---
description: Crea una bacheca multimediale con streaming dei contenuti in tempo reale.
title: Parete multimediale
exl-id: 597af7e1-9ada-4893-9071-e17c21ef0d04
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 0%

---

# Media Wall{#media-wall}

Crea una bacheca multimediale con streaming dei contenuti in tempo reale.

Media Wall consente di creare un muro sociale in tempo reale per il sito. Utilizza il pacchetto snello-wallpackage dell’SDK JavaScript per Livefyre per visualizzare i feed social di Livefyre come un’esperienza visivamente coinvolgente, a schermo intero e con contenuti a tessere che è ottimo per la copertura di eventi live, l’hosting di concorsi fotografici e la promozione di sezioni social del tuo sito web.

## Integrazione {#section_jfm_bwb_c1b}

Il modo più rapido per aggiungere una Media Wall è quello di utilizzare la versione creata ospitata sulla rete CDN di Livefyre.

Innanzitutto, aggiungi [Livefyre.js](https://github.com/Livefyre/Livefyre.js) al tuo sito.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

Quindi, posiziona l&#39;elemento in cui apparirà la Media Wall.

```
<div id="wall"></div>
```

Infine, utilizza `Livefyre.require` per creare il componente.

```
<script> 
Livefyre.require([ 
    'streamhub-wall#5' 
], function(MediaWall) {     
    var wall = window.wall = new MediaWall({ 
        el: document.getElementById("wall"), 
        collection: { 
            "network": "client-solutions.fyre.co", 
            "siteId": "364309", 
            "articleId": "answers-mediawall" 
        } 
    }); 
}); 
</script>
```

Ora avete un muro! Vedi tutto in azione in [questo esempio](https://codepen.io/gobengo/pen/dFwDL).

**Hit un errore?** Verifica di trasmettere il parametro di ambiente corretto. Le opzioni disponibili sono `livefyre.com` (produzione) o `t402.livefyre.com` (UAT).

>[!NOTE]
>
>Qualsiasi personalizzazione dello stile dei tweet renderizzati dalla tua app Media Wall deve essere effettuata in conformità ai [Requisiti di visualizzazione di Twitter](https://dev.twitter.com/terms/display-requirements).

## Opzioni di configurazione {#section_ucv_qvb_c1b}

`columns`

Consente di definire il numero di colonne per Media Wall durante la costruzione della parete. Se questa opzione è impostata, la larghezza di ogni colonna si adatta automaticamente alle dimensioni del contenitore di Media Wall, mantenendo il numero specificato di colonne.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5 
});
```

`initial`

Il numero di elementi di contenuto di cui eseguire il rendering al caricamento della pagina. Il valore predefinito è 50.

```
var wallView = new MediaWall({ 
   el: document.getElementById('wall'), 
   initial: 10 
});
```

`minContentWidth`

Consente di impostare la larghezza minima (in pixel) per ogni colonna all’interno dell’elemento contenitore di Media Wall. La Media Wall selezionerà automaticamente un numero adeguato di colonne, a seconda della larghezza del relativo elemento contenitore. Per impostazione predefinita, la larghezza di Media Wall divisa per la larghezza minima del contenuto (300 px, se non definita) determina il numero di colonne.)

>[!NOTE]
>
>Non utilizzare questa opzione in combinazione con l’opzione Colonne .

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    minContentWidth: 300 
});
```

`modal`

Per impostazione predefinita, quando sono presenti allegati per una parte di contenuto, in Media Walls viene visualizzata una miniatura cliccabile. Quando fai clic su , l’app apre una finestra modale che mostra l’allegato foto/video nella sua interezza. Per disabilitare questa opzione, imposta modale su false.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5, 
    modal: false 
});
```

`postButton`

Definisce il pulsante [!UICONTROL Post Content] da visualizzare sulla parete. Questa opzione richiede di passare `opts.collection` e aggiungere un’integrazione di Livefyre.js Auth alla pagina.

`postButton` parametri:

* `false` (predefinito): Non mostrare un pulsante Post Content (Contenuto post). (Crea una Media Wall di sola lettura).
* `true` o  `LiveMediaWall.postButtons.contentWithPhotos`: Includi un pulsante che consente agli utenti di aggiungere testo con le foto allegate.

* `LiveMediaWall.postButtons.content`: Includi un pulsante che consente agli utenti di aggiungere contenuto di testo, ma non di allegare foto.
* `LiveMediaWall.postButtons.photo`: Includi un pulsante che consente agli utenti di aggiungere una foto, ma senza testo.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    collection: collection, 
    postButton: true, 
    minContentWidth: 300 
});
```

`showMore`

Definisce il numero di elementi di contenuto da aggiungere alla parete quando si fa clic sul pulsante [!UICONTROL Show More] .

```
var wallView = new LiveMediaWall({ 
    el: document.getElementById('wall'), 
    showMore: 10 
});
```

## Opzioni di configurazione dello stile {#section_ztv_dvb_c1b}

Media Wall offre anche diverse opzioni di configurazione che consentono di personalizzare il colore del testo, lo stile e le dimensioni. Per implementare queste opzioni, utilizza la sintassi seguente:

```
var wall2 = window.wall2 = new MediaWall({ 
   el: document.getElementById("listView1"), 
   collection: collection, 
   cardBackgroundColor: '#333', 
   textColor: 'magenta', 
   linkColor: 'orange', 
   footerTextColor: 'lime', 
   displayNameColor: 'cyan', 
   usernameColor: 'red', 
   fontFamily: 'Helvetica, Arial', 
   linkAttachmentBackgroundColor: '#555', 
   linkAttachmentBorderColor: '#888' 
}); 
```

Per un input valido, consulta gli standard W3C per le proprietà CSS [Font Family](https://www.w3.org/TR/CSS2/fonts.html#propdef-font-family), [Font Size](https://www.w3.org/TR/CSS2/fonts.html#font-size-props), [Line Height,](https://www.w3.org/TR/CSS2/visudet.html#propdef-line-height) e [Color](https://www.w3.org/TR/css3-color/#colorunits).

* **bodyFontSize** *(CSS Font Size String)* La dimensione del font per il testo del corpo del contenuto.

* **bodyLineHeight** *(CSS Line Height String)* L&#39;altezza della riga per il testo del corpo del contenuto.

* **buttonActiveBackgroundColor** *(CSS Color String)** Il colore dello sfondo del pulsante su attivo.

* **buttonBorderColor** *(CSS Color String)** Il colore per i bordi dei pulsanti.

* **buttonHoverBackgroundColor** *(CSS Color String)* Il colore dello sfondo del pulsante al passaggio del mouse.

* **buttonTextColor** *(CSS Color String)* Il colore per le etichette dei pulsanti.

* **cardBackgroundColor** *(CSS Color String)* Il colore di sfondo per le schede di contenuto nella bacheca dei supporti.

* **displayNameColor** *(CSS Color String)* Il colore dei nomi visualizzati nel nome della riga di testo.

* **fontFamily** *(CSS Font Family String)* La famiglia di font per il testo del corpo.

* **footerTextColor** *(CSS Color String)* Il colore del testo secondario (ad esempio il testo a piè di pagina e il nome utente nel nome utente).

* **linkAttachmentBackgroundColor** *(CSS Color String)* Il colore di sfondo per gli allegati di collegamento (allegati impilati).

* **linkAttachmentBorderColor** *(CSS Color String)* Il colore del bordo per gli allegati di collegamento (allegati sovrapposti).

* **linkAttachmentTextColor** *(CSS Color String)* Il colore per il testo di collegamento.

* **linkColor** *(CSS Color String)* Il colore dei collegamenti ipertestuali (ad esempio collegamenti nel testo del corpo e collegamenti ai nomi visualizzati).

* **textColor** *(CSS Color String)* Il colore per il testo del corpo.

* **titleFontSize** *(CSS Font Size String)* La dimensione del font per i titoli dei contenuti.

* **titleLineHeight** *(CSS Line Height String)* L&#39;altezza della riga per i titoli dei contenuti.

* **sourceLogoColor** *(CSS Color String)* Il colore per il logo sorgente.

* **usernameColor** *(CSS Color String)* Il colore per i nomi utente nel nome utente nel nome utente.
