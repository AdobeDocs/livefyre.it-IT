---
description: Create una bacheca media, con lo streaming di contenuti in tempo reale.
seo-description: Create una bacheca media, con lo streaming di contenuti in tempo reale.
seo-title: Media Wall
solution: Experience Manager
title: Media Wall
uuid: c 6087 c 80-a 35 b -44 d 2-9 dd 4-ba 9 cd 471172 d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Media Wall{#media-wall}

Create una bacheca media, con lo streaming di contenuti in tempo reale.

Media Wall consente di creare una bacheca social in tempo reale per il sito. Utilizzate il pacchetto «streamer-wallpackage» di Livefyre Javascrire per visualizzare i feed social di Livefyre come un&#39;esperienza di contenuto a schermo intero, accattivante, a schermo intero che è grande per gli eventi in diretta, l&#39;hosting di concorsi fotografici e la capacità di gestire sezioni social del vostro sito Web.

## Integrazione {#section_jfm_bwb_c1b}

Il modo più rapido per aggiungere un file Media Wall consiste nell&#39;usare la versione integrata nella CDN di Livefyre.

Innanzitutto, aggiungete [Livefyre. js](https://github.com/Livefyre/Livefyre.js) al sito.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

Quindi, posizionate l&#39;elemento in cui verrà visualizzato il file multimediale.

```
<div id="wall"></div>
```

Infine, utilizzate `Livefyre.require` per creare il componente.

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

Ora hai una Bacheca! Consultate questa sezione in [questo esempio](https://codepen.io/gobengo/pen/dFwDL).

**Hit un errore?** Verificate di aver superato il parametro dell&#39;ambiente corretto. Le opzioni includono `livefyre.com` (produzione) o `t402.livefyre.com` (UAT).

>[!NOTE]
>
>Qualsiasi personalizzazione di stile dei tweet che viene resa dall&#39;app Media Wall deve essere eseguita in conformità ai requisiti [di visualizzazione di Twitter](https://dev.twitter.com/terms/display-requirements).

## Opzioni di configurazione {#section_ucv_qvb_c1b}

`columns`

Consente di definire il numero di colonne per i Media Wall durante la costruzione della bacheca. Se questa opzione è impostata, la larghezza di ogni colonna si adatta automaticamente alle dimensioni del contenitore di Media Wall, mantenendo il numero specificato di colonne.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5 
});
```

`initial`

Numero di elementi Contenuto da rappresentare al caricamento della pagina. Il valore predefinito è 50.

```
var wallView = new MediaWall({ 
   el: document.getElementById('wall'), 
   initial: 10 
});
```

`minContentWidth`

Consente di impostare la larghezza minima (pixel) per ogni colonna nell&#39;elemento contenitore di Media Wall. (Media Wall seleziona automaticamente un numero appropriato di colonne, a seconda della larghezza del suo elemento contenitore. Per impostazione predefinita, la larghezza di Media Wall divisa per la larghezza minima del contenuto (300 px, se non definito) determina il numero di colonne.

>[!NOTE]
>
>Non utilizzate questa opzione in combinazione con l&#39;opzione colonne.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    minContentWidth: 300 
});
```

`modal`

Per impostazione predefinita, se sono presenti allegati per contenuti, Media Walls visualizza una miniatura selezionabile. Quando viene fatto clic su, l&#39;app apre una modale che visualizza l&#39;allegato di foto/video integralmente. Per disattivare questa opzione, impostate modale su false.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5, 
    modal: false 
});
```

`postButton`

Definisce [!UICONTROL Post Content] il pulsante da visualizzare sulla bacheca. Questa opzione richiede l&#39;accesso `opts.collection`e aggiunge un&#39;integrazione di Livefyre. js alla pagina.

`postButton` parametri:

* `false` (predefinito): Non visualizzare un pulsante Post post. (Crea una Media Wall di sola lettura).
* `true` (o `LiveMediaWall.postButtons.contentWithPhotos`): Includete un pulsante che consente agli utenti di aggiungere contenuto di testo, con foto allegate.

* `LiveMediaWall.postButtons.content`: Includete un pulsante che consente agli utenti di aggiungere contenuto di testo, ma non di allegare foto.
* `LiveMediaWall.postButtons.photo`: Includete un pulsante che consenta agli utenti di aggiungere una foto, ma nessun testo.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    collection: collection, 
    postButton: true, 
    minContentWidth: 300 
});
```

`showMore`

Definisce il numero di elementi Contenuto da aggiungere alla bacheca quando si fa clic [!UICONTROL Show More] sul pulsante.

```
var wallView = new LiveMediaWall({ 
    el: document.getElementById('wall'), 
    showMore: 10 
});
```

## Opzioni di configurazione stile {#section_ztv_dvb_c1b}

Media Wall offre inoltre diverse opzioni di configurazione che consentono di personalizzare colore, stile e dimensioni del testo. Per implementare queste opzioni, utilizzare la sintassi seguente:

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

Per un input valido, consultare gli standard W 3 C per le proprietà Famiglia [font CSS](https://www.w3.org/TR/CSS2/fonts.html#propdef-font-family), [Dimensione font](https://www.w3.org/TR/CSS2/fonts.html#font-size-props), [Altezza riga](https://www.w3.org/TR/CSS2/visudet.html#propdef-line-height) e [Colore](https://www.w3.org/TR/css3-color/#colorunits) .

* **Bodyfontsize** *(CSS Font Size String)* La dimensione del font per il testo del corpo del contenuto.

* **Bodylineheight** *(Stringa altezza CSS)* L&#39;altezza della riga per il testo del corpo del contenuto.

* **Buttonactivebackgroundcolor** *(CSS Color String)** Il colore dello sfondo del pulsante attivato.

* **Buttonbordercolor** *(CSS Color String)** Il colore per i bordi dei pulsanti.

* **Buttonhoverbackgroundcolor** *(CSS Color String)* Il colore per lo sfondo del pulsante al passaggio del mouse.

* **Buttontextcolor** *(CSS Color String)* Il colore per le etichette dei pulsanti.

* **Cardbackgroundcolor** *(CSS Color String)* Il colore di sfondo per le schede di contenuto nella bacheca del supporto.

* **Displaynamecolor** *(CSS Color String)* Il colore per i nomi visualizzati nel nome.

* **Fontfamily** *(CSS Font Family String)* La famiglia di font per il testo corpo.

* **Footertextcolor** *(CSS Color String)* Il colore per il testo secondario (ad esempio il testo piè di pagina e il nome utente nella riga byte).

* **Linkattachmentbackgroundcolor** *(CSS Color String)* Il colore di sfondo per gli allegati di collegamento (allegati impilati).

* **Linkattachmentbordercolor** *(CSS Color String)* Il colore del bordo per gli allegati di collegamento (allegati impilati).

* **Linkattachmenttextcolor** *(CSS Color String)* Il colore per il testo allegato collegamento.

* **Linkcolor** *(CSS Color String)* Il colore per i collegamenti ipertestuali (ad esempio i collegamenti nel testo corpo e i collegamenti nome visualizzato).

* **Textcolor** *(CSS Color String)* Il colore del testo corpo.

* **Titlefontsize** *(CSS Font Size String)* Dimensione del font per i titoli dei contenuti.

* **Titleelineheight** *(Stringa altezza riga CSS)* Altezza della riga per i titoli dei contenuti.

* **Sourcelogocolor** *(CSS Color String)* Il colore del logo sorgente.

* **Usernamecolor** *(CSS Color String)* Il colore per i nomi utente nel nome.
