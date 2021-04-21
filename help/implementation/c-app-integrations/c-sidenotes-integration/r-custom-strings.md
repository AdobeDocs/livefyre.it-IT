---
title: Note sulle stringhe personalizzate
description: Note sulle stringhe personalizzate
exl-id: b5e2c18b-5b98-45ff-aa89-dd92a02949a9
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 6%

---

# Note sulle stringhe personalizzate{#sidenotes-custom-strings}

Le stringhe personalizzate vengono applicate attraverso un oggetto inserito nel costruttore Sidenotes e sostituiscono le stringhe predefinite utilizzate tramite l&#39;applicazione. Questi possono essere utilizzati per personalizzare qualsiasi parte della lingua in base alle specifiche del tuo stile o della tua lingua. Le stringhe vengono unite automaticamente con le impostazioni predefinite.

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
| appName | Note |
| commentModeratorTag | Mod |
| commentPendingTag | In sospeso |
| commentReadMoreLink | Ulteriori informazioni |
| commentReplyLink | Vedi {number} risposte |
| commentReplyLinkSing | Vedi risposta |
| commentCount | voti |
| commentCountSing | votare |
| editorPlaceholder | Cosa ne pensate? |
| editorPostBtn | Post Sidenote |
| editorPostBtnMobile | Post |
| editorPosting | Registrazione in corso.. |
| editorReplyBtn | Pubblica risposta |
| editorReplyTitle | Scrivi risposta |
| editorTitle | Nota di scrittura |
| emptyImageBlockTxt | Cosa ne pensate? |
| emptyTextBlockTxt | + |
| errorConnection | Uh oh. Sembra che tu non abbia una buona connessione. |
| errorDuplicate | Anche a noi piace la tua nota, ma non puoi pubblicarla due volte. |
| errorGeneral | Errore. Riprova. |
| errorServer | Si è verificato un problema con il nostro server. Provate ancora? |
| facebookShareCaption | SideNotes in &quot;{title}&quot; |
| menuAuthSignedInMsg | Devi effettuare l&#39;accesso a {action} |
| menuAuthSignInBtn | Accedere |
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
| menuFlagOptionNonD | Non concordo |
| menuFlagOptionOffensive | Offensivo |
| menuFlagOptionOffTopic | Argomento disattivato |
| menuFlagOptionSpam | Spam |
| menuFlagTitle | Contrassegna come.. |
| menuInfoCopyright | © Livefyre, Inc. 2014 |
| menuInfoHelp | Aiuto |
| menuInfoLivefyreLink | Visita Livefyre.com |
| menuRepliesViewReply | Risposta alla conversazione |
| menuRepliesViewTitle | Dettagli |
| menuShareOptionFacebook | Facebook |
| menuShareOptionLink | Copia permalink |
| menuShareOptionLinkComplete | Copiato |
| menuShareOptionLinkFailed | Copia non riuscita |
| menuShareOptionTwitter | Twitter |
| menuShareTitle | Condividi |
| notificationApproved | Approvato |
| notificationDeleted | Eliminato |
| notificationFlagged | Segnalato |
| permalinkBackBtn | Tutte |
| permalinkTitle | Permalink |
| domandaSpiegazione | Ora è possibile leggere e scrivere commenti direttamente su frasi, paragrafi, immagini e citazioni.<br><br>Evidenzia il testo e fai clic sull’icona &quot;fycon-write&quot; o fai clic sull’icona &quot;fycon-action-view&quot; alla fine di ciascun paragrafo. |
| QuestionMockText | Ciò che è &quot;noto a tutti&quot; non è ben noto, solo per il motivo che è &quot;familiare&quot;. |
| QuestionTitle | Cos&#39;è un Sidenote? |
| codaCommentiPlurale | {number} Note a margine |
| codaCommentiSingolare | 1 Nuovo Sidenote |
| codaRispostePlurale | {number} nuove risposte |
| codaRisposteSingolare | 1 Nuova risposta |
| responseBtn | Rispondi |
| signInToPost | Accedi per scrivere una nota |
| sliderCommentTally | di |
| sliderInviteRead | Letto |
| sliderInviteWrite | Scrivi |
| sliderWriteText | Cosa ne pensate? Tocca per scrivere |
| threadCollapseBtn | Comprimi |
| threadExpandBtnPlural | Espandi {numero} risposte |
| threadExpandBtnSingular | Espandi 1 risposta |
| threadReplyBtn | Risposta alla conversazione |
