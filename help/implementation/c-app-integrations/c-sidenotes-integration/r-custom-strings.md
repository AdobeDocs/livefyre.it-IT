---
description: nulle
seo-description: nulle
seo-title: Stringhe personalizzate
title: Stringhe personalizzate
uuid: 73745273-d 3 fb -4569-8910-d 149 fb 37 a 7 b 4
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Stringhe personalizzate{#sidenotes-custom-strings}

Le stringhe personalizzate vengono applicate tramite un oggetto inserito nella costruttore Sidenotes e ignorate le stringhe predefinite utilizzate tramite l'applicazione. Possono essere utilizzati per personalizzare qualsiasi parte della lingua in base alle specifiche di stile o lingua. Le stringhe vengono unite automaticamente con le impostazioni predefinite.

```
var customStrings = { 
   'menuBackBtn': 'return' }; 
new Livefyre.Sidenotes({ 
   strings: customStrings, 
   ...  
});
```

| Chiave | Predefinito |
|---|---|
| Appname | Sidenotes |
| Commentmoderatortag | Mod |
| Commentpendingtag | In sospeso |
| Commentreadmorelink | Ulteriori informazioni |
| Commentreplylink | Vedere {numero} risposte |
| Commentreplylinksing | Vedere risposta |
| Commentvotecount | voti |
| Commentvotecountsing | votare |
| Editorplaceholder | Che cosa pensate? |
| Editorpostbtn | Post Sidenote |
| Editorpostbtnmobile | Post |
| Editorposting | Pubblicazione in corso… |
| Editorreplybtn | Post Reply |
| Editorreplytitle | Scrivi risposta |
| Editortitle | Nota |
| Emptyimageblocktxt | Che cosa pensate? |
| Emptytextblocktxt | + |
| Errorconnection | Ah-oh. L'utente non sembra avere una buona connessione. |
| Errorduplicate | Anche la tua nota mi piace, ma non puoi pubblicarla due volte. |
| Errorgeneral | Si è verificato un errore. Riprovate. |
| Errorserver | Si è verificato un errore nel nostro server. Riprovare? |
| Facebooksharecaption | Sidenotes su «{title}» |
| Menuauthsignedinmsg | È necessario accedere a {action} |
| Menuauthsigninbtn | Accedi |
| Menubackbtn | Indietro |
| Menuconfirmaccept | Sì, {action} |
| Menuconfirmcancel | Annulla |
| Menuconfirmtitle | Sei sicuro? |
| Menuetcoptionapprove | Approva |
| Menuetcoptiondelete | Elimina |
| Menuetcoptionedit | Modifica |
| Menuetcoptionflag | Flag |
| Menuetcoptionshare | Condividi |
| Menuetcpostedat | Pubblicato in {data} |
| Menuetctitle | Altro |
| Menuflagoptiondisagree | Non d'accordo |
| Menuflagoptionoffensive | Offensivo |
| Menuflagoptionofftopic | Argomento Off |
| Menuflagoptionspam | Spam |
| Menuflagtitle | Flag come… |
| Menuinfocopyright | © Livefyre, Inc. 2014 |
| Menuinfohelp | Aiuto |
| Menuinfolivefyrelink | Visitate Livefyre.com |
| Menurepliesviewanswer | Rispondi alla conversazione |
| Menurepliesviewtitle | Dettagli |
| Menushareoptionfacebook | Facebook |
| Menushareoptionlink | Copia permalink |
| Menushareoptionlinkcomplete | Copiato |
| Menushareoptionlinkfailed | Copia non riuscita |
| Menushareoptiontwitter | Twitter |
| Menusharetitle | Condividi |
| Notificationapproved | Approvato |
| Notificationdelete | Eliminato |
| Notificationflded | Segnalata |
| Permalinkbackbtn | Tutto |
| Permalinktitle | Permalink |
| Questionexplain | È ora possibile leggere e scrivere commenti direttamente su frasi, paragrafi, immagini e preventivi.<br><br>Evidenzia il testo e fai clic sull'icona «fycon-write» o fai clic sull'icona «fycon-action-view» alla fine di ciascun paragrafo. |
| Questionmocktext | Ciò che è «noto» non è noto correttamente, per il motivo di «familiare». |
| Questiontitle | Che cos'è un Sidenote? |
| Queuedcommentsplural | {numero} Nuove Sidenotes |
| Queuedcommentssingular | 1 New Sidenote |
| Queuedresolfantasy queuedRepliesPlural | {numero} Nuove risposte |
| Queuedrepliessingular | 1 Nuova risposta |
| Responybtn | Risposta |
| Signintopost | Effettuate l'accesso per scrivere un sidenote |
| Slidercommenttally | di |
| Sliderinviteread | Leggi |
| Sliderinvitewrite | Scrittura |
| Sliderwritetext | Che cosa pensate? Toccate per scrivere |
| Threadcollapsebtn | Comprimi |
| Threadexpandbtnplural | Espandi {numero} risposte |
| Threadexpandbtnsingular | Espandi 1 risposta |
| Threadreplybtn | Rispondi alla conversazione |
