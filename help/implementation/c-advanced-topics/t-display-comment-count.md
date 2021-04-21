---
description: Prendi il conteggio dei post e dei commenti per alcune raccolte da visualizzare sulle tue pagine di indice.
title: Visualizza conteggio commenti
exl-id: 03c911f0-1fdd-4d5c-9262-9ff7485b7b14
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Conteggio dei commenti visualizzati{#display-comment-count}

Prendi il conteggio dei post e dei commenti per alcune raccolte da visualizzare sulle tue pagine di indice.

Il `CommentCount.js` di Livefyre consente di recuperare i conteggi dei contenuti per le raccolte sul sito. Anche se le app mostreranno il conteggio dei commenti per la raccolta corrente, può essere utile che questi conteggi siano sindacati in tutto il sito. Questa funzione è particolarmente utile se il contenuto del database non è persistente (o se il database CMS non è sincronizzato con Livefyre).

1. Carica il JavaScript.

   Per utilizzare `CommentCount.js`, incorpora prima il file JavaScript nella sezione `<head>` della pagina o del modello in cui desideri utilizzarlo.

   ```
   <script 
      type="text/javascript" 
      data-lf-domain="{network name (domain.fyre.co)}" 
      src="//cdn.livefyre.com/libs/commentcount/v1.0/commentcount.js"> 
   </script>
   ```

1. Eseguire il binding dell’elemento HTML.

   Una volta caricato lo script, tenterà di trovare altri elementi sulla pagina con un nome di classe `livefyre-commentcount`. Per ciascuno di questi elementi, lo script cercherà gli attributi `data-lf-site-id` e `data-lf-article-id` HTML, e li utilizzerà per recuperare il contenuto da Livefyre e aggiornare ogni elemento con il valore più recente.

   Ad esempio, viene aggiornato il seguente elemento:

   ```
   <span class="livefyre-commentcount" data-lf-site-id="{site_id}" data-lf-article-id="{article_id}"> 
   0 Comments  
   </span>
   ```

   >[!NOTE]
   >
   >Il codice `CommentCount.js` verifica la presenza di un valore numerico da aggiornare con il conteggio effettivo. Accertati di includere un valore numerico tra i tag .

   **Esempio 1**  (utilizzando l’URL come ID articolo):

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="https://mikesoldner.com/blog.php">  
   0 Comments  
   </span>
   ```

   **Esempio 2**  (utilizzo di un sistema numerato come ID articolo):

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="25"> 0 Comments </span>
   ```

1. Configurare le opzioni.

   Per un maggiore controllo sulla modalità di sostituzione dei conteggi dei contenuti, invoca `LF.CommentCount()` e passa un oggetto contenente le opzioni di configurazione. Assicurati di chiamare la funzione dopo che tutti gli elementi che devono essere sostituiti sono nel DOM. La posizione migliore per chiamare questo metodo è nel piè di pagina, quindi si verifica quando il DOM viene caricato, ma prima degli eventi document e window ready.

   Consentiamo le seguenti opzioni di configurazione:

* **replace:** Funzione o Regex utilizzata per sostituire il testo di ciascun conteggio di contenuto.

* **funzione:** utilizzata per eseguire la sostituzione su ogni elemento. Gli argomenti della funzione sono:

   **elemento:** l’elemento HTML in fase di aggiornamento.
   **count:** il conteggio dei contenuti per questo elemento.

* **regex:** utilizzato per determinare quale parte del testo dell’elemento deve essere sostituita dal conteggio.

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
   >Utilizza il sostituitore per personalizzare o internazionalizzare il messaggio del conteggio dei commenti.
