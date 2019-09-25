---
description: Acquisite il conteggio dei post e dei commenti affinché alcune raccolte vengano visualizzate nelle pagine di indice.
seo-description: Acquisite il conteggio dei post e dei commenti affinché alcune raccolte vengano visualizzate nelle pagine di indice.
seo-title: Visualizza conteggio commenti
solution: Experience Manager
title: Visualizza conteggio commenti
uuid: 0f39b25e-11e0-4945-be71-55fb4798b6c7
translation-type: tm+mt
source-git-commit: c287e7a880f956f0444af746adee682571fe5a72

---


# Visualizza conteggio commenti{#display-comment-count}

Acquisite il conteggio dei post e dei commenti affinché alcune raccolte vengano visualizzate nelle pagine di indice.

Livefyre `CommentCount.js` consente di recuperare i conteggi dei contenuti per le raccolte sul sito. Anche se le app visualizzeranno il conteggio dei commenti per la raccolta corrente, può essere utile avere questi conteggi sindacati nel sito. Questa funzione è particolarmente utile se il contenuto non persiste nel database (o se il database CMS non è sincronizzato con Livefyre).

1. Caricate il codice JavaScript.

   Per utilizzare `CommentCount.js`, incorporate innanzitutto il file JavaScript nella `<head>` sezione della pagina o del modello in cui desiderate utilizzarlo.

   ```
   <script 
      type="text/javascript" 
      data-lf-domain="{network name (domain.fyre.co)}" 
      src="//cdn.livefyre.com/libs/commentcount/v1.0/commentcount.js"> 
   </script>
   ```

1. Eseguire il binding dell'elemento HTML.

   Una volta caricato lo script, si tenta di trovare altri elementi sulla pagina con il nome di classe `livefyre-commentcount`. Per ciascuno di questi elementi, lo script cercherà gli attributi `data-lf-site-id` e `data-lf-article-id` HTML e li utilizzerà per recuperare il contenuto da Livefyre e aggiornare ogni elemento con il valore più recente.

   Ad esempio, viene aggiornato il seguente elemento:

   ```
   <span class="livefyre-commentcount" data-lf-site-id="{site_id}" data-lf-article-id="{article_id}"> 
   0 Comments  
   </span>
   ```

   >[!NOTE] {important="high"}
   >
   >Il `CommentCount.js` codice verifica la presenza di un valore numerico da aggiornare con il conteggio effettivo. Accertarsi di includere un valore numerico tra i tag.

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

   Per un maggiore controllo sulla modalità di sostituzione dei conteggi dei contenuti, chiamate `LF.CommentCount()` e passate un oggetto contenente le opzioni di configurazione. Accertarsi di chiamare la funzione dopo che tutti gli elementi da sostituire si trovano nel DOM. La posizione migliore per chiamare questo metodo è nel piè di pagina, quindi si verifica quando il DOM viene caricato, ma prima degli eventi document e window ready.

   Sono disponibili le seguenti opzioni di configurazione:

* **** sostituto: Funzione o Regex utilizzata per sostituire il testo di ciascun conteggio di contenuti.

* **** function: Utilizzato per eseguire la sostituzione su ogni elemento. Gli argomenti della funzione sono:

   **** element: The HTML element that is being updated.
   **** count: Conteggio dei contenuti per questo elemento.

* **** regex: Used to determine which part of the element’s text should be replaced by the count.

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
   >Use the replacer to customize or internationalize the comment count message.
