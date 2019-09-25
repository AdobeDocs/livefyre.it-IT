---
description: Create una bacheca multimediale con streaming dei contenuti in tempo reale.
seo-description: Create una bacheca multimediale con streaming dei contenuti in tempo reale.
seo-title: Muro di supporto
solution: Experience Manager
title: Muro di supporto
uuid: c6087c80-a35b-44d2-9dd4-ba9cd471172d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Muro di supporto{#media-wall}

Create una bacheca multimediale con streaming dei contenuti in tempo reale.

Media Wall consente di creare un muro sociale in tempo reale per il sito. Utilizzate il pacchetto di streaming per l'SDK JavaScript di Livefyre per visualizzare i feed social di Livefyre come un'esperienza di contenuto a schermo intero e coinvolgente dal punto di vista visivo, che è ideale per la copertura di eventi in diretta, l'hosting di concorsi fotografici e l'alimentazione di sezioni social del sito Web.

## Integrazione {#section_jfm_bwb_c1b}

Il modo più rapido per aggiungere un Media Wall consiste nell’utilizzare la versione creata ospitata sulla rete CDN di Livefyre.

Innanzitutto, aggiungete [Livefyre.js](https://github.com/Livefyre/Livefyre.js) al sito.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

Quindi, posizionate l’elemento in cui apparirà la Parete multimediale.

```
<div id="wall"></div>
```

Infine, utilizzare `Livefyre.require` per creare il componente.

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

Ora hai un muro! Vedete tutto in azione in [questo esempio](https://codepen.io/gobengo/pen/dFwDL).

**Ha avuto un errore?** Verificate di trasmettere il parametro di ambiente corretto. Le opzioni includono `livefyre.com` (produzione) o `t402.livefyre.com` (UAT).

>[!NOTE]
>
>Qualsiasi personalizzazione stile dei tweet renderizzati dall’app Media Wall deve essere eseguita in conformità ai requisiti [di](https://dev.twitter.com/terms/display-requirements)visualizzazione di Twitter.

## Opzioni di configurazione {#section_ucv_qvb_c1b}

`columns`

Consente di definire il numero di colonne per la parete multimediale durante la costruzione della parete. Se questa opzione è impostata, la larghezza di ciascuna colonna si adatta automaticamente alle dimensioni del contenitore di Media Wall, mantenendo al contempo il numero specificato di colonne.

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

Consente di impostare la larghezza minima (in pixel) per ogni colonna all’interno dell’elemento contenitore di Media Wall. (La Media Wall selezionerà automaticamente un numero appropriato di colonne, a seconda della larghezza del relativo elemento contenitore. Per impostazione predefinita, la larghezza di Media Wall divisa per la larghezza minima del contenuto (300 pixel, se non definita) determina il numero di colonne.)

>[!NOTE]
>
>Non utilizzate questa opzione in combinazione con l'opzione relativa alle colonne.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    minContentWidth: 300 
});
```

`modal`

Per impostazione predefinita, in presenza di allegati per una parte di contenuto, nelle mura dei supporti viene visualizzata una miniatura selezionabile. Quando un utente fa clic su di esso, l'app si apre una modalità con l'allegato foto/video interamente visualizzato. Per disattivare questa opzione, impostate modale su false.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5, 
    modal: false 
});
```

`postButton`

Definisce il [!UICONTROL Post Content] pulsante da visualizzare sulla parete. Questa opzione richiede il passaggio `opts.collection`e l'aggiunta di un'integrazione Livefyre.js Auth alla pagina.

`postButton` parametri:

* `false` (predefinito): Non mostrare un pulsante Post Content (Contenuto post). (Crea una bacheca di sola lettura).
* `true` o `LiveMediaWall.postButtons.contentWithPhotos`: Includere un pulsante che consenta agli utenti di aggiungere del testo, con le foto allegate.

* `LiveMediaWall.postButtons.content`: Include un pulsante che consente agli utenti di aggiungere del testo, ma non allegare foto.
* `LiveMediaWall.postButtons.photo`: Include un pulsante che consente agli utenti di aggiungere una foto, ma nessun testo.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    collection: collection, 
    postButton: true, 
    minContentWidth: 300 
});
```

`showMore`

Definisce il numero di elementi di contenuto da aggiungere alla bacheca quando si fa clic sul [!UICONTROL Show More] pulsante.

```
var wallView = new LiveMediaWall({ 
    el: document.getElementById('wall'), 
    showMore: 10 
});
```

## Opzioni configurazione stile {#section_ztv_dvb_c1b}

Media Wall offre inoltre diverse opzioni di configurazione che consentono di personalizzare il colore, lo stile e la dimensione del testo. Per implementare queste opzioni, utilizzate la sintassi seguente:

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

Per un input valido, consultate gli standard W3C per le proprietà Famiglia [di](https://www.w3.org/TR/CSS2/fonts.html#propdef-font-family)font CSS, Dimensione [](https://www.w3.org/TR/CSS2/fonts.html#font-size-props)font, [Altezza](https://www.w3.org/TR/CSS2/visudet.html#propdef-line-height) linea e [Colore](https://www.w3.org/TR/css3-color/#colorunits) .

* **bodyFontSize** *(CSS Font Size String)* La dimensione del font per il testo del corpo del contenuto.

* **bodyLineHeight** *(CSS Line Height String)* L'altezza della riga per il testo del corpo del contenuto.

* **buttonActiveBackgroundColor** *(CSS Color String)** Colore per lo sfondo del pulsante attivo.

* **buttonBorderColor** *(CSS Color String)** Il colore dei bordi del pulsante.

* **buttonHoverBackgroundColor** *(CSS Color String)* Il colore dello sfondo del pulsante al passaggio del mouse.

* **buttonTextColor** *(CSS Color String)* Il colore per le etichette dei pulsanti.

* **cardBackgroundColor** *(CSS Color String)* Il colore di sfondo per le schede di contenuto nella bacheca del supporto.

* **displayNameColor** *(CSS Color String)* Il colore per i nomi di visualizzazione nel nome della riga.

* **fontFamily** *(CSS Font Family String)* La famiglia di font per il testo del corpo.

* **footerTextColor** *(CSS Color String)* Il colore del testo secondario (ad esempio il testo del piè di pagina e il nome utente nel nome utente).

* **linkAttachmentBackgroundColor** *(CSS Color String)* Colore di sfondo per gli allegati di collegamenti (allegati sovrapposti).

* **linkAttachmentBorderColor** *(CSS Color String)* Colore del bordo per gli allegati di collegamenti (allegati sovrapposti).

* **linkAttachmentTextColor** *(CSS Color String)* Il colore del testo di collegamento.

* **linkColor** *(CSS Color String)* Il colore dei collegamenti ipertestuali (ad esempio, i collegamenti nel testo del corpo e i collegamenti dei nomi visualizzati).

* **textColor** *(CSS Color String)* Il colore del testo del corpo.

* **titleFontSize** *(CSS Font Size String)* La dimensione del font per i titoli dei contenuti.

* **titleLineHeight** *(CSS Line Height String)* L'altezza della riga per i titoli del contenuto.

* **sourceLogoColor** *(CSS Color String)* Il colore per il logo sorgente.

* **usernameColor** *(Stringa colore CSS)* Il colore per i nomi utente nel nome utente.
