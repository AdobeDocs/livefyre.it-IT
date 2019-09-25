---
description: Personalizzazione delle stringhe di testo per Livefyre Sidenotes
seo-description: Personalizzazione delle stringhe di testo per Livefyre Sidenotes
seo-title: Note Di Testo Stringhe
solution: Experience Manager
title: Note Di Testo Stringhe
uuid: a3735237-e55d-4bc0-b88d-8a323980ee09
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Note Di Testo Stringhe{#sidenotes-text-strings}

Personalizzazione delle stringhe di testo per Livefyre Sidenotes

Questa pagina elenca e descrive tutte le stringhe disponibili per la personalizzazione nelle app Sidenotes. Per informazioni sulle stringhe disponibili per le app Livefyre di base, consultate Personalizzazioni delle stringhe.

ImplementationAuthStream InfoAuthor / Content InfoUser ActionsPost FunctionsModerator InterfaceErrors

## Implementazione {#section_wp2_ql4_xz}

Per implementare questa funzione, trasmettere una mappatura oggetto 1-1 delle stringhe che si desidera ignorare all'oggetto di configurazione Javascript. Se non si fornisce un campo, verrà utilizzato il testo predefinito.

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
| Stringhe del menu di autenticazione | menuAuthSignInBtn | Accedi |
|  | menuAuthSignedInMsg | È necessario aver effettuato l'accesso a {action} |
|  | menuUserEditProfile | Modifica profilo |
|  | menuUserAdmin | Admin Console |
|  | menuUserLogout | Disconnetti |
|  | menuUserBackBtn | Tutte |

## Informazioni flusso {#section_wpy_gl4_xz}

Stringhe disponibili per le informazioni e la visualizzazione del flusso di contenuto.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| Opzioni del menu Informazioni | menuInfoCopyright | © Livefyre, Inc. 2014 |
|  | menuInfoHelp | Aiuto |
|  | menuInfoLivefyreLink | Visita Livefyre.com |

## Autore/Informazioni contenuto {#section_dhb_gl4_xz}

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
|  | datetimeMonths | Un array. Impostazione predefinita =`[‘January’, ‘February’, ‘March’, ‘April’, ‘May’, ‘June’, ‘July’, ‘August’, ‘September’, ‘October’, ‘November’, ‘December’]` |
|  | questionExplanation | Ora è possibile leggere e scrivere commenti direttamente su frasi, paragrafi, immagini e citazioni.<br><br><span class="&rdquo;lf-highlight-text&rdquo;">Evidenzia il testo</span> e fai clic sull’ <span class="&rdquo;fycon-write&rdquo;"></span> icona o fai clic sull’ <span class="&rdquo;fycon-action-view&rdquo;"></span> icona alla fine di ciascun paragrafo. |
|  | questionMockText | Ciò che è "familiare" non è ben noto, solo per il motivo che è "familiare". |
|  | questionTitle | Cos'è una Sidenote? |

## Azioni utente {#section_qxd_fl4_xz}

Stringhe disponibili per le azioni dell'utente: applicazione di flag, condivisione e collegamento ai contenuti esistenti.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| Opzioni del menu Rispondi | menuRepliesViewTitle | Dettagli |
|  | menuRepliesViewReply | Rispondi alla conversazione |
| Opzioni del menu Condividi | menuShareOptionFacebook | Facebook |
|  | menuShareOptionTwitter | Twitter |
|  | menuShareTitle | Condividi |
| Opzioni del menu Flag | menuFlagOptionDisagreement | Non d'accordo |
|  | menuFlagOptionOffensive | Offensivo |
|  | menuFlagOptionOffTopic | Disattiva argomento |
|  | menuFlagOptionSpam | Spam |
|  | menuFlagTitle | Contrassegna come... |
|  | facebookShareCaption | Note su "{title}" |
| Opzioni utente per dispositivi mobili | sliderCommentTally | di |
|  | sliderInviteRead | Letto |
|  | sliderInviteWrite | Write |
|  | sliderLoading | Caricamento in corso... |
|  | sliderWriteText | Che ne pensa? Toccate per scrivere. |

## Funzioni di post {#section_xzf_2l4_xz}

Stringhe disponibili per gli utenti che pubblicano contenuti.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
|  | editorEditBtn | Salva |
|  | editorEditPosting | Salvataggio in corso... |
|  | editorEditReplyTitle | Modifica risposta |
|  | editorEditTitle | Modifica pannello |
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
| Opzioni del menu Elimina | menuConfirmAccept | Sì, {action} |
|  | menuConfirmCancel | Annulla |
|  | menuConfirmTitle | Sei sicuro? |
| Opzioni del menu Ecc | menuEtcOptionApprove | Approva |
|  | menuEtcOptionDelete | Elimina |
|  | menuEtcOptionEdit | Modificare       |
|  | menuEtcOptionFlag | Contrassegna |
|  | menuEtcOptionShare | Condividi |
|  | menuEtcPostedAt | Pubblicato il {date} |
|  | menuEtcTitle | Altro |

## Interfaccia Moderatore {#section_o5f_dl4_xz}

Stringhe disponibili per l'interfaccia del moderatore autenticato dall'utente.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| Messaggi di conferma dal menu Altro | notificationEnabled | Approvato |
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

