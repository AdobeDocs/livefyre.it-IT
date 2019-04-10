---
description: I set di traduzioni consentono di specificare lingua alternativa per
  le app.
seo-description: I set di traduzioni consentono di specificare lingua alternativa
  per le app.
seo-title: Set di traduzioni
solution: Experience Manager
title: Set di traduzioni
uuid: 8 ba 66 a 61-5520-482 a-bc 0 b-e 4 f 6 b 57 f 1744
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Set di traduzioni {#translation-sets}

I set di traduzioni consentono di specificare lingua alternativa per le app.

<!-- 
c_translation_sets.dita
-->

Utilizzate le impostazioni di traduzione per localizzare le app in diverse lingue o per specificare testo alternativo per più app da una posizione in Studio. Ad esempio, puoi fare in modo che tutti i siti della lingua spagnola utilizzino lingua spagnolo per tutti i campi App. Potete inoltre modificare il testo in modo che tutti i campi corrispondano alla voce del sito o della rete.

Potete specificare le impostazioni di conversione per tutte le app, ad eccezione di Storify 2. Per ulteriori informazioni sui campi che è possibile localizzare, vedere [Localizza stringhe](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md).

Commenti, Blog live e Chat condividono lo stesso set di stringhe all'interno di un set di traduzioni.

Specifica un set di traduzioni per una rete, un sito, un'app o un'API.

I set di conversione a diversi livelli si sostituiscono a seconda di questo pattern:

* Il set di traduzione API sostituisce eventuali set di conversione a qualsiasi livello (App, Rete e Sito)
* Il set di traduzione delle app sostituisce i set di traduzione a livello di rete e a livello di sito.
* I set di traduzioni a livello di sito ignorano i set di traduzione a livello di rete.

## Rivedi stringhe di testo {#c-review-text-strings}

Personalizzazione delle stringhe di testo per Livefyre Reviews.

Questa pagina elenca e descrive le stringhe disponibili per la personalizzazione nelle app di revisione. Le stringhe elencate qui sono oltre alle sostituzioni per le app di base di Livefyre, elencate in Personalizzazione stringa. Se sono elencati i duplicati, le stringhe elencate in queste tabelle sono il valore predefinito per le app Revisione.

* Implementazione
* Interfaccia di revisione/valutazione
* Informazioni flusso
* Autore/Informazioni contenuto
* Azioni utente
* Funzioni post
* Errori

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
| --------------- | ------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| Pulsanti |  |  |
|  | Editreviewbtn | Modifica revisione |
|  | Reviewbtn | Revisione in scrittura |
|  | Reviewsclosed | Revisioni chiuse |
|  | Showreviewbtn | Mostra revisione |
|  | segui | l'm interessati |
|  | Sharetext | Ho appena scritto una revisione. Check it out! |
| Valutazione dei suggerimenti |  |  |
|  | Ratingvalues | Un array. Default =['Poor ','Poor ','Fair ','Fair ','Averagè,'Averagè,'Good ','Good ','Ottimo ','Eccellentè]; |
|  |  | Nota: I valori nell'array devono essere duplicati per assegnare allo stesso nome sia la metà sinistra che quella destra di ciascuna stella. |
| Valutazione delle parti secondarie |  |  |
|  | Ratingsubpartplaceholder | Un array. Predefinito =[] |
|  | Ratingsubparttitles | Un array. Predefinito =[] |
|  | Reviewstreamtitle | Vuoto per impostazione predefinita. Titolo della sezione di riepilogo della revisione. |
| Misc |  |  |
|  | Averagerating | Valutazione media utente |
|  | Breakdownheader | Suddivisione valutazione |
|  | utili | % s di % s trovato utile |
|  | Helpfulplural | % s di % s trovato utile |
|  | Outof | / |
|  | Ratingtype | stella |

## Informazioni flusso {#section_wmv_yj4_xz}

Stringhe disponibili per le informazioni sul flusso di contenuto e la visualizzazione.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| *Ordinamento* |  |  |
|  | Sortby | *Vuoto per impostazione predefinita.* |
|  | Sorthighestrated | [Valutazione più elevata](https://d.pr/i/huTd) |
|  | Sortlowestrated | [Valutazione più bassa](https://d.pr/i/huTd) |
|  | Sortmosthelpful | [Molto utili](https://d.pr/i/huTd) |
| *Flusso misc.* |  |  |
|  | Showmore | Mostra altro |
| *Velocità ad alta velocità* |  |  |
|  | Newcomment | Nuova revisione |
|  | Newcomments | Nuove recensioni |
| *Conteggio dei listener* |  |  |
|  | Listenercount | persona ascolto |
|  | Listenercountplural | persone ascolto |
| *Conteggio dei commenti* |  |  |
|  | Commentcountlabel | Livereviews |
|  | Commentcountlabelpleral | Livereviews |
| *Conteggio dei commenti dei commenti* |  |  |
|  | Commentnotifier | Nuova revisione |
|  | Commentnotifierplural | Nuove recensioni |

## Autore/Informazioni contenuto {#section_osx_xj4_xz}

Stings disponibili per informazioni sull'autore e sul contenuto.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| *Thread Breakout* |  |  |
|  | Reviewpurchentnotfoundmsg | [La revisione non è più visibile](https://d.pr/i/svXs) |
|  | Backtocomments | Torna alle revisioni |

## Azioni utente {#section_tlx_wj4_xz}

Stringhe disponibili per le azioni dell'utente: segnalazione, condivisione e contrassegno di contenuti esistenti come utili.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| *Piè di pagina commento* |  |  |
|  | Wasreviewhelpful | [Utile?](https://d.pr/i/Q0mA) |
|  | Wasreviewhelpfulmobile | Utile? |
|  | Ownwasreviewhelpful | [Trovato utile.](https://d.pr/i/Q0mA) |
|  | Reviewwashelpful | [Sì](https://d.pr/i/Q0mA) |
|  | Helpfuldivider | [& amp; vert;](https://d.pr/i/Q0mA) |
|  | Reviewwasnothelpful | [No](https://d.pr/i/Q0mA) |
| *Modale votazione* |  |  |
|  | Votetitle | Questa revisione è utile? |
|  | Votedownvote | No |
|  | Livesteplytitle | Questa risposta è utile? |
|  | Votetitle | Questo commento è stato utile? |
|  | Voteupvote | Sì |
| *Flag modale* |  |  |
|  | Flagtitle | Review % s's review |
|  | Flagsuccessmsg | La revisione è stata segnalata. |
| *Flag Mobile* |  |  |
|  | Flagconfirmationmessage | Flag % s's review as % s? |
| *Menzioni modali* |  |  |
|  | Mentiondefaulttext | I mentioned you in a Livefyre review! |
| *Modale condivisione* |  |  |
|  | Sharetitle | Condivisione condivisione |

## Funzioni post {#section_yl1_wj4_xz}

Stringhe disponibili per gli utenti che pubblicano revisioni.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| *Editor* |  |  |
|  | Bodyplaceholder | Revisione scrittura… |
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
| Errori |  |  |
|  | Erroralreadyposting | È possibile pubblicare una sola revisione. |
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

## Stringhe testo Sidenotes {#c_sidenotes_text_strings}

Personalizzazione delle stringhe di testo per Livefyre Sidenotes

<!-- 

c_sidenotes_text_strings.dita

 -->

Questa pagina elenca e descrive tutte le stringhe disponibili per la personalizzazione nelle app Sidenotes. Per informazioni sulle stringhe disponibili per le app di base Livefyre, consultate Personalizzazioni stringa.

* Implementazione
* Autenticazione
* Informazioni flusso
* Autore/Informazioni contenuto
* Azioni utente
* Funzioni post
* Interfaccia moderatore
* Errori

## Implementazione {#section_wp2_ql4_xz}

Per implementare questa funzione, passare una mappatura di oggetti 1-1 delle stringhe che desiderate ignorare all'oggetto di configurazione Javascript. Se non fornite un campo, verrà utilizzato il testo predefinito.

Esempio:

```
var customStrings = { 
   postAsButton: "New Post As Text", 
   postEditButton: "New Post Edit Text" 
}; 
networkConfig["strings"] = customStrings; fyre.conv.load( 
   networkConfig, 
   [convConfig], 
   function(){} 
);
```

## Autenticazione {#section_pqf_3l4_xz}

Stringhe disponibili per il processo Autenticazione e dai menu utente autenticati.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| *Stringhe di menu di autenticazione* |  |  |
|  | Menuauthsigninbtn | Accedi |
|  | Menuauthsignedinmsg | È necessario accedere a {action} |
|  | Menuusereditprofile | Modifica profilo |
|  | Menuuseradmin | Admin Console |
|  | Menuuserlogout | Esci |
|  | Menuuserbackbtn | Tutto |

## Informazioni flusso {#section_wpy_gl4_xz}

Stringhe disponibili per le informazioni sul flusso di contenuto e la visualizzazione.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| *Opzioni del menu Info* |  |  |
|  | Menuinfocopyright | © Livefyre, Inc. 2014 |
|  | Menuinfohelp | Aiuto |
|  | Menuinfolivefyrelink | Visitate Livefyre.com |

## Autore/Informazioni contenuto {#section_dhb_gl4_xz}

Stings disponibili per informazioni sull'autore e sul contenuto.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
|  | Commentmoderatortag | Mod |
|  | Commentpendingtag | In sospeso |
|  | Commentreadmorelink | Ulteriori informazioni |
|  | Commentreplylink | Vedere {numero} risposte |
|  | Commentreplylinksing | Vedere risposta |
|  | Commentvotecount | voti |
|  | Commentvotecountsing | votare |
|  | Datetimeminuteprefix | m |
|  | Datetimemonths | * Un array. Default = *[ 'January ','febbraio ','March ','April ','May ','Junè,'July ','August ','September ','October ','November ','December ' ] |
|  | Questionexplain | È ora possibile leggere e scrivere commenti direttamente su frasi, paragrafi, immagini e preventivi. <br>Evidenzia il testo e fai clic sull'icona o fai clic sull'icona alla fine di ciascun paragrafo. |
|  | Questionmocktext | Ciò che è «noto» non è noto correttamente, per il motivo di «familiare». |
|  | Questiontitle | Che cos'è un Sidenote? |

## Azioni utente {#section_qxd_fl4_xz}

Stringhe disponibili per le azioni dell'utente: segnalazione, condivisione e livecing di contenuti esistenti.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| *Opzioni del menu di risposta* |  |  |
|  | Menurepliesviewtitle | Dettagli |
|  | Menurepliesviewanswer | Rispondi alla conversazione |
| *Opzioni del menu Condividi* |  |  |
|  | Menushareoptionfacebook | Facebook |
|  | Menushareoptiontwitter | Twitter |
|  | Menusharetitle | Condividi |
| *Opzioni del menu Flag* |  |  |
|  | Menuflagoptiondisagree | Non d'accordo |
|  | Menuflagoptionoffensive | Offensivo |
|  | Menuflagoptionofftopic | Argomento Off |
|  | Menuflagoptionspam | Spam |
|  | Menuflagtitle | Flag come… |
|  | Facebooksharecaption | Filienalità su «{title}» |
| *Opzioni utente per dispositivi mobili* |  |  |
|  | Slidercommenttally | di |
|  | Sliderinviteread | Leggi |
|  | Sliderinvitewrite | Scrittura |
|  | Sliderloading | Caricamento in corso… |
|  | Sliderwritetext | Che cosa pensate? Toccate per scrivere. |

## Funzioni post {#section_xzf_2l4_xz}

Stringhe disponibili per gli utenti che pubblicano contenuto.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
|  | Editoreditbtn | Salva |
|  | Editoreditposting | Salvataggio in corso… |
|  | Editoreditreplytitle | Modifica risposta |
|  | Editoredittitle | Edit Sidenote (Modifica Sidenote) |
|  | Editorplaceholder | Che cosa pensate? |
|  | Editorpostbtn | Post Sidenote |
|  | Editorpostbtnmobile | Post |
|  | Editorposting | Pubblicazione in corso… |
|  | Editorreplybtn | Post Reply |
|  | Editorreplytitle | Scrivi risposta |
|  | Editortitle | Scrivi sidenote |
|  | Emptyimageblocktxt | Che cosa pensate? |
|  | Emptytextblocktxt | + |
|  | Responybtn | Risposta |
|  | Threadreplybtn | Rispondi alla conversazione |
| *Opzioni del menu Elimina* |  |  |
|  | Menuconfirmaccept | Sì, {action} |
|  | Menuconfirmcancel | Annulla |
|  | Menuconfirmtitle | Sei sicuro? |
| *Opzioni di menu ecc.* |  |  |
|  | Menuetcoptionapprove | Approva |
|  | Menuetcoptiondelete | Elimina |
|  | Menuetcoptionedit | Modifica |
|  | Menuetcoptionflag | Flag |
|  | Menuetcoptionshare | Condividi |
|  | Menuetcpostedat | Pubblicato in {data} |
|  | Menuetctitle | Altro |

## Interfaccia moderatore {#section_o5f_dl4_xz}

Stringhe disponibili per l'interfaccia moderatore autenticata dall'utente.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| *Messaggi di conferma dal menu Altro* |  |  |
|  | Notificationapproved | Approvato |
|  | Notificationdelete | Eliminato |
|  | Notificationflded | Segnalata |

## Errori {#section_gtk_cl4_xz}

Stringhe disponibili per messaggi di errore generici.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
|  | Errorconnection | Ah-oh. L'utente non sembra avere una buona connessione. |
|  | Errorduplicate | Anche la tua nota mi piace, ma non puoi pubblicarla due volte. |
|  | Errorgeneral | Si è verificato un errore. Riprovate. |
|  | Errorserver | Si è verificato un errore nel nostro server. Riprovare? |
