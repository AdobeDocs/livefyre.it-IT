---
description: Personalizzazione delle stringhe di testo per Livefyre Sidenotes
title: Stringhe di testo a margine
exl-id: 132a7c8d-10e1-419c-9d79-a40553e70785
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 9%

---

# Note a barre del testo{#sidenotes-text-strings}

Personalizzazione delle stringhe di testo per Livefyre Sidenotes

Questa pagina elenca e descrive tutte le stringhe disponibili per la personalizzazione nelle app Sidenotes. Per informazioni sulle stringhe disponibili per le app di base Livefyre, consulta Personalizzazioni di stringhe .

Implementazione
Auth
Informazioni flusso
Informazioni sull’autore/contenuto
Azioni utente
Funzioni post
Interfaccia moderatore
Errori

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
| Stringhe del menu di autenticazione | menuAuthSignInBtn | Accedere |
|  | menuAuthSignedInMsg | Devi effettuare l&#39;accesso a {action} |
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

## Informazioni sull&#39;autore/contenuto {#section_dhb_gl4_xz}

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
|  | datetimeMonths | Un array. Impostazione predefinita =`[‘January’, ‘February’, ‘March’, ‘April’, ‘May’, ‘June’, ‘July’, ‘August’, ‘September’, ‘October’, ‘November’, ‘December’]` |
|  | domandaSpiegazione | Ora è possibile leggere e scrivere commenti direttamente su frasi, paragrafi, immagini e citazioni.<br><br><span class="&rdquo;lf-highlight-text&rdquo;">Evidenzia </span> il testo e fai clic sull’ <span class="&rdquo;fycon-write&rdquo;"></span> icona o fai clic sull’ <span class="&rdquo;fycon-action-view&rdquo;"></span> icona alla fine di ciascun paragrafo. |
|  | QuestionMockText | Ciò che è &quot;noto a tutti&quot; non è ben noto, solo per il motivo che è &quot;familiare&quot;. |
|  | QuestionTitle | Cos&#39;è un Sidenote? |

## Azioni utente {#section_qxd_fl4_xz}

Stringhe disponibili per le azioni dell’utente: creazione di flag, condivisione e collegamento di contenuti esistenti.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| Opzioni del menu Risposta | menuRepliesViewTitle | Dettagli |
|  | menuRepliesViewReply | Risposta alla conversazione |
| Opzioni del menu Condividi | menuShareOptionFacebook | Facebook |
|  | menuShareOptionTwitter | Twitter |
|  | menuShareTitle | Condividi |
| Opzioni del menu Contrassegna | menuFlagOptionNonD | Non concordo |
|  | menuFlagOptionOffensive | Offensivo |
|  | menuFlagOptionOffTopic | Argomento disattivato |
|  | menuFlagOptionSpam | Spam |
|  | menuFlagTitle | Contrassegna come.. |
|  | facebookShareCaption | Note a margine su &quot;{title}&quot; |
| Opzioni utente mobile | sliderCommentTally | di |
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

## Interfaccia moderatore {#section_o5f_dl4_xz}

Stringhe disponibili per l&#39;interfaccia del moderatore autenticato dall&#39;utente.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| Messaggi di conferma dal menu Altro | notificationApproved | Approvato |
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
