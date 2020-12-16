---
description: I set di traduzioni consentono di specificare la lingua alternativa per le app.
seo-description: I set di traduzioni consentono di specificare la lingua alternativa per le app.
seo-title: Set di traduzioni
solution: Experience Manager
title: Set di traduzioni
uuid: 8ba66a61-5520-482a-bc0b-e4f6b57f1744
translation-type: tm+mt
source-git-commit: 366b7248c2f3b6994fa10419599e66fa1c8e5e48
workflow-type: tm+mt
source-wordcount: '1355'
ht-degree: 5%

---


# Set di traduzioni {#translation-sets}

I set di traduzioni consentono di specificare la lingua alternativa per le app.

<!-- 
c_translation_sets.dita
-->

Utilizzate le impostazioni di traduzione per localizzare le app in diverse lingue o per specificare testo alternativo per più app da una posizione in Studio. Ad esempio, puoi fare in modo che tutti i siti in lingua spagnola utilizzino la lingua spagnola per tutti i campi App. È inoltre possibile modificare il testo in modo che tutti i campi corrispondano alla voce e al comportamento del sito o della rete.

Potete specificare le impostazioni di conversione per tutte le app, eccetto Storify 2. Per ulteriori informazioni sui campi che è possibile localizzare, vedere [Localize Strings](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md).

Commenti, Live Blog e Chat condividono lo stesso set di stringhe all&#39;interno di un set di traduzioni.

Specificate un set di traduzione per una rete, un sito, un&#39;app o per l&#39;utilizzo di un&#39;API.

I set di conversione a diversi livelli si ignorano a vicenda seguendo questo pattern:

* Il set di conversione API ha la precedenza su qualsiasi set di conversione a qualsiasi livello (app, rete e sito)
* Il set di conversione delle app ha la precedenza sui set di traduzione a livello di rete e di sito.
* I set di conversione a livello di sito ignorano i set di conversione a livello di rete.

## Rivedi stringhe di testo {#c-review-text-strings}

Personalizzazione delle stringhe di testo per Livefyre Reviews.

Questa pagina elenca e descrive le stringhe disponibili per la personalizzazione nelle app di revisione. Le stringhe elencate di seguito sono oltre alle stringhe predefinite per le app di base Livefyre e sostituiscono tali stringhe, elencate in String Customizations. Se sono elencati i duplicati, le stringhe elencate in queste tabelle sono le stringhe predefinite per le app di revisione.

* Implementazione
* Interfaccia di revisione/valutazione
* Informazioni flusso
* Autore/Informazioni contenuto
* Azioni utente
* Funzioni di post
* Errori

## Implementazione {#section-vsy-1k4-xz}

Per implementare questa funzione, trasmettere una mappatura oggetto 1-1 delle stringhe che si desidera ignorare all&#39;oggetto di configurazione Javascript. Se non si fornisce un campo, verrà utilizzato il testo predefinito.

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

Stringhe disponibili per l&#39;interfaccia utente Revisione e Valutazione.

| Elemento | Chiave | Testo predefinito |
| --------------- | ------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| Pulsanti |  |  |
|  | editReviewBtn | Modifica revisione |
|  | reviewBtn | Scrivi recensione |
|  | reviewClosed | Recensioni chiuse |
|  | showReviewBtn | Mostra revisione |
|  | follow | Sono interessato |
|  | shareText | Ho appena scritto una recensione. Guardate! |
| Descrizioni comandi di valutazione |  |  |
|  | ratingValues | Un array. Default = [&quot;Poor&quot;, &quot;Poor&quot;, &quot;Fair&quot;, &quot;Fair&quot;, &quot;Average&quot;, &quot;Average&quot;, &quot;Good&quot;, &quot;Good&quot;, &quot;Excellent&quot;, &quot;Excellent&quot;]; |
|  |  | Nota: i valori nell&#39;array devono essere duplicati per assegnare lo stesso nome sia alla metà sinistra che alla metà destra di ciascuna stella. |
| Sottoparti valutazione |  |  |
|  | ratingSubpartPlaceholder | Un array. Impostazione predefinita = [] |
|  | ratingSubpartTitles | Un array. Impostazione predefinita = [] |
|  | reviewStreamTitle | Vuoto per impostazione predefinita. Titolo della sezione riepilogativa della revisione. |
| Misc |  |  |
|  | averageRating | Valutazione utente media |
|  | destHeader | Suddivisione valutazione |
|  | assist | %s di %s trovato utile |
|  | assistPlural | %s di %s trovato utile |
|  | outOf | / |
|  | ratingType | star |

## Informazioni flusso {#section_wmv_yj4_xz}

Stringhe disponibili per le informazioni e la visualizzazione del flusso di contenuto.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| *Ordinamento* |  |  |
|  | sortBy | *Vuoto per impostazione predefinita.* |
|  | sortHighestRated | [Valutazione più alta](https://d.pr/i/huTd) |
|  | sortLowestRated | [Valutazione più bassa](https://d.pr/i/huTd) |
|  | sortMostHelpful | [Molto utili](https://d.pr/i/huTd) |
| *Flusso diverso.* |  |  |
|  | showMore | Mostra altro |
| *Velocità elevata flusso* |  |  |
|  | newComment | Nuova revisione |
|  | newComments | Nuove recensioni |
| *Conteggio listener* |  |  |
|  | listenerCount | persona che ascolta |
|  | listenerCountPlural | persone che ascoltano |
| *Conteggio commenti* |  |  |
|  | commentCountLabel | LiveReviews |
|  | commentCountLabelPlural | LiveReviews |
| *Conteggio dei notifier dei commenti* |  |  |
|  | commentNotifier | Nuova revisione |
|  | commentNotifierPlural | Nuove recensioni |

## Autore / Informazioni contenuto {#section_osx_xj4_xz}

Impostazioni disponibili per le informazioni sull’autore e i singoli contenuti.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| *Suddivisione thread* |  |  |
|  | reviewContentNotFoundMsg | [Questa revisione non è più visibile](https://d.pr/i/svXs) |
|  | backToComments | Torna alle recensioni |

## Azioni utente {#section_tlx_wj4_xz}

Stringhe disponibili per le azioni dell&#39;utente: potete contrassegnare i contenuti, condividerli e contrassegnarli come utili.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| *Piè di pagina commento* |  |  |
|  | wasReviewHelpful | [Utile?](https://d.pr/i/Q0mA) |
|  | wasReviewHelpfulMobile | Utile? |
|  | ownIsReviewHelpful | [Trovato utile.](https://d.pr/i/Q0mA) |
|  | reviewwasHelpful | [Sì](https://d.pr/i/Q0mA) |
|  | helpDivider | [&amp;vert;](https://d.pr/i/Q0mA) |
|  | reviewwasNotHelpful | [No](https://d.pr/i/Q0mA) |
| *Votazione modale* |  |  |
|  | votiTitle | Questa revisione è stata utile? |
|  | VotazioneDownVoto | No |
|  | answerTitle | Questa risposta è stata utile? |
|  | votiTitle | Questo commento è stato utile? |
|  | votiUpvote | Sì |
| *Contrassegno modale* |  |  |
|  | flagTitle | Flag %s revisione |
|  | flagSuccessMsg | La revisione è stata contrassegnata. |
| *Flag Mobile* |  |  |
|  | flagConfirmMessage | Flag %s revisione come %s? |
| *Menzione modale* |  |  |
|  | namedDefaultText | Ti ho menzionato in una recensione di Livefyre! |
| *Condivisione modale* |  |  |
|  | shareTitle | Condividi revisione |

## Funzioni post {#section_yl1_wj4_xz}

Stringhe disponibili per gli utenti che pubblicano le revisioni.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| *Editor* |  |  |
|  | bodyPlaceholder | Scrivi recensione... |
|  | postEditButton | Modificare       |
|  | postEditCancelButton | Annulla |
|  | postAsButton | Post review as... |
|  | postButton | Post review |
|  | postReplyAsButton | Invia come... |
|  | postReplyButton | Post |
|  | shareButton | Condividi |
|  | titlePlaceholder | Titolo… |

## Errori {#section_jbc_vj4_xz}

Stringhe disponibili per i messaggi di errore generali.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| Errori |  |  |
|  | errorAlreadyPosted | È possibile pubblicare una sola revisione. |
|  | errorAuthError | Non sei autorizzato a pubblicare una revisione su questa conversazione |
|  | errorCommentsNotAllowed | Al momento non è possibile pubblicare le recensioni |
|  | errorDislikeOwnComment | Non puoi rifiutare la tua revisione |
|  | errorDuplicate | Per quanto vi sia piaciuta la recensione, non potete pubblicarla due volte. |
|  | errorEditDuplicate | È necessario modificare il corpo della revisione al momento della modifica. |
|  | errorEditNotAllowed | In questa conversazione non è consentito modificare le revisioni. |
|  | errorEditTimeExceeded | Il periodo di modifica della revisione è scaduto. |
|  | errorEmpty | Si sta tentando di pubblicare una revisione vuota. |
|  | errorEmptyTitle | Sembra che stiate tentando di inserire un titolo vuoto |
|  | errorFieldRating | classificazione a stella |
|  | errorFieldReview | review |
|  | errorFieldTitle | title |
|  | errorMaxChars | Spiacenti, la tua recensione è troppo lunga. Modificare e riprovare. |
|  | errorMissingFields | Immettere un |
|  | errorRatingEmpty | Non è possibile inviare una valutazione vuota |
|  | errorRatingNotSet | Tutte le valutazioni devono essere impostate |
|  | errorRatingNotInvalid | La valutazione deve essere un oggetto |
|  | errorShowMore | Si è verificato un errore durante il caricamento di più revisioni. |
|  | errorTitleMaxChars | Il titolo è troppo lungo. Modificare e riprovare. |
|  | errorVoteOwnComment | Non puoi votare da solo |

## Note delle stringhe di testo {#c_sidenotes_text_strings}

Personalizzazione delle stringhe di testo per Livefyre Sidenotes

<!-- 

c_sidenotes_text_strings.dita

 -->

Questa pagina elenca e descrive tutte le stringhe disponibili per la personalizzazione nelle app Sidenotes. Per informazioni sulle stringhe disponibili per le app Livefyre di base, consultate Personalizzazioni delle stringhe.

* Implementazione
* Auth
* Informazioni flusso
* Autore/Informazioni contenuto
* Azioni utente
* Funzioni di post
* Interfaccia Moderatore
* Errori

## Implementazione {#section_wp2_ql4_xz}

Per implementare questa funzione, trasmettere una mappatura oggetto 1-1 delle stringhe che si desidera ignorare all&#39;oggetto di configurazione Javascript. Se non si fornisce un campo, verrà utilizzato il testo predefinito.

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
|  | menuAuthSignInBtn | Accedi |
|  | menuAuthSignedInMsg | È necessario aver effettuato l&#39;accesso a {action} |
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

## Autore / Informazioni contenuto {#section_dhb_gl4_xz}

Impostazioni disponibili per le informazioni sull’autore e i singoli contenuti.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
|  | commentModeratorTag | Mod |
|  | commentPendingTag | In sospeso |
|  | commentReadMoreLink | Leggi tutto |
|  | commentReplyLink | Vedere {number} risposte |
|  | commentReplyLinkSing | Vedere la risposta |
|  | commentVoteCount | voti |
|  | commentCountSing | Votazione |
|  | datetimeMinutePrefix | m |
|  | datetimeMonths | *Un array. Valore predefinito = *[ &quot;gennaio&quot;, &quot;febbraio&quot;, &quot;marzo&quot;, &quot;aprile&quot;, &quot;maggio&quot;, &quot;giugno&quot;, &quot;luglio&quot;, &quot;agosto&quot;, &quot;settembre&quot;, &quot;ottobre&quot;, &quot;novembre&quot;, &quot;dicembre&quot; ] |
|  | questionExplanation | Ora è possibile leggere e scrivere commenti direttamente su frasi, paragrafi, immagini e citazioni. <br>Evidenzia il testo e fai clic sull’icona o fai clic sull’icona alla fine di ciascun paragrafo. |
|  | questionMockText | Ciò che è &quot;familiare&quot; non è ben noto, solo per il motivo che è &quot;familiare&quot;. |
|  | questionTitle | Cos&#39;è una Sidenote? |

## Azioni utente {#section_qxd_fl4_xz}

Stringhe disponibili per le azioni dell&#39;utente: applicazione di flag, condivisione e collegamento ai contenuti esistenti.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| *Opzioni del menu Rispondi* |  |  |
|  | menuRepliesViewTitle | Dettagli |
|  | menuRepliesViewReply | Rispondi alla conversazione |
| *Opzioni del menu Condividi* |  |  |
|  | menuShareOptionFacebook | Facebook |
|  | menuShareOptionTwitter | Twitter |
|  | menuShareTitle | Condividi |
| *Opzioni del menu Contrassegno* |  |  |
|  | menuFlagOptionDisagreement | Non d&#39;accordo |
|  | menuFlagOptionOffensive | Offensivo |
|  | menuFlagOptionOffTopic | Disattiva argomento |
|  | menuFlagOptionSpam | Spam |
|  | menuFlagTitle | Contrassegna come... |
|  | facebookShareCaption | Note su &quot;{title}&quot; |
| *Opzioni utente per dispositivi mobili* |  |  |
|  | sliderCommentTally | di |
|  | sliderInviteRead | Letto |
|  | sliderInviteWrite | Write |
|  | sliderLoading | Caricamento in corso... |
|  | sliderWriteText | Che ne pensa? Toccate per scrivere. |

## Funzioni post {#section_xzf_2l4_xz}

Stringhe disponibili per gli utenti che pubblicano contenuti.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
|  | editorEditBtn | Salva |
|  | editorEditPosting | Salvataggio in corso... |
|  | editorEditReplyTitle | Modifica risposta |
|  | editorEditTitle | Modifica Sidenote |
|  | editorPlaceholder | Che ne pensa? |
|  | editorPostBtn | Post Sidenote |
|  | editorPostBtnMobile | Post |
|  | editorPosting | Registrazione in corso... |
|  | editorReplyBtn | Pubblica risposta |
|  | editorReplyTitle | Scrivi risposta |
|  | editorTitle | Scrivi Sidenote |
|  | emptyImageBlockTxt | Che ne pensa? |
|  | emptyTextBlockTxt | + |
|  | replyBtn | Rispondi |
|  | threadReplyBtn | Rispondi alla conversazione |
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
|  | notificationEnabled | Approvato |
|  | notificationDeleted | Eliminato |
|  | notificationFlagged | Segnalato |

## Errori {#section_gtk_cl4_xz}

Stringhe disponibili per i messaggi di errore generali.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
|  | errorConnection | Oh-oh. Non sembra che tu abbia una buona connessione. |
|  | errorDuplicate | Anche la nota è gradita, ma non può essere pubblicata due volte. |
|  | errorGeneral | Si è verificato un errore. Prova ancora. |
|  | errorServer | Si è verificato un problema con il nostro server. Provi ancora? |
