---
description: Personalizzazione delle stringhe di testo per Livefyre Reviews.
seo-description: Personalizzazione delle stringhe di testo per Livefyre Reviews.
seo-title: Rivedi stringhe di testo
solution: Experience Manager
title: Rivedi stringhe di testo
uuid: 86251 e 49-bc 73-4 eec -9 f 9 b-b 4 b 0 a 5 b 42099
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Rivedi stringhe di testo{#review-text-strings}

Personalizzazione delle stringhe di testo per Livefyre Reviews.

Questa pagina elenca e descrive le stringhe disponibili per la personalizzazione nelle app di revisione. Le stringhe elencate qui sono oltre alle sostituzioni per le app di base di Livefyre, elencate in Personalizzazione stringa. Se sono elencati i duplicati, le stringhe elencate in queste tabelle sono il valore predefinito per le app Revisione.

Errori di implementazione dell'implementazione/Interfaccia
di valutazione Flusso di informazioni
sull'autore/Informazioni
sulle azioni
di Post

## Implementazione {#section-vsy-1k4-xz}

Per implementare questa funzione, passare una mappatura di oggetti 1-1 delle stringhe che desiderate ignorare all'oggetto di configurazione Javascript. Se non fornite un campo, verrà utilizzato il testo predefinito.

Esempio:

```
var customStrings = { 
   postAsButton: "New Post As Text", 
   postEditButton: "New Post Edit Text" }; 
networkConfig["strings"] = customStrings; fyre.conv.load( 
   networkConfig, 
   [convConfig], 
   function(){} 
);
```

## Interfaccia di revisione/valutazione {#section_iyv_zj4_xz}

Stringhe disponibili per l'interfaccia utente Revisione e Valutazione.

| Elemento | Chiave | Testo predefinito |
|--- |--- |--- |
| Pulsanti | Editreviewbtn | Modifica revisione |
|  | Reviewbtn | [Revisione in scrittura](https://d.pr/i/QscA) |
|  | Reviewsclosed | [Revisioni chiuse](https://d.pr/i/zr7M) |
|  | Showreviewbtn | [Mostra revisione](https://d.pr/i/onxU) |
|  | segui | l'm interessati |
|  | Sharetext | Ho appena scritto una revisione. Check it out! |
| Valutazione dei suggerimenti | Ratingvalues | Un array. Default = `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`; <br>Nota: I valori nell'array devono essere duplicati per assegnare allo stesso nome sia la metà sinistra che quella destra di ciascuna stella. |
| Valutazione delle parti secondarie | Ratingsubpartplaceholder | Un array. Predefinito = `[]` |
|  | Ratingsubparttitles | Un array. Predefinito = `[]` |
|  | Reviewstreamtitle | Vuoto per impostazione predefinita. Titolo della sezione di riepilogo della revisione. |
| Misc | Averagerating | [Valutazione media utente](https://d.pr/i/QscA) |
|  | Breakdownheader | [Suddivisione valutazione](https://d.pr/i/QscA) |
|  | utili | % s di % s trovato utile |
|  | Helpfulplural | % s di % s trovato utile |
|  | Outof | / |
|  | Ratingtype | stella |

## Informazioni flusso {#section_wmv_yj4_xz}

Stringhe disponibili per le informazioni sul flusso di contenuto e la visualizzazione.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| Ordinamento | Sortby | Vuoto per impostazione predefinita. |
|  | Sorthighestrated | [Valutazione più elevata](https://d.pr/i/huTd) |
|  | Sortlowestrated | [Valutazione più bassa](https://d.pr/i/huTd) |
|  | Sortmosthelpful | [Molto utili](https://d.pr/i/huTd) |
| Flusso misc. | Showmore | Mostra altro |
| Velocità ad alta velocità | Newcomment | Nuova revisione |
|  | Newcomments | Nuove recensioni |
| Conteggio dei listener | Listenercount | persona ascolto |
|  | Listenercountplural | persone ascolto |
| Conteggio dei commenti | Commentcountlabel | Livereviews<strong> | </strong>% s |
|  | Commentcountlabelpleral | Livereviews<strong> | </strong>% s |
| Conteggio dei commenti dei commenti | Commentnotifier | Nuova revisione |
|  | Commentnotifierplural | Nuove recensioni |

## Autore/Informazioni contenuto {#section_osx_xj4_xz}

Stings disponibili per informazioni sull'autore e sul contenuto.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| Thread Breakout | Reviewpurchentnotfoundmsg | [La revisione non è più visibile](https://d.pr/i/svXs) |
|  | Backtocomments | Torna alle revisioni |

## Azioni utente {#section_tlx_wj4_xz}

Stringhe disponibili per le azioni dell'utente: segnalazione, condivisione e contrassegno di contenuti esistenti come utili.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| Piè di pagina commento | Wasreviewhelpful | [Utile?](https://d.pr/i/Q0mA) |
|  | Wasreviewhelpfulmobile | Utile? |
|  | Ownwasreviewhelpful | [Trovato utile.](https://d.pr/i/Q0mA) |
|  | Reviewwashelpful | [Sì](https://d.pr/i/Q0mA) |
|  | Helpfuldivider | [& amp; vert;](https://d.pr/i/Q0mA) |
|  | Reviewwasnothelpful | [No](https://d.pr/i/Q0mA) |
| Modale votazione | Votetitle | Questa revisione è utile? |
|  | Votedownvote | No |
|  | Livesteplytitle | Questa risposta è utile? |
|  | Votetitle | Questo commento è stato utile? |
|  | Voteupvote | Sì |
| Flag modale | Flagtitle | Review % s's review |
|  | Flagsuccessmsg | La revisione è stata segnalata. |
| Flag Mobile | Flagconfirmationmessage | Flag % s's review as % s? |
| Menzioni modali | Mentiondefaulttext | I mentioned you in a Livefyre review! |
| Modale condivisione | Sharetitle | Condivisione condivisione |

## Funzioni post {#section_yl1_wj4_xz}

Stringhe disponibili per gli utenti che pubblicano revisioni.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| Editor | Bodyplaceholder | Revisione scrittura… |
|  | Posteditbutton | Modifica |
|  | Posteditcancelbutton | Annulla |
|  | Postasbutton | Post review as… |
|  | Postbutton | Revisione post |
|  | Postreplyasbutton | Pubblica come… |
|  | Postreplybutton | Post |
|  | Sharebutton | Condividi |
|  | Titleplaceholder | Titolo… |

## Errori {#section_jbc_vj4_xz}

Stringhe disponibili per messaggi di errore generici.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| Errori | Erroralreadyposting | È possibile pubblicare una sola revisione. |
|  | Errorautherror | Non sei autorizzato a pubblicare una revisione in questa conversazione |
|  | Errorcommentsnotallowed | Le revisioni non possono essere pubblicate al momento |
|  | Errordiswithowncomment | Non puoi disattivare la tua recensione |
|  | Errorduplicate | Non è possibile pubblicare due volte la tua recensione. |
|  | Erroreditduplicate | È necessario modificare il corpo della revisione quando la si modifica. |
|  | Erroreditnotallowed | Non è possibile modificare le revisioni in questa conversazione. |
|  | Erroredittimeexceeded | Il periodo di modifica della revisione è scaduto. |
|  | Errorempty | Sembra che stiate tentando di pubblicare una revisione vuota. |
|  | Erroremptytitle | Sembra che tu stia tentando di pubblicare un titolo vuoto |
|  | Errorfieldrating | valutazione a stella |
|  | Errorfieldreview | review |
|  | Errorfieldtitle | title |
|  | Errormaxchars | La revisione è troppo lunga. Please edit and try again. |
|  | Errormissingfields | Immettete un |
|  | Errorratingempty | Non è possibile inviare una valutazione vuota |
|  | Errorratingnotset | Tutte le valutazioni devono essere impostate |
|  | Errorratingnotvalid | La valutazione deve essere un oggetto |
|  | Errorshowmore | Si è verificato un errore durante il caricamento di più revisioni. |
|  | Errortitlemaxchars | Il titolo è troppo lungo. Please edit and try again. |
|  | Errorvoteowncomment | Non potete votare nella vostra revisione |

