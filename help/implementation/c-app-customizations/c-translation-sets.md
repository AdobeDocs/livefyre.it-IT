---
description: I set di traduzione consentono di specificare la lingua alternativa per le app.
title: Set di traduzioni
exl-id: 688138bf-f8e9-4fe5-99e2-2451deefd217
source-git-commit: 3091db9d7b9611e26ad65c1432856c9465694e92
workflow-type: tm+mt
source-wordcount: '1302'
ht-degree: 6%

---

# Set di traduzioni {#translation-sets}

I set di traduzione consentono di specificare la lingua alternativa per le app.

Utilizza le impostazioni di traduzione per localizzare le app in diverse lingue o per specificare testo alternativo per più app da una posizione in Studio. Ad esempio, puoi assicurarti che tutti i siti in lingua spagnola utilizzino la lingua spagnola per tutti i campi dell’app. È inoltre possibile modificare il testo in modo che tutti i campi corrispondano alla voce e alle caratteristiche del sito o della rete.

Puoi specificare le impostazioni di traduzione per tutte le app, ad eccezione di Storify 2. Per ulteriori informazioni sui campi che è possibile localizzare, vedere [Localizzare le stringhe](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md).

Commenti, blog dal vivo e chat condividono lo stesso set di stringhe all’interno di un set di traduzione.

Specifica un set di traduzione per una rete, un sito, un’app o per l’utilizzo di un’API.

I set di traduzione a diversi livelli si sostituiscono a vicenda seguendo questo pattern:

* Il set di traduzione API sostituisce qualsiasi set di traduzione a qualsiasi livello (App, rete e sito)
* Il set di traduzione delle app ha la precedenza sui set di traduzione a livello di rete e di sito.
* I set di traduzione a livello di sito sovrascrivono i set di traduzione a livello di rete.

## Rivedi stringhe di testo {#c-review-text-strings}

Personalizzazione delle stringhe di testo per le recensioni di Livefyre.

Questa pagina elenca e descrive le stringhe disponibili per la personalizzazione nelle app di revisione. Le stringhe elencate qui sono in aggiunta e sostituiscono le stringhe predefinite per le app di base Livefyre, elencate in Personalizzazioni di stringhe. Se sono elencati i duplicati, le stringhe elencate in queste tabelle sono quelle predefinite per le app Reviews.

* Implementazione
* Interfaccia di revisione/valutazione
* Informazioni flusso
* Informazioni sull’autore/contenuto
* Azioni utente
* Funzioni post
* Errori

## Implementazione {#section-vsy-1k4-xz}

Per implementare questa funzione, passa una mappatura oggetto 1-1 delle stringhe che desideri ignorare all&#39;oggetto di configurazione Javascript. Se non si fornisce un campo, verrà utilizzato il testo predefinito.

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

Stringhe disponibili per l&#39;interfaccia utente di Revisione e Valutazione.

| Elemento | Chiave | Testo predefinito |
| --------------- | ------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| Pulsanti |  |  |
|  | editReviewBtn | Modifica revisione |
|  | reviewBtn | Revisione in scrittura |
|  | recensioniChiuso | Recensioni chiuse |
|  | showReviewBtn | Mostra revisione |
|  | seguire | Sono interessato |
|  | shareText | Ho appena scritto una recensione. Guardate! |
| Descrizioni comandi di valutazione |  |  |
|  | ratingValues | Un array. Predefinito = [&quot;Scarso&quot;, &quot;Scarso&quot;, &quot;Equo&quot;, &quot;Equo&quot;, &quot;Media&quot;, &quot;Media&quot;, &quot;Buono&quot;, &quot;Buono&quot;, &quot;Eccellente&quot;, &quot;Eccellente&quot;]; |
|  |  | Nota: i valori nella matrice devono essere duplicati per assegnare lo stesso nome sia alla metà sinistra che alla metà destra di ogni stella. |
| Sottoparti di valutazione |  |  |
|  | ratingSubpartPlaceholder | Un array. Impostazione predefinita = [] |
|  | ratingSubpartTitles | Un array. Impostazione predefinita = [] |
|  | reviewStreamTitle | Vuoto per impostazione predefinita. Titolo della sezione di riepilogo della revisione. |
| Varie |  |  |
|  | averageRating | Valutazione media utente |
|  | suddivisioneHeader | Suddivisione dei rating |
|  | utile | %s di %s trovato utile |
|  | helpPlural | %s di %s trovato utile |
|  | outOf | / |
|  | ratingType | stella |

## Informazioni flusso {#section_wmv_yj4_xz}

Stringhe disponibili per le informazioni e la visualizzazione del flusso di contenuto.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| *Ordinamento* |  |  |
|  | sortBy | *Vuoto per impostazione predefinita.* |
|  | sortHighestRated | Valutazione più elevata |
|  | sortLowestRated | Classificazione più bassa |
|  | sortMostHelpful | Più utile |
| *Flusso varie.* |  |  |
|  | showMore | Mostra altro |
| *Velocità elevata del flusso* |  |  |
|  | newComment | Nuova revisione |
|  | newComments | Nuove recensioni |
| *Conteggi listener* |  |  |
|  | listenerCount | ascolto personale |
|  | listenerCountPlural | gente che ascolta |
| *Conteggi dei commenti* |  |  |
|  | commentCountLabel | LiveReviews |
|  | commentCountLabelPlural | LiveReviews |
| *Conteggi dei notificatori dei commenti* |  |  |
|  | commentNotifier | Nuova revisione |
|  | commentNotifierPlural | Nuove recensioni |

## Informazioni sull’autore/contenuto {#section_osx_xj4_xz}

Impostazioni disponibili per informazioni sull’autore e sui singoli contenuti.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| *Suddivisione dei thread* |  |  |
|  | reviewContentNotFoundMsg | Questa revisione non è più visibile |
|  | backToComments | Torna a Recensioni |

## Azioni utente {#section_tlx_wj4_xz}

Stringhe disponibili per le azioni dell’utente: puoi assegnare tag, condividere e contrassegnare i contenuti esistenti come utili.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| *Piè di pagina commento* |  |  |
|  | wasReviewHelpful | Utile? |
|  | wasReviewHelpfulMobile | Utile? |
|  | ownwasReviewHelpful | Trovato utile. |
|  | reviewwasHelpful | Sì |
|  | helpDivider | &amp;vert; |
|  | reviewWASNotHelpful | No |
| *Votazione modale* |  |  |
|  | voteTitle | Questa recensione è stata utile? |
|  | voteDownvote | No |
|  | voteReplyTitle | Questa risposta è stata utile? |
|  | voteTitle | Questo commento è stato utile? |
|  | voteUpvote | Sì |
| *Flag modale* |  |  |
|  | flagTitle | Contrassegna la revisione di %s |
|  | flagSuccessMsg | La revisione è stata contrassegnata. |
| *Flag Mobile* |  |  |
|  | flagConfirmationMessage | Contrassegna la revisione di %s come %s? |
| *Modale di menzione* |  |  |
|  | mentionDefaultText | Ti ho menzionato in una recensione di Livefyre! |
| *Condividi modale* |  |  |
|  | shareTitle | Condividi revisione |

## Funzioni post {#section_yl1_wj4_xz}

Stringhe disponibili per gli utenti che pubblicano le revisioni.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| *Editor* |  |  |
|  | bodyPlaceholder | Scrivi recensione... |
|  | postEditButton | Modificare       |
|  | postEditCancelButton | Annulla |
|  | postAsButton | Post review as.. |
|  | postButton | Revisione post |
|  | postReplyAsButton | Pubblica come... |
|  | postReplyButton | Post |
|  | shareButton | Condividi |
|  | titlePlaceholder | Titolo… |

## Errori {#section_jbc_vj4_xz}

Stringhe disponibili per messaggi di errore generali.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| Errori |  |  |
|  | errorAlreadyPosted | Puoi pubblicare una sola recensione. |
|  | errorAuthError | Non sei autorizzato a pubblicare una recensione su questa conversazione |
|  | errorCommentsNotAllowed | Impossibile pubblicare le recensioni in questo momento |
|  | errorDislikeOwnComment | Non puoi disgradire la tua recensione |
|  | errorDuplicate | Per quanto ti sia piaciuta la tua recensione, non sei autorizzato a pubblicarla due volte. |
|  | errorEditDuplicate | È necessario modificare il corpo della revisione quando la si modifica. |
|  | errorEditNotAllowed | In questa conversazione non è consentito modificare le revisioni. |
|  | errorEditTimeSuperato | Il periodo di modifica della revisione è scaduto. |
|  | errorEmpty | Sembra che tu stia tentando di pubblicare una revisione vuota. |
|  | errorEmptyTitle | Sembra che tu stia tentando di pubblicare un titolo vuoto |
|  | errorFieldRating | classificazione a stella |
|  | errorFieldReview | revisione |
|  | errorFieldTitle | title |
|  | errorMaxChars | Spiacente, la tua recensione è troppo lunga. Modifica e riprova. |
|  | errorMissingFields | Inserisci un |
|  | errorRatingEmpty | Non è possibile inviare una valutazione vuota |
|  | errorRatingNotSet | Tutte le valutazioni devono essere impostate |
|  | errorRatingNotValid | La valutazione deve essere un oggetto |
|  | errorShowMore | Errore durante il caricamento di più recensioni. |
|  | errorTitleMaxChars | Il tuo titolo è troppo lungo. Modifica e riprova. |
|  | errorvoteOwnComment | Non puoi votare da solo |

## Stringhe di testo a margine {#c_sidenotes_text_strings}

Personalizzazione delle stringhe di testo per Livefyre Sidenotes

<!-- 

c_sidenotes_text_strings.dita

 -->

Questa pagina elenca e descrive tutte le stringhe disponibili per la personalizzazione nelle app Sidenotes. Per informazioni sulle stringhe disponibili per le app di base Livefyre, consulta Personalizzazioni di stringhe .

* Implementazione
* Auth
* Informazioni flusso
* Informazioni sull’autore/contenuto
* Azioni utente
* Funzioni post
* Interfaccia moderatore
* Errori

## Implementazione {#section_wp2_ql4_xz}

Per implementare questa funzione, passa una mappatura oggetto 1-1 delle stringhe che desideri ignorare all&#39;oggetto di configurazione Javascript. Se non si fornisce un campo, verrà utilizzato il testo predefinito.

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

Stringhe disponibili per il processo di autenticazione e dai menu utente autenticati.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| *Stringhe del menu di autenticazione* |  |  |
|  | menuAuthSignInBtn | Accedere |
|  | menuAuthSignedInMsg | Devi effettuare l&#39;accesso a {action} |
|  | menuUserEditProfile | Modifica profilo |
|  | menuUserAdmin | Admin Console |
|  | menuUserLogout | Disconnetti |
|  | menuUserBackBtn | Tutte |

## Informazioni flusso {#section_wpy_gl4_xz}

Stringhe disponibili per le informazioni e la visualizzazione del flusso di contenuto.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| *Opzioni del menu Informazioni* |  |  |
|  | menuInfoCopyright | © Livefyre, Inc. 2014 |
|  | menuInfoHelp | Aiuto |
|  | menuInfoLivefyreLink | Visita Livefyre.com |

## Informazioni sull’autore/contenuto {#section_dhb_gl4_xz}

Impostazioni disponibili per informazioni sull’autore e sui singoli contenuti.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
|  | commentModeratorTag | Mod |
|  | commentPendingTag | In sospeso |
|  | commentReadMoreLink | Ulteriori informazioni |
|  | commentReplyLink | Vedi {number} risposte |
|  | commentReplyLinkSing | Vedi risposta |
|  | commentCount | voti |
|  | commentCountSing | votare |
|  | datetimeMinutePrefix | m |
|  | datetimeMonths | *Un array. Predefinito = *[ &quot;gennaio&quot;, &quot;febbraio&quot;, &quot;marzo&quot;, &quot;aprile&quot;, &quot;maggio&quot;, &quot;giugno&quot;, &quot;luglio&quot;, &quot;agosto&quot;, &quot;settembre&quot;, &quot;ottobre&quot;, &quot;novembre&quot;, &quot;dicembre&quot; ] |
|  | domandaSpiegazione | Ora è possibile leggere e scrivere commenti direttamente su frasi, paragrafi, immagini e citazioni. <br>Evidenzia il testo e fai clic sull’icona o fai clic sull’icona alla fine di ciascun paragrafo. |
|  | QuestionMockText | Ciò che è &quot;noto a tutti&quot; non è ben noto, solo per il motivo che è &quot;familiare&quot;. |
|  | QuestionTitle | Cos&#39;è un Sidenote? |

## Azioni utente {#section_qxd_fl4_xz}

Stringhe disponibili per le azioni dell’utente: creazione di flag, condivisione e collegamento di contenuti esistenti.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| *Opzioni del menu Risposta* |  |  |
|  | menuRepliesViewTitle | Dettagli |
|  | menuRepliesViewReply | Risposta alla conversazione |
| *Opzioni del menu Condividi* |  |  |
|  | menuShareOptionFacebook | Facebook |
|  | menuShareOptionTwitter | Twitter |
|  | menuShareTitle | Condividi |
| *Opzioni del menu Contrassegna* |  |  |
|  | menuFlagOptionNonD | Non concordo |
|  | menuFlagOptionOffensive | Offensivo |
|  | menuFlagOptionOffTopic | Argomento disattivato |
|  | menuFlagOptionSpam | Spam |
|  | menuFlagTitle | Contrassegna come.. |
|  | facebookShareCaption | Note a margine su &quot;{title}&quot; |
| *Opzioni utente mobile* |  |  |
|  | sliderCommentTally | di |
|  | sliderInviteRead | Letto |
|  | sliderInviteWrite | Scrivi |
|  | sliderLoading | Caricamento in corso... |
|  | sliderWriteText | Cosa ne pensate? Tocca per scrivere. |

## Funzioni post {#section_xzf_2l4_xz}

Stringhe disponibili per gli utenti che pubblicano contenuti.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
|  | editorEditBtn | Salva |
|  | editorEditPosting | Salvataggio in corso.. |
|  | editorEditReplyTitle | Modifica risposta |
|  | editorEditTitle | Modifica pannello laterale |
|  | editorPlaceholder | Cosa ne pensate? |
|  | editorPostBtn | Post Sidenote |
|  | editorPostBtnMobile | Post |
|  | editorPosting | Registrazione in corso.. |
|  | editorReplyBtn | Pubblica risposta |
|  | editorReplyTitle | Scrivi risposta |
|  | editorTitle | Scrivi Sidenote |
|  | emptyImageBlockTxt | Cosa ne pensate? |
|  | emptyTextBlockTxt | + |
|  | responseBtn | Rispondi |
|  | threadReplyBtn | Risposta alla conversazione |
| *Opzioni del menu Elimina* |  |  |
|  | menuConfirmAccept | Sì, {action} |
|  | menuConfirmCancel | Annulla |
|  | menuConfirmTitle | Sei sicuro? |
| *Opzioni del menu Ecc* |  |  |
|  | menuEtcOptionApprove | Approva |
|  | menuEtcOptionDelete | Elimina |
|  | menuEtcOptionEdit | Modificare       |
|  | menuEtcOptionFlag | Contrassegna |
|  | menuEtcOptionShare | Condividi |
|  | menuEtcPostedAt | Pubblicato il {date} |
|  | menuEtcTitle | Altro |

## Interfaccia moderatore {#section_o5f_dl4_xz}

Stringhe disponibili per l&#39;interfaccia del moderatore autenticato dall&#39;utente.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| *Messaggi di conferma dal menu Altro* |  |  |
|  | notificationApproved | Approvato |
|  | notificationDeleted | Eliminato |
|  | notificationFlagged | Segnalato |

## Errori {#section_gtk_cl4_xz}

Stringhe disponibili per messaggi di errore generali.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
|  | errorConnection | Uh oh. Sembra che tu non abbia una buona connessione. |
|  | errorDuplicate | Anche a noi piace la tua nota, ma non puoi pubblicarla due volte. |
|  | errorGeneral | Errore. Riprova. |
|  | errorServer | Si è verificato un problema con il nostro server. Provate ancora? |
