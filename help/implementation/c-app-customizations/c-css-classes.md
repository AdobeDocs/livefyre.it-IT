---
description: Utilizzate le classi CSS disponibili per personalizzare la visualizzazione delle app.
seo-description: Utilizzate le classi CSS disponibili per personalizzare la visualizzazione delle app.
seo-title: Classi CSS
solution: Experience Manager
title: Classi CSS
uuid: 8714 e 7 e 5-3858-458 f-a 464-de 87 fd 2 f 0 ff 0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Classi CSS{#css-classes}

Utilizzate le classi CSS disponibili per personalizzare la visualizzazione delle app.

Disponibile per chat, commenti, blog live, recensioni e Sidenotes.

Utilizzate CSS per personalizzare le app Livefyre per un&#39;integrazione più completa con la pagina, ignorando semplicemente il CSS app predefinito con il vostro foglio di stile. In questa sezione sono descritte le personalizzazioni CSS disponibili.

* [Editor CSS](#c_css_classes/section_edx_prh_xz)
* [CSS Opzioni di ordinamento](#c_css_classes/section_btq_4rh_xz)
* [CSS commenti](#c_css_classes/section_mlv_nrh_xz)
* [CSS commenti contenuti](#c_css_classes/section_m2v_mrh_xz)
* [CSS commenti archiviati](#c_css_classes/section_bs5_lrh_xz)
* [CSS dei commenti dei commenti](#c_css_classes/section_dy4_krh_xz)
* [Storify CSS Classes](../c-app-customizations/c-storify-css-classes.md#c_storify_css_classes)

## Editor CSS {#section_edx_prh_xz}

Utilizzare queste classi per modificare l&#39;interfaccia dell&#39;editor post.

| Classe | Descrizione |
|---|---|
| . fyre-comment-count | Testo che visualizza il numero di commenti. |
| . fyre-login-bar | Il rettangolo di selezione contenente la barra di accesso e le opzioni. |
| . fyre-live-container | Rettangolo di selezione intorno al numero di persone che ascolto e agli avatar. |
| . fyre-editor | Il rettangolo di selezione intorno al. fyre-login-bar. fyre-live-container e all&#39;area di testo in cui gli utenti scrivono i loro commenti. |
| . fyre-stream-sort | Il rettangolo di selezione intorno alle opzioni di ordinamento. |

Potete anche modificare gli stili nella configurazione App stessa, incluso il colore dello sfondo del campo dell&#39;editor, nonché il colore, le dimensioni e la famiglia del testo che vengono visualizzati all&#39;interno dell&#39;editor.

Per personalizzare l&#39;editor commento, aggiungete editorcss: {} a fyre. conv. load () e includete lo stile desiderato. Ad esempio, per aggiornare l&#39;editor con il CSS personalizzato:

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

## CSS Opzioni di ordinamento {#section_btq_4rh_xz}

| Classe | Descrizione |
|---|---|
| . fyre-stream-sort | L&#39;intero div delle opzioni di ordinamento. |
| . fyre-stream-sort-newest | L&#39;opzione «Più recente». |
| . fyre-stream-sort-older | L&#39;opzione «Meno recente». |
| . fyre-stream-sort-bar | La barra separatore tra le opzioni. |
| . fyre-stream-sort-selected | L&#39;opzione di ordinamento attualmente selezionata. |

Struttura HTML:

```
<div class="fyre-stream-sort"> 
   <a href="#" class="fyre-stream-sort-newest fyre-stream-sort-selected">Newest</a>  
   <span class="fyre-stream-sort-bar"> | </span> 
   <a href="#" class="fyre-stream-sort-oldest">Oldest</a> 
</div>
```

Nascondi|&#39; separa le opzioni di ordinamento.

```
.fyre-stream-sort .fyre-stream-sort-bar { 
    display: none !important; 
}
```

## CSS commenti {#section_mlv_nrh_xz}

| Classe | Descrizione |
|---|---|
| . fyre-comment-author-tag- *`custom tag name`* | Livefyre creerà una classe CSS in questo formato per ogni tag utente aggiunto tramite Livefyre&#39;s Studio, [Profile Sync](/help/implementation/t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-sync-with-livefyre-using-ping-for-pull.md). Questa classe può essere utilizzata per lo stile dello sfondo per qualsiasi contenuto pubblicato da account utente incluso tale tag. |
| . fyre-tag-content-icon- *`tag name`* | Livefyre creerà una classe CSS in questo formato per ciascun tag di contenuto aggiunto tramite Livefyre [Studio](/help/implementation/c-app-customizations/c-adding-users-to-groups.md). Questa classe può essere utilizzata per formattare qualsiasi contenuto a cui avete aggiunto il tag. |
| . fyre-comment-user | Il rettangolo di selezione che contiene l&#39;immagine del profilo utente. |
| . fyre-comment-username | Nome utente. |
| . fyre-moderator | Il rettangolo di selezione del moderatore. |
| . fyre-comment | Rettangolo di selezione intorno al testo o al collegamento del commento. |
| . fyre-comment-article | Il rettangolo di selezione per l&#39;intero contenuto del commento. |
| . fyre-comment-date | Il tag associato all&#39;elemento «ora dalla pubblicazione». |
| . fyre-comment-media | Il rettangolo di selezione intorno al contenuto multimediale. |
| . fyre-comment-actions | Il rettangolo di selezione intorno alle azioni disponibili per fare un commento. |
| . fyre-comment-like | Il rettangolo di selezione intorno al collegamento «Like». |
| . fyre-comment-response | Il rettangolo di selezione intorno al collegamento «Risposta». |

## CSS commenti contenuti {#section_m2v_mrh_xz}

>[!NOTE]
>
>Tutte le classi CSS dei commenti possono essere applicate anche a Contenuti contenuti.

| Classe | Descrizione |
|---|---|
| . fyre-featured-content-wrapper | Div contenitore per il lettore. |
| . fyre-featured-header | La barra del titolo iniziale. |
| . fyre-featctive-icon-icon | Icona quill dell&#39;intestazione. |
| . fyre-featured-title | Il testo dell&#39;intestazione. |
| . fyre-featin-body | Il div contenitore per contenuti contenuti nel lettore. |
| . fyre-featured-quote | L&#39;icona delle virgolette che inizia ogni elemento contenuto. |

## CSS commenti archiviati {#section_bs5_lrh_xz}

>[!NOTE]
>
>Tutte le classi CSS di contenuto possono essere applicate anche al contenuto archiviato.

| Classe | Descrizione |
|---|---|
| . fyre-archive-title | Il testo «Dal archivio». |
| . fyre-archive-stream-icon-icon | Logo per l&#39;intestazione «Dall&#39;archivio». |

## CSS dei commenti dei commenti {#section_dy4_krh_xz}

Queste classi consentono di personalizzare il modulo di notifica commenti di Livefyre.

| Classe | Descrizione |
|---|---|
| . fyre-notification | Elemento div per l&#39;elemento elenco (sia nuovo che archivio). |
| . fyre-notifier | Il wrapper per il contenuto del modulo di notifica. |
| . fyre-notifier-archive | Il wrapper per tutti i nuovi contenuti diversi dal post più recente. |
| . fyre-notifier-avatar | Immagine per l&#39;avatar. |
| . fyre-notifier-avatar-container | Il div contenitore per l&#39;avatar dell&#39;utente. Consente di definire il posizionamento. |
| . fyre-notifier-avatar-shading | L&#39;ombreggiatura del div avatar. |
| . fyre-notifier-banner | Contenitore per il contenuto dell&#39;anteprima del componente Notifier, che visualizza l&#39;avatar dell&#39;utente e uno snippet di contenuto per l&#39;elemento pubblicato più di recente. |
| . fyre-notifier-based | Il contenitore per le informazioni contenute nel componente Notifier, che elenca il numero di nuovi commenti, la didascalia del componente Notifier e il pulsante close. |
| . fyre-notifier-based-close | Il div contenitore per il pulsante di chiusura (x) per il Notifier. |
| . fyre-notifier-basic-shadow | L&#39;ombreggiatura della base del modulo di notifica. |
| . fyre-notifier-caption | Testo visualizzato per il modulo di notifica. «Nuovi commenti» per impostazione predefinita. |
| . fyre-notifier-close | Un pulsante che chiude il modulo di notifica. |
| . fyre-notifier-container | Il contenitore del modulo di notifica include sia il banner che la base. |
| . fyre-notifier-counter | Contenitore per il numero elencato nel modulo di notifica. |
| . fyre-notifier-list | Contenitore per la parte più recente del contenuto. |
| . fyre-notifier-message | I primi ~ 30 caratteri del contenuto visualizzato. |
| . fyre-notifier-message-container | Il div contenitore per il messaggio header. |
