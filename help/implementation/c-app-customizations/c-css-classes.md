---
description: Utilizzate le classi CSS disponibili per personalizzare la visualizzazione delle app.
seo-description: Utilizzate le classi CSS disponibili per personalizzare la visualizzazione delle app.
seo-title: Classi CSS
solution: Experience Manager
title: Classi CSS
uuid: 8714e7e5-3858-458f-a464-de87fd2f0ff0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Classi CSS{#css-classes}

Utilizzate le classi CSS disponibili per personalizzare la visualizzazione delle app.

Disponibile per chat, commenti, blog dal vivo, recensioni e note.

Utilizzare i CSS per personalizzare le app Livefyre per un'integrazione più completa con la pagina, semplicemente ignorando il CSS app predefinito con il proprio foglio di stile. Questa sezione descrive le personalizzazioni CSS disponibili.

* [Editor CSS](#c_css_classes/section_edx_prh_xz)
* [Opzioni di ordinamento CSS](#c_css_classes/section_btq_4rh_xz)
* [CSS commento](#c_css_classes/section_mlv_nrh_xz)
* [Commenti in evidenza CSS](#c_css_classes/section_m2v_mrh_xz)
* [CSS commenti archiviati](#c_css_classes/section_bs5_lrh_xz)
* [CSS modulo di notifica commenti](#c_css_classes/section_dy4_krh_xz)
* [Storify classi CSS](../c-app-customizations/c-storify-css-classes.md#c_storify_css_classes)

## Editor CSS {#section_edx_prh_xz}

Utilizzare queste classi per modificare l'interfaccia dell'editor post.

| Classe | Descrizione |
|---|---|
| .fyre-comment-count | Testo che visualizza il numero di commenti. |
| .fyre-login-bar | Il rettangolo di selezione contenente la barra di login e le opzioni. |
| .fyre-live-container | Il rettangolo di selezione intorno al numero di persone che ascoltano e ai loro avatar. |
| .fyre-editor | Il rettangolo di selezione intorno alla barra .fyre-login-bar, .fyre-live-container e l’area di testo in cui gli utenti scrivono i propri commenti. |
| .fyre-stream-sort | Il rettangolo di selezione intorno alle opzioni di ordinamento. |

Potete anche modificare gli stili nella configurazione dell'app stessa, incluso il colore di sfondo del campo dell'editor, nonché il colore del font, le dimensioni e la famiglia del testo che appare all'interno dell'editor.

Per personalizzare l’editor dei commenti, aggiungete l’oggetto editorCss:{} a fyre.conv.load() e includete lo stile desiderato. Ad esempio, per aggiornare l’editor con il CSS personalizzato:

```
fyre.conv.load(networkConfig, [{ 
   siteId: LF_siteId, 
   el: 'livefyre', 
   articleId: LF_articleId, 
   collectionMeta: #CollectionMeta 
   editorCss: { 
      background: '#ccc', 
      color: 'red', 
      font: '30px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif' 
   } 
}]);
```

## Opzioni di ordinamento CSS {#section_btq_4rh_xz}

| Classe | Descrizione |
|---|---|
| .fyre-stream-sort | L'intero div delle opzioni di ordinamento. |
| .fyre-stream-sort-newest | Opzione "Più recente". |
| .fyre-stream-sort-old | Opzione "Più vecchio". |
| .fyre-stream-sort-bar | La barra di separazione tra le opzioni. |
| .fyre-stream-sort-selected | Opzione di ordinamento attualmente selezionata. |

Struttura HTML:

```
<div class="fyre-stream-sort"> 
   <a href="#" class="fyre-stream-sort-newest fyre-stream-sort-selected">Newest</a>  
   <span class="fyre-stream-sort-bar"> | </span> 
   <a href="#" class="fyre-stream-sort-oldest">Oldest</a> 
</div>
```

Nascondete l'opzione "|" per separare le opzioni di ordinamento.

```
.fyre-stream-sort .fyre-stream-sort-bar { 
    display: none !important; 
}
```

## CSS commento {#section_mlv_nrh_xz}

| Classe | Descrizione |
|---|---|
| .fyre-comment-author-tag- *`custom tag name`* | Livefyre creerà una classe CSS in questo formato per ciascun tag utente aggiunto tramite Livefyre’s Studio, [Profile Sync](/help/implementation/t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-sync-with-livefyre-using-ping-for-pull.md)(Sincronizzazione profilo). Questa classe può essere utilizzata per formattare lo sfondo per qualsiasi contenuto registrato dagli account utente, incluso tale tag. |
| .fyre-tag-content-icon- *`tag name`* | Livefyre creerà una classe CSS in questo formato per ciascun tag di contenuto aggiunto tramite Livefyre [Studio](/help/implementation/c-app-customizations/c-adding-users-to-groups.md). Questa classe può essere utilizzata per definire lo stile di qualsiasi contenuto al quale avete aggiunto il tag. |
| .fyre-comment-user | Il rettangolo di selezione che contiene l’immagine del profilo utente. |
| .fyre-comment-username | Il nome utente. |
| .fyre-moderator | Il riquadro di delimitazione del moderatore. |
| .fyre-comment | Rettangolo di selezione intorno al testo o al collegamento del commento. |
| .fyre-comment-article | Il rettangolo di selezione per l’intero contenuto del commento. |
| .fyre-comment-date | Il tag associato all’elemento "tempo trascorso dalla data di pubblicazione". |
| .fyre-comment-media | Il rettangolo di selezione intorno al contenuto multimediale. |
| .fyre-comment-actions | Il rettangolo di selezione intorno alle azioni disponibili per inserire un commento. |
| .fyre-comment-like | Il rettangolo di selezione intorno al collegamento "Mi piace". |
| .fyre-comment-response | Il rettangolo di selezione intorno al collegamento "Rispondi". |

## Commenti in evidenza CSS {#section_m2v_mrh_xz}

>[!NOTE]
>
>Tutte le classi CSS di Commento possono essere applicate anche a Contenuto in primo piano.

| Classe | Descrizione |
|---|---|
| .fyre-featured-content-wrapper | Il div contenitore per il lettore. |
| .fyre-featured-header | Barra del titolo iniziale. |
| .fyre-featured-header-icon | L’icona dell’anteprima dell’intestazione. |
| .fyre-featured-title | Testo dell’intestazione. |
| .fyre-featured-body | Il div del contenitore per il contenuto in evidenza nel lettore. |
| .fyre-featured | Icona della quotazione che inizia ogni elemento di contenuto. |

## CSS commenti archiviati {#section_bs5_lrh_xz}

>[!NOTE]
>
>Tutte le classi CSS di contenuto possono essere applicate anche al contenuto archiviato.

| Classe | Descrizione |
|---|---|
| .fyre-archive-stream-title | Testo "Dall'archivio". |
| .fyre-archive-stream-title-icon | Logo per l’intestazione "Dall’archivio". |

## CSS modulo di notifica commenti {#section_dy4_krh_xz}

Queste classi consentono di personalizzare il modulo di notifica per commenti Livefyre.

| Classe | Descrizione |
|---|---|
| .fyre-notifica | Il div per la voce di elenco (contenuto nuovo e contenuto di archivio). |
| .fyre-notifier | Il wrapper per il contenuto del modulo di notifica. |
| .fyre-notifier-archive | Il wrapper per tutti i nuovi contenuti diversi da quelli più recenti. |
| .fyre-notifier-avatar | Immagine per l'avatar. |
| .fyre-notifier-avatar-container | Il div del contenitore per l'avatar utente. Consente di definire il posizionamento. |
| .fyre-notifier-avatar-shading | Ombreggiatura per l'avatar div. |
| .fyre-notifier-banner | Contenitore del contenuto di anteprima del modulo di notifica, che visualizza l’avatar dell’utente e uno snippet di contenuto per l’elemento pubblicato più di recente. |
| .fyre-notifier-base | Contenitore della parte informativa del modulo di notifica, in cui sono elencati il numero di nuovi commenti, la didascalia e il pulsante Chiudi. |
| .fyre-notifier-base-close | Il div del contenitore per il pulsante di chiusura (x) del modulo di notifica. |
| .fyre-notifier-base-shadow | Ombreggiatura per la base del modulo di notifica. |
| .fyre-notifier-caption | Testo visualizzato per il modulo di notifica. "Nuovi commenti" per impostazione predefinita. |
| .fyre-notifier-close | Pulsante che consente di chiudere il modulo di notifica. |
| .fyre-notifier-container | Il contenitore del modulo di notifica include sia il banner che la base. |
| .fyre-notifier-counter | Contenitore del numero elencato nel modulo di notifica. |
| .fyre-notifier-list | Contenitore per il contenuto più recente. |
| .fyre-notifier-message | I primi ~30 caratteri del contenuto visualizzato. |
| .fyre-notifier-message-container | Il div contenitore per il messaggio di intestazione. |
