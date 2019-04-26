---
description: Per personalizzare il contenuto di stile per i gruppi di utenti, dovete
  prima aggiungere un tag utente all'account, quindi stile del contenuto mediante
  CSS.
seo-description: Per personalizzare il contenuto di stile per i gruppi di utenti,
  dovete prima aggiungere un tag utente all'account, quindi stile del contenuto mediante
  CSS.
seo-title: Applicazione di stili personalizzati
solution: Experience Manager
title: Applicazione di stili personalizzati
uuid: 0556 aa 2 f -4 fcd -4 bde-abb 5-479 ec 682 f 573
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Applicazione di stili personalizzati{#applying-custom-styles}

Per personalizzare il contenuto di stile per i gruppi di utenti, dovete prima aggiungere un tag utente all'account, quindi stile del contenuto mediante CSS.

Per ogni tag utente aggiunto tramite Studio o Ping per Pull, Livefyre creerà due classi CSS, entrambe che possono essere utilizzate per formattare il contenuto del gruppo.

Quando convertite i tag utente in classi CSS:

* Livefyre crea due classi: fyre-author-tag-*** < your_ group >*** e fyre-tag-author-*** < your_ group >***. Potete utilizzare entrambi per formattare il contenuto.

* Gli spazi inclusi nel tag saranno convertiti in caratteri di sottolineatura. Ad esempio: L'opzione «Utente preferito» diventa preferita_ utente.
* I caratteri Unicode inclusi nei nomi dei gruppi non verranno convertiti e saranno visualizzati come Unicode nei nomi delle classi. Ad esempio: Il gruppo di utenti «modérateur» diventerà fyre-comment-author-style-modérateur.

Una volta creati i gruppi di utenti, utilizzate le classi CSS di Livefyre per applicare lo stile personalizzato al contenuto.

## Contenuto dello stile per Moderatori (e Proprietari) {#section_vjv_2cv_xz}

* Utilizzate la classe CSS. fyre-moderator.

   >[!NOTE]
   >
   >I proprietari, perché sono anche Moderatori, conterranno anche questa classe al loro contenuto nel flusso.

* Create una regola CSS per mostrare o formattare un contrassegno per il gruppo:

   ```
   .fyre-moderator { 
       font: 13px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
       text-decoration: none; 
       color: #404040; 
       padding-left: 28px; 
       padding-top: 4px; 
   }
   ```

## Contenuto dello stile per i gruppi di utenti {#section_ghn_s1v_xz}

Create una regola CSS per mostrare o formattare un contrassegno per il gruppo:

```
<span class="fyre-comment-author-tag fyre-comment-author-tag-writer fyre-comment-plus" data-fyre-author-tag="staff">Staff Writer</span>
```

```
.livechat-comments-container .fyre .fyre-comment-wrapper .fyre-comment-author-tag, .comments-container .fyre .fyre-comment-wrapper .fyre-comment-author-tag { 
    display: inline-block !important; 
    background: #603url('/etc/designs/site/images/comments-icon-staff.8db5be91.png?1438807177') no-repeat left center !important; 
    padding-right: 3px !important; 
    padding-left: 20px !important; 
    text-transform: uppercase !important; 
    font-weight: bold !important; 
    font-size: 11px !important; 
    border-radius: 0 !important; 
    color: #ffffff !important; 
}
```

Utilizzate la classe CSS fyre-author-tag-*** < group >*** o fyre-tag-author-*** < your_ group >*** per stile del font e dello sfondo per ogni elemento pubblicato da un account associato al tag selezionato.

```
.fyre-comment-author-tag-<your_group> .fyre-comment-author-tag { 
    font: 10px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
    text-decoration: none; 
    color: #404040; 
    padding-left: 28px; 
    padding-top: 4px; 
}
```

