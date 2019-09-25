---
description: Personalizzazione delle stringhe di testo per Livefyre Reviews.
seo-description: Personalizzazione delle stringhe di testo per Livefyre Reviews.
seo-title: Rivedi stringhe di testo
solution: Experience Manager
title: Rivedi stringhe di testo
uuid: 86251e49-bc73-4eec-9f9b-b4b0a5b42099
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Rivedi stringhe di testo{#review-text-strings}

Personalizzazione delle stringhe di testo per Livefyre Reviews.

Questa pagina elenca e descrive le stringhe disponibili per la personalizzazione nelle app di revisione. Le stringhe elencate di seguito sono oltre alle stringhe predefinite per le app di base Livefyre e sostituiscono tali stringhe, elencate in String Customizations. Se sono elencati i duplicati, le stringhe elencate in queste tabelle sono le stringhe predefinite per le app di revisione.

ImplementationReview/Rating InterfaceStream InfoAuthor/Content InfoUser ActionsPost FunctionsErrors

## Implementazione {#section-vsy-1k4-xz}

Per implementare questa funzione, trasmettere una mappatura oggetto 1-1 delle stringhe che si desidera ignorare all'oggetto di configurazione Javascript. Se non si fornisce un campo, verrà utilizzato il testo predefinito.

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

## Interfaccia revisione/valutazione {#section_iyv_zj4_xz}

Stringhe disponibili per l'interfaccia utente Revisione e Valutazione.

| Elemento | Chiave | Testo predefinito |
|--- |--- |--- |
| Pulsanti | editReviewBtn | Modifica revisione |
|  | reviewBtn | [Scrivi recensione](https://d.pr/i/QscA) |
|  | reviewClosed | [Recensioni chiuse](https://d.pr/i/zr7M) |
|  | showReviewBtn | [Mostra revisione](https://d.pr/i/onxU) |
|  | follow | Sono interessato |
|  | shareText | Ho appena scritto una recensione. Guardate! |
| Descrizioni comandi di valutazione | ratingValues | Un array. Default = `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`; <br>Nota: I valori nella matrice devono essere duplicati per assegnare lo stesso nome sia alla metà sinistra che alla metà destra di ciascuna stella. |
| Sottoparti valutazione | ratingSubpartPlaceholder | Un array. Impostazione predefinita = `[]` |
|  | ratingSubpartTitles | Un array. Impostazione predefinita = `[]` |
|  | reviewStreamTitle | Vuoto per impostazione predefinita. Titolo della sezione di riepilogo della revisione. |
| Misc | averageRating | [Valutazione utente media](https://d.pr/i/QscA) |
|  | destHeader | [Suddivisione valutazione](https://d.pr/i/QscA) |
|  | assist | %s di %s trovato utile |
|  | assistPlural | %s di %s trovato utile |
|  | outOf | / |
|  | ratingType | star |

## Informazioni flusso {#section_wmv_yj4_xz}

Stringhe disponibili per le informazioni e la visualizzazione del flusso di contenuto.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| Ordinamento | sortBy | Vuoto per impostazione predefinita. |
|  | sortHighestRated | [Valutazione più alta](https://d.pr/i/huTd) |
|  | sortLowestRated | [Valutazione più bassa](https://d.pr/i/huTd) |
|  | sortMostHelpful | [Molto utili](https://d.pr/i/huTd) |
| Flusso diverso. | showMore | Mostra altro |
| Velocità elevata flusso | newComment | Nuova revisione |
|  | newComments | Nuove recensioni |
| Conteggio listener | listenerCount | persona che ascolta |
|  | listenerCountPlural | gente che ascolta |
| Conteggio commenti | commentCountLabel | LiveReviews<strong> | </strong>%s |
|  | commentCountLabelPlural | LiveReviews<strong> | </strong>%s |
| Conteggio dei notifier dei commenti | commentNotifier | Nuova revisione |
|  | commentNotifierPlural | Nuove recensioni |

## Autore/Informazioni contenuto {#section_osx_xj4_xz}

Impostazioni disponibili per le informazioni sull’autore e i singoli contenuti.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| Suddivisione thread | reviewContentNotFoundMsg | [Questa revisione non è più visibile](https://d.pr/i/svXs) |
|  | backToComments | Torna alle recensioni |

## Azioni utente {#section_tlx_wj4_xz}

Stringhe disponibili per le azioni dell'utente: potete contrassegnare i contenuti, condividerli e contrassegnarli come utili.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| Piè di pagina commento | wasReviewHelpful | [Utile?](https://d.pr/i/Q0mA) |
|  | wasReviewHelpfulMobile | Utile? |
|  | ownIsReviewHelpful | [Trovato utile.](https://d.pr/i/Q0mA) |
|  | reviewwasHelpful | [Sì](https://d.pr/i/Q0mA) |
|  | helpDivider | [&amp;vert;](https://d.pr/i/Q0mA) |
|  | reviewwasNotHelpful | [No](https://d.pr/i/Q0mA) |
| Votazione modale | votiTitle | Questa revisione è stata utile? |
|  | VotazioneDownVoto | No |
|  | answerTitle | Questa risposta è stata utile? |
|  | votiTitle | Questo commento è stato utile? |
|  | votiUpvote | Sì |
| Contrassegno modale | flagTitle | Flag %s revisione |
|  | flagSuccessMsg | La revisione è stata contrassegnata. |
| Flag Mobile | flagConfirmMessage | Flag %s revisione come %s? |
| Menzione modale | namedDefaultText | Ti ho menzionato in una recensione di Livefyre! |
| Condivisione modale | shareTitle | Condividi revisione |

## Funzioni di post {#section_yl1_wj4_xz}

Stringhe disponibili per gli utenti che pubblicano le revisioni.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| Editor | bodyPlaceholder | Scrivi recensione... |
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
|  Errori | errorAlreadyPosted | È possibile pubblicare una sola revisione. |
|  | errorAuthError | Non sei autorizzato a pubblicare una revisione su questa conversazione |
|  | errorCommentsNotAllowed | Al momento non è possibile pubblicare le recensioni |
|  | errorDislikeOwnComment | Non puoi rifiutare la tua revisione |
|  | errorDuplicate | Per quanto vi sia piaciuta la recensione, non potete pubblicarla due volte. |
|  | errorEditDuplicate | È necessario modificare il corpo della revisione al momento della modifica. |
|  | errorEditNotAllowed | In questa conversazione non è consentito modificare le revisioni. |
|  | errorEditTimeExceeded | Il periodo di modifica della revisione è scaduto. |
|  | errorEmpty | Si sta tentando di pubblicare una revisione vuota. |
|  | errorEmptyTitle | Si sta tentando di inserire un titolo vuoto |
|  | errorFieldRating | classificazione a stella |
|  | errorFieldReview | review |
|  | errorFieldTitle | title |
|  | errorMaxChars | Spiacenti, la tua recensione è troppo lunga. Modificare e riprovare. |
|  | errorMissingFields | Immettere un |
|  | errorRatingEmpty | Non è possibile inviare una valutazione vuota |
|  | errorRatingNotSet | Tutte le valutazioni devono essere impostate |
|  | errorRatingNotInvalid | La valutazione deve essere un oggetto |
|  | errorShowMore | Errore durante il caricamento di più revisioni. |
|  | errorTitleMaxChars | Il titolo è troppo lungo. Modificare e riprovare. |
|  | errorVoteOwnComment | Non puoi votare da solo |

