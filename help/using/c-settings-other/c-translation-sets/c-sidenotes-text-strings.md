---
description: Personalizzazione delle stringhe di testo per Livefyre Sidenotes
seo-description: Personalizzazione delle stringhe di testo per Livefyre Sidenotes
seo-title: Stringhe testo Sidenotes
solution: Experience Manager
title: Stringhe testo Sidenotes
uuid: a 3735237-e 55 d -4 bc 0-b 88 d -8 a 323980 ee 09
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Stringhe testo Sidenotes{#sidenotes-text-strings}

Personalizzazione delle stringhe di testo per Livefyre Sidenotes

Questa pagina elenca e descrive tutte le stringhe disponibili per la personalizzazione nelle app Sidenotes. Per informazioni sulle stringhe disponibili per le app di base Livefyre, consultate Personalizzazioni stringa.

Implementazione
di Auth
Stream Info
Author/Content Info
User Actions
Post Funzioni
di interfaccia
Moderatore

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
| Stringhe di menu di autenticazione | Menuauthsigninbtn | Accedi |
|  | Menuauthsignedinmsg | È necessario accedere a {action} |
|  | Menuusereditprofile | Modifica profilo |
|  | Menuuseradmin | Admin Console |
|  | Menuuserlogout | Esci |
|  | Menuuserbackbtn | Tutto |

## Informazioni flusso {#section_wpy_gl4_xz}

Stringhe disponibili per le informazioni sul flusso di contenuto e la visualizzazione.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| Opzioni del menu Info | Menuinfocopyright | © Livefyre, Inc. 2014 |
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
|  | Datetimemonths | Un array. Predefinito =`[‘January’, ‘February’, ‘March’, ‘April’, ‘May’, ‘June’, ‘July’, ‘August’, ‘September’, ‘October’, ‘November’, ‘December’]` |
|  | Questionexplain | È ora possibile leggere e scrivere commenti direttamente su frasi, paragrafi, immagini e preventivi.<br><br><span class="&rdquo;lf-highlight-text&rdquo;">Evidenzia il testo</span> e fai clic sull <span class="&rdquo;fycon-write&rdquo;"></span> 'icona o fai clic sull' <span class="&rdquo;fycon-action-view&rdquo;"></span> icona alla fine di ciascun paragrafo. |
|  | Questionmocktext | Ciò che è «noto» non è noto correttamente, per il motivo di «familiare». |
|  | Questiontitle | Che cos'è un Sidenote? |

## Azioni utente {#section_qxd_fl4_xz}

Stringhe disponibili per le azioni dell'utente: segnalazione, condivisione e livecing di contenuti esistenti.

| Elemento | Chiave | Testo predefinito |
|---|---|---|
| Opzioni del menu di risposta | Menurepliesviewtitle | Dettagli |
|  | Menurepliesviewanswer | Rispondi alla conversazione |
| Opzioni del menu Condividi | Menushareoptionfacebook | Facebook |
|  | Menushareoptiontwitter | Twitter |
|  | Menusharetitle | Condividi |
| Opzioni del menu Flag | Menuflagoptiondisagree | Non d'accordo |
|  | Menuflagoptionoffensive | Offensivo |
|  | Menuflagoptionofftopic | Argomento Off |
|  | Menuflagoptionspam | Spam |
|  | Menuflagtitle | Flag come… |
|  | Facebooksharecaption | Filienalità su «{title}» |
| Opzioni utente per dispositivi mobili | Slidercommenttally | di |
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
| Opzioni del menu Elimina | Menuconfirmaccept | Sì, {action} |
|  | Menuconfirmcancel | Annulla |
|  | Menuconfirmtitle | Sei sicuro? |
| Opzioni di menu ecc. | Menuetcoptionapprove | Approva |
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
| Messaggi di conferma dal menu Altro | Notificationapproved | Approvato |
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

