---
description: nulle
seo-description: nulle
seo-title: Note Personalizzate
title: Note Personalizzate
uuid: 73745273-d3fb-4569-8910-d149fb37a7b4
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Note Personalizzate{#sidenotes-custom-strings}

Le stringhe personalizzate vengono applicate attraverso un oggetto inserito nel costruttore Sidenotes e ignorano le stringhe predefinite utilizzate nell'applicazione. che possono essere utilizzati per personalizzare qualsiasi parte della lingua in base alle specifiche di stile o lingua. Le stringhe vengono automaticamente unite alle impostazioni predefinite.

```
var customStrings = { 
   'menuBackBtn': 'return' }; 
new Livefyre.Sidenotes({ 
   strings: customStrings, 
   ...  
});
```

| Chiave | impostazione predefinita |
|---|---|
| appName | Sidenotes |
| commentModeratorTag | Mod |
| commentPendingTag | In sospeso |
| commentReadMoreLink | Leggi tutto |
| commentReplyLink | Vedere {number} risposte |
| commentReplyLinkSing | Vedere la risposta |
| commentVoteCount | voti |
| commentCountSing | Votazione |
| editorPlaceholder | Che ne pensa? |
| editorPostBtn | Post Sidenote |
| editorPostBtnMobile | Post |
| editorPosting | Registrazione in corso... |
| editorReplyBtn | Pubblica risposta |
| editorReplyTitle | Scrivi risposta |
| editorTitle | Scrivi nota |
| emptyImageBlockTxt | Che ne pensa? |
| emptyTextBlockTxt | + |
| errorConnection | Oh-oh. Non sembra che tu abbia una buona connessione. |
| errorDuplicate | Anche la nota è gradita, ma non può essere pubblicata due volte. |
| errorGeneral | Si è verificato un errore. Prova ancora. |
| errorServer | Si è verificato un problema con il nostro server. Provi ancora? |
| facebookShareCaption | SideNotes in "{title}" |
| menuAuthSignedInMsg | È necessario aver effettuato l'accesso a {action} |
| menuAuthSignInBtn | Accedi |
| menuBackBtn | Indietro |
| menuConfirmAccept | Sì, {action} |
| menuConfirmCancel | Annulla |
| menuConfirmTitle | Sei sicuro? |
| menuEtcOptionApprove | Approva |
| menuEtcOptionDelete | Elimina |
| menuEtcOptionEdit | Modificare       |
| menuEtcOptionFlag | Contrassegna |
| menuEtcOptionShare | Condividi |
| menuEtcPostedAt | Pubblicato il {date} |
| menuEtcTitle | Altro |
| menuFlagOptionDisagreement | Non d'accordo |
| menuFlagOptionOffensive | Offensivo |
| menuFlagOptionOffTopic | Disattiva argomento |
| menuFlagOptionSpam | Spam |
| menuFlagTitle | Contrassegna come... |
| menuInfoCopyright | © Livefyre, Inc. 2014 |
| menuInfoHelp | Aiuto |
| menuInfoLivefyreLink | Visita Livefyre.com |
| menuRepliesViewReply | Rispondi alla conversazione |
| menuRepliesViewTitle | Dettagli |
| menuShareOptionFacebook | Facebook |
| menuShareOptionLink | Copia permalink |
| menuShareOptionLinkComplete | Copiato |
| menuShareOptionLinkFailed | Copia non riuscita |
| menuShareOptionTwitter | Twitter |
| menuShareTitle | Condividi |
| notificationEnabled | Approvato |
| notificationDeleted | Eliminato |
| notificationFlagged | Segnalato |
| permalinkBackBtn | Tutte |
| permalinkTitle | Permalink |
| questionExplanation | Ora è possibile leggere e scrivere commenti direttamente su frasi, paragrafi, immagini e citazioni.<br><br>Evidenzia il testo e fai clic sull’icona "fycon-write" o fai clic sull’icona "fycon-action-view" alla fine di ciascun paragrafo. |
| questionMockText | Ciò che è "familiare" non è ben noto, solo per il motivo che è "familiare". |
| questionTitle | Cos'è una Sidenote? |
| queusedCommentsPlural | {number} Nuove note |
| queusedCommentsSingular | 1 Nuova Sidenote |
| queusedRepliesPlural | {number} Nuove risposte |
| queusedRepliesSingular | 1 Nuova risposta |
| replyBtn | Rispondi |
| signInToPost | Accesso per scrivere una nota |
| sliderCommentTally | di |
| sliderInviteRead | Letto |
| sliderInviteWrite | Write |
| sliderWriteText | Che ne pensa? Toccate per scrivere |
| threadCollapseBtn | Comprimi |
| threadExpandBtnPlural | Espandi {numero} risposte |
| threadExpandBtnSingular | Espandi 1 risposta |
| threadReplyBtn | Rispondi alla conversazione |
