---
description: Acquisite i conteggi dei post e dei commenti per determinate raccolte
  da visualizzare nelle pagine indice.
seo-description: Acquisite i conteggi dei post e dei commenti per determinate raccolte
  da visualizzare nelle pagine indice.
seo-title: Visualizza conteggio commenti
solution: Experience Manager
title: Visualizza conteggio commenti
uuid: 0 f 39 b 25 e -11 e 0-4945-be 71-55 fb 4798 b 6 c 7
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Visualizza conteggio commenti{#display-comment-count}

Acquisite i conteggi dei post e dei commenti per determinate raccolte da visualizzare nelle pagine indice.

Livefyre `CommentCount.js` consente di recuperare i conteggi dei contenuti delle raccolte sul sito. Anche se le app visualizzeranno il conteggio dei commenti per la raccolta corrente, possono essere utili anche questi conteggi. Questa funzione è particolarmente utile se non persistete il contenuto nel database (o se il database CMS non viene sincronizzato con Livefyre).

1. Caricare javascript.

   Per utilizzare `CommentCount.js`, occorre innanzitutto incorporare il file javascript nella `<head>` sezione della pagina o del modello in cui si desidera utilizzarlo.

   ```
   <script 
      type="text/javascript" 
      data-lf-domain="{network name (domain.fyre.co)}" 
      src="//cdn.livefyre.com/libs/commentcount/v1.0/commentcount.js"> 
   </script>
   ```

1. Associare l'elemento HTML.

   Una volta caricato lo script, si tenterà di trovare altri elementi sulla pagina con il nome di classe di `livefyre-commentcount`. Per ognuno di questi elementi, lo script cerca `data-lf-site-id` e gli attributi `data-lf-article-id` HTML, e li utilizzerà per recuperare contenuto da Livefyre e aggiornare ogni elemento con il valore più recente.

   Ad esempio, viene aggiornato il seguente elemento:

   ```
   <span class="livefyre-commentcount" data-lf-site-id="{site_id}" data-lf-article-id="{article_id}"> 
   0 Comments  
   </span>
   ```

   >[!NOTE] {importance = "high"}
   >
   >`CommentCount.js` Il codice verifica che un valore numerico venga aggiornato con il conteggio effettivo. Accertarsi di includere un valore numerico tra i tag.

   **Esempio 1** (utilizzo dell'URL come ID articolo):

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="https://mikesoldner.com/blog.php">  
   0 Comments  
   </span>
   ```

   **Esempio 2** (utilizzo di un sistema numerato come ID articolo):

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="25"> 0 Comments </span>
   ```

1. Configurare le opzioni.

   Per un maggiore controllo sul modo in cui vengono sostituiti i conteggi dei contenuti, chiamate `LF.CommentCount()` e trasmettete un oggetto contenente le opzioni di configurazione. Assicuratevi di chiamare la funzione dopo che tutti gli elementi che devono essere sostituiti sono nel DOM. Il punto migliore per richiamare questo metodo è nel piè di pagina, quindi si verifica quando il DOM viene caricato, ma prima degli eventi del documento e della finestra.

   Sono disponibili le seguenti opzioni di configurazione:

* **replacer:** Funzione o regex utilizzato per sostituire il testo di ciascun conteggio dei contenuti.

* **funzioni:** Utilizzato per eseguire la sostituzione su ogni elemento. Gli argomenti della funzione sono:

   **elemento:** L'elemento HTML che viene aggiornato.
   **count:** Il numero di contenuto per questo elemento.

* **regex:** Utilizzato per determinare quale parte del testo dell'elemento deve essere sostituita dal conteggio.

   **Esempio**:

   ```
      <script type="text/javascript"> LF.CommentCount({ 
        replacer: function(element, count) { 
            element.innerHTML = count +' Comment'+ (count === 1 ? '' : 's'); 
        } 
    }); 
   </script>
   ```

   >[!NOTE]
   >
   >Usate il replacer per personalizzare o internazionalizzare il messaggio del conteggio dei commenti.
