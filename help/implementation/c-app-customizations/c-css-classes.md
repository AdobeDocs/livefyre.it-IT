---
description: Utilizza le classi CSS disponibili per personalizzare la visualizzazione delle app.
title: Classi CSS
exl-id: 605f2c47-13f7-4535-90b1-c53cbf548534
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 1%

---

# Classi CSS{#css-classes}

Utilizza le classi CSS disponibili per personalizzare la visualizzazione delle app.

Disponibile per Chat, Commenti, Live Blog, Recensioni e Note a margine.

Utilizza i CSS per personalizzare le app Livefyre per un’integrazione più completa con la pagina, semplicemente ignorando i CSS app predefiniti con il tuo foglio di stile. Questa sezione descrive le personalizzazioni CSS disponibili.

* [Editor CSS](#c_css_classes/section_edx_prh_xz)
* [Ordinamento delle opzioni CSS](#c_css_classes/section_btq_4rh_xz)
* [Commenta CSS](#c_css_classes/section_mlv_nrh_xz)
* [Commenti in primo piano CSS](#c_css_classes/section_m2v_mrh_xz)
* [CSS commenti archiviati](#c_css_classes/section_bs5_lrh_xz)
* [CSS notificatore commenti](#c_css_classes/section_dy4_krh_xz)
* [Storificare le classi CSS](../c-app-customizations/c-storify-css-classes.md#c_storify_css_classes)

## Editor CSS {#section_edx_prh_xz}

Utilizza queste classi per modificare l&#39;interfaccia dell&#39;editor post.

| Classe | Descrizione |
|---|---|
| .fyre-comment-count | Testo che visualizza il numero di commenti. |
| .fyre-login-bar | Il riquadro di delimitazione contenente la barra di accesso e le opzioni. |
| .fyre-live-container | Il riquadro che delimita il numero di persone che ascoltano e i loro avatar. |
| .fyre-editor | Il riquadro di delimitazione intorno a .fyre-login-bar, .fyre-live-container e l&#39;area di testo in cui gli utenti scrivono i loro commenti. |
| .fyre-stream-sort | Il riquadro di delimitazione intorno alle opzioni di ordinamento. |

Puoi anche modificare gli stili nella configurazione dell’app stessa, incluso il colore di sfondo del campo dell’editor, nonché il colore del font, le dimensioni e la famiglia del testo che appare all’interno dell’editor.

Per personalizzare l’editor dei commenti, aggiungi l’oggetto editorCss:{} a fyre.conv.load() e includi lo stile desiderato. Ad esempio, per aggiornare l’editor con il CSS personalizzato:

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

## Ordinamento delle opzioni CSS {#section_btq_4rh_xz}

| Classe | Descrizione |
|---|---|
| .fyre-stream-sort | Tutte le opzioni di ordinamento div. |
| .fyre-stream-sort-newest | Opzione &quot;Più recente&quot;. |
| .fyre-stream-sort-dest | Opzione &quot;Oldest&quot;. |
| .fyre-stream-sort-bar | La barra di separazione tra le opzioni. |
| .fyre-stream-sort-selected | L’opzione di ordinamento attualmente selezionata. |

Struttura HTML:

```
<div class="fyre-stream-sort"> 
   <a href="#" class="fyre-stream-sort-newest fyre-stream-sort-selected">Newest</a>  
   <span class="fyre-stream-sort-bar"> | </span> 
   <a href="#" class="fyre-stream-sort-oldest">Oldest</a> 
</div>
```

Nascondere il simbolo &quot;|&quot; separando le opzioni di ordinamento.

```
.fyre-stream-sort .fyre-stream-sort-bar { 
    display: none !important; 
}
```

## Commenta CSS {#section_mlv_nrh_xz}

| Classe | Descrizione |
|---|---|
| .fyre-comment-author-tag- *`custom tag name`* | Livefyre creerà una classe CSS in questo formato per ogni tag utente aggiunto tramite Livefyre’s Studio, [Sincronizzazione profilo](/help/implementation/t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-sync-with-livefyre-using-ping-for-pull.md). Questa classe può essere utilizzata per formattare lo sfondo per qualsiasi contenuto pubblicato dagli account utente, incluso quel tag. |
| .fyre-tag-content-icon- *`tag name`* | Livefyre creerà una classe CSS in questo formato per ogni tag di contenuto aggiunto tramite Livefyre [Studio](/help/implementation/c-app-customizations/c-adding-users-to-groups.md). Questa classe può essere utilizzata per assegnare uno stile a qualsiasi contenuto al quale è stato aggiunto il tag . |
| .fyre-comment-user | Il riquadro di delimitazione contenente l&#39;immagine del profilo utente. |
| .fyre-comment-username | Nome utente. |
| .fyre-moderator | Il riquadro di delimitazione del moderatore. |
| .fyre-comment | Casella di collegamento intorno al testo o al collegamento del commento. |
| .fyre-comment-article | Il riquadro di delimitazione per l’intero contenuto del commento. |
| .fyre-comment-date | Il tag associato all’elemento &quot;tempo dal momento della pubblicazione&quot;. |
| .fyre-comment-media | Il riquadro di delimitazione intorno al contenuto multimediale. |
| .fyre-comment-actions | Il riquadro di delimitazione delle azioni disponibili per un commento. |
| .fyre-comment-like | Il riquadro di delimitazione intorno al collegamento &quot;Mi piace&quot;. |
| .fyre-comment-response | Il riquadro di delimitazione intorno al collegamento &quot;Risposta&quot;. |

## Commenti in primo piano CSS {#section_m2v_mrh_xz}

>[!NOTE]
>
>Tutte le classi CSS Commento possono essere applicate anche al contenuto in primo piano.

| Classe | Descrizione |
|---|---|
| .fyre-featured-content-wrapper | Il div contenitore per il lettore. |
| .fyre-featured-header | Barra del titolo iniziale. |
| .fyre-featured-header-icon | Icona della fresa dell’intestazione. |
| .fyre-featured-title | Testo dell’intestazione. |
| .fyre-featured-body | Il div contenitore per il contenuto in primo piano nel lettore. |
| .fyre-featured-quote | Icona che inizia ogni elemento di contenuto. |

## Commenti archiviati CSS {#section_bs5_lrh_xz}

>[!NOTE]
>
>Tutte le classi CSS di contenuto possono essere applicate anche al contenuto archiviato.

| Classe | Descrizione |
|---|---|
| .fyre-archive-stream-title | Testo &quot;Dall’archivio&quot;. |
| .fyre-archive-stream-title-icon | Logo dell’intestazione &quot;Dall’archivio&quot;. |

## Modulo di notifica dei commenti CSS {#section_dy4_krh_xz}

Queste classi ti consentono di personalizzare il modulo di notifica dei commenti Livefyre.

| Classe | Descrizione |
|---|---|
| .fyre-notificazione | Il div per la voce di elenco (sia contenuto nuovo che contenuto di archivio). |
| .fyre-notificfier | Il wrapper per il contenuto del notificatore. |
| .fyre-notificfier-archive | Il wrapper per tutti i nuovi contenuti diversi dal post più recente. |
| .fyre-notificfier-avatar | L&#39;immagine per l&#39;avatar. |
| .fyre-notificfier-avatar-container | Il div contenitore per l&#39;avatar utente. Consente di definire il posizionamento. |
| .fyre-notificfier-avatar-shading | Ombreggiatura per l&#39;avatar div. |
| .fyre-notificfier-banner | Contenitore per il contenuto di anteprima del notificatore, che visualizza l’avatar utente e uno snippet di contenuto per l’elemento pubblicato più di recente. |
| .fyre-notificfier-base | Contenitore per la parte informativa del componente di notifica, in cui sono elencati il numero di nuovi commenti, la didascalia del componente di avviso e il pulsante Chiudi. |
| .fyre-notificfier-base-close | Il div del contenitore per il pulsante di chiusura (x) per il componente di notifica. |
| .fyre-notificfier-base-shadow | Ombreggiatura della base del notificatore. |
| .fyre-notificfier-caption | Testo visualizzato per il notificatore. &quot;Nuovi commenti&quot; per impostazione predefinita. |
| .fyre-notificfier-close | Pulsante che chiude il notificatore. |
| .fyre-notificfier-container | Il contenitore del componente di notifica include sia il banner che la base. |
| .fyre-notificfier-counter | Contenitore del numero elencato nel modulo di notifica. |
| .fyre-notificfier-list | Il contenitore per il contenuto più recente. |
| .fyre-notificfier-message | I primi circa 30 caratteri del contenuto visualizzato. |
| .fyre-notificfier-message-container | Il div contenitore per il messaggio di intestazione. |
