---
description: Per personalizzare il contenuto dello stile per i gruppi di utenti, dovete prima aggiungere un tag utente all'account, quindi formattarlo utilizzando i CSS.
seo-description: Per personalizzare il contenuto dello stile per i gruppi di utenti, dovete prima aggiungere un tag utente all'account, quindi formattarlo utilizzando i CSS.
seo-title: Applicazione di stili personalizzati
solution: Experience Manager
title: Applicazione di stili personalizzati
uuid: 0556aa2f-4fcd-4bde-abb5-479ec682f573
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---


# Applicazione di stili personalizzati{#applying-custom-styles}

Per personalizzare il contenuto dello stile per i gruppi di utenti, dovete prima aggiungere un tag utente all&#39;account, quindi formattarlo utilizzando i CSS.

Per ciascun tag utente aggiunto tramite Studio o Ping for Pull, Livefyre creerà due classi CSS, entrambe utilizzabili per formattare il contenuto del gruppo.

Durante la conversione di tag utente in classi CSS:

* Livefyre crea due classi: fyre-author-tag-***&lt;your_group>*** e fyre-tag-author-***&lt;your_group>***. Entrambi possono essere utilizzati per formattare il contenuto.

* Eventuali spazi inclusi nel tag verranno convertiti in caratteri di sottolineatura. Ad esempio: &quot;Favorite User&quot; diventerà favorite_user.
* I caratteri Unicode inclusi nei nomi dei gruppi non saranno convertiti e saranno visualizzati come Unicode nei nomi delle classi. Ad esempio: Il gruppo di utenti &quot;modérateur&quot; diventerà fyre-comment-author-tag-modérateur.

Una volta creati i gruppi di utenti, utilizzate le classi CSS di Livefyre per applicare lo stile personalizzato al contenuto.

## Contenuto stile per moderatori (e proprietari) {#section_vjv_2cv_xz}

* Utilizzate la classe CSS .fyre-moderator.

   >[!NOTE]
   >
   >I proprietari, poiché sono anche Moderatori, avranno questa classe applicata anche al loro contenuto nel flusso.

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

## Contenuto stile per gruppi di utenti {#section_ghn_s1v_xz}

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

Utilizzate la classe CSS fyre-author-tag-****&lt;vostro_gruppo>*** o fyre-tag-author-****&lt;vostro_gruppo>**** per formattare il font e lo sfondo per ogni elemento pubblicato da un account associato al tag selezionato.

```
.fyre-comment-author-tag-<your_group> .fyre-comment-author-tag { 
    font: 10px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
    text-decoration: none; 
    color: #404040; 
    padding-left: 28px; 
    padding-top: 4px; 
}
```

