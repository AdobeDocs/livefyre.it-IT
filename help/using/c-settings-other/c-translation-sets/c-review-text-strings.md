---
description: Personalizzazione delle stringhe di testo per le recensioni di Livefyre.
title: Rivedi stringhe di testo
exl-id: 82ced091-d573-4514-9b91-3451a94ed5d3
source-git-commit: 1d9088eecf797e1af881cb6be55b3c96284f75e5
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 5%

---

# Rivedi stringhe di testo{#review-text-strings}

Personalizzazione delle stringhe di testo per le recensioni di Livefyre.

Questa pagina elenca e descrive le stringhe disponibili per la personalizzazione nelle app di revisione. Le stringhe elencate qui sono in aggiunta e sostituiscono le stringhe predefinite per le app di base Livefyre, elencate in Personalizzazioni di stringhe. Se sono elencati i duplicati, le stringhe elencate in queste tabelle sono quelle predefinite per le app Reviews.

Implementazione
Interfaccia di revisione/valutazione
Informazioni flusso
Informazioni sull’autore/contenuto
Azioni utente
Funzioni post
Errori

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
|--- |--- |--- |
| Pulsanti | editReviewBtn | Modifica revisione |
|  | reviewBtn | Revisione in scrittura |
|  | recensioniChiuso | Recensioni chiuse |
|  | showReviewBtn | Mostra revisione |
|  | seguire | Sono interessato |
|  | shareText | Ho appena scritto una recensione. Guardate! |
| Descrizioni comandi di valutazione | ratingValues | Un array. Predefinito = `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`; <br>Nota: I valori nella matrice devono essere duplicati per assegnare lo stesso nome sia alla metà sinistra che alla metà destra di ogni stella. |
| Sottoparti di valutazione | ratingSubpartPlaceholder | Un array. Impostazione predefinita = `[]` |
|  | ratingSubpartTitles | Un array. Impostazione predefinita = `[]` |
|  | reviewStreamTitle | Vuoto per impostazione predefinita. Titolo della sezione di riepilogo della revisione. |
| Varie | averageRating | Valutazione media utente |
|  | suddivisioneHeader | Suddivisione dei rating |
|  | utile | %s di %s trovato utile |
|  | helpPlural | %s di %s trovato utile |
|  | outOf | / |
|  | ratingType | stella |

## Informazioni flusso {#section_wmv_yj4_xz}

Stringhe disponibili per le informazioni e la visualizzazione del flusso di contenuto.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| Ordinamento | sortBy | Vuoto per impostazione predefinita. |
|  | sortHighestRated | Valutazione più elevata |
|  | sortLowestRated | Classificazione più bassa |
|  | sortMostHelpful | Più utile |
| Flusso varie. | showMore | Mostra altro |
| Velocità elevata del flusso | newComment | Nuova revisione |
|  | newComments | Nuove recensioni |
| Conteggi listener | listenerCount | ascolto personale |
|  | listenerCountPlural | gente che ascolta |
| Conteggi dei commenti | commentCountLabel | LiveReviews<strong> | </strong>%s |
|  | commentCountLabelPlural | LiveReviews<strong> | </strong>%s |
| Conteggi dei notificatori dei commenti | commentNotifier | Nuova revisione |
|  | commentNotifierPlural | Nuove recensioni |

## Informazioni sull’autore/contenuto {#section_osx_xj4_xz}

Impostazioni disponibili per informazioni sull’autore e sui singoli contenuti.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| Suddivisione dei thread | reviewContentNotFoundMsg | Questa revisione non è più visibile |
|  | backToComments | Torna a Recensioni |

## Azioni utente {#section_tlx_wj4_xz}

Stringhe disponibili per le azioni dell’utente: puoi assegnare tag, condividere e contrassegnare i contenuti esistenti come utili.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| Piè di pagina commento | wasReviewHelpful | Utile? |
|  | wasReviewHelpfulMobile | Utile? |
|  | ownwasReviewHelpful | Trovato utile. |
|  | reviewwasHelpful | Sì |
|  | helpDivider | &amp;vert; |
|  | reviewWASNotHelpful | No |
| Votazione modale | voteTitle | Questa recensione è stata utile? |
|  | voteDownvote | No |
|  | voteReplyTitle | Questa risposta è stata utile? |
|  | voteTitle | Questo commento è stato utile? |
|  | voteUpvote | Sì |
| Flag modale | flagTitle | Contrassegna la revisione di %s |
|  | flagSuccessMsg | La revisione è stata contrassegnata. |
| Flag Mobile | flagConfirmationMessage | Contrassegna la revisione di %s come %s? |
| Modale di menzione | mentionDefaultText | Ti ho menzionato in una recensione di Livefyre! |
| Condividi modale | shareTitle | Condividi revisione |

## Funzioni post {#section_yl1_wj4_xz}

Stringhe disponibili per gli utenti che pubblicano le revisioni.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| Editor | bodyPlaceholder | Scrivi recensione... |
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
| Errori | errorAlreadyPosted | Puoi pubblicare una sola recensione. |
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
