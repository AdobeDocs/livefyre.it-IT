---
description: Per personalizzare lo stile del contenuto per i gruppi di utenti, devi prima aggiungere un tag utente all’account , quindi assegnare uno stile al contenuto utilizzando CSS.
title: Applicazione di stili personalizzati
exl-id: 54692525-32ce-487a-b3c3-da1261b58da1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Applicazione di stili personalizzati{#applying-custom-styles}

Per personalizzare lo stile del contenuto per i gruppi di utenti, devi prima aggiungere un tag utente all’account , quindi assegnare uno stile al contenuto utilizzando CSS.

Per ogni tag utente aggiunto tramite Studio o Ping for Pull, Livefyre creerà due classi CSS, entrambe utilizzabili per lo stile del contenuto del gruppo.

Durante la conversione di tag utente in classi CSS:

* Livefyre crea due classi: fyre-author-tag-***&lt;your_group>*** e fyre-tag-author-***&lt;your_group>***. Entrambi possono essere utilizzati per definire lo stile del contenuto.

* Gli spazi inclusi nel tag verranno convertiti in caratteri di sottolineatura. Ad esempio: L&#39;utente preferito diventerà favorite_user.
* I caratteri Unicode inclusi nei nomi dei gruppi non verranno convertiti e verranno visualizzati come Unicode nei nomi delle classi. Ad esempio: Il gruppo di utenti &quot;modérateur&quot; diventerà fyre-comment-author-tag-modérateur.

Una volta creati i gruppi di utenti, utilizza le classi CSS di Livefyre per applicare lo stile personalizzato per il contenuto.

## Contenuto di stile per moderatori (e proprietari) {#section_vjv_2cv_xz}

* Utilizza la classe CSS .fyre-moderator.

   >[!NOTE]
   >
   >I proprietari, poiché sono anche i moderatori, avranno questa classe applicata anche al loro contenuto nel flusso.

* Crea una regola CSS per mostrare o personalizzare lo stile di un badge per il gruppo:

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

Crea una regola CSS per mostrare o personalizzare lo stile di un badge per il gruppo:

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

Utilizza la classe CSS fyre-author-tag-***&lt;your_group>*** o fyre-tag-author-***&lt;your_group>*** per assegnare lo stile al font e allo sfondo per ogni elemento pubblicato da un account associato al tag selezionato.

```
.fyre-comment-author-tag-<your_group> .fyre-comment-author-tag { 
    font: 10px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
    text-decoration: none; 
    color: #404040; 
    padding-left: 28px; 
    padding-top: 4px; 
}
```
