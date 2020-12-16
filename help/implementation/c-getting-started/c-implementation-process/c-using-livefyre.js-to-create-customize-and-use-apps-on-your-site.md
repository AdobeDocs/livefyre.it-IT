---
seo-title: Incorporare un'app
solution: Experience Manager
title: Incorporare un'app
uuid: e75caf0e-04ea-4b04-89ed-fea1183ecf63
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---


# Incorpora un&#39;app{#embed-an-app}

Aggiungete le app Livefyre alle pagine Web mediante la struttura di codice incorporato Livefyre.js.

Questa documentazione è destinata a un pubblico tecnico. Per [informazioni non tecniche sulle app](/help/using/c-about-apps/c-about-apps.md).

Questa sezione descrive la struttura del codice che sarà necessario includere nel modello di pagina per incorporare le app Livefyre nel sito.

1. Create un file .html con un segnaposto Livefyre.

   Create un nuovo file .html nell’editor di testo desiderato. Create un elemento Livefyre `<div>` segnaposto in cui verrà incorporata l&#39;app.

   ```
   <html> 
      <head> </head> 
      <body> 
         <div id='livefyre'> </div> 
      </body> 
   </html>
   ```

1. Includete la libreria Livefyre.js.

   Quindi, includete la libreria Livefyre JS. Posizionare il riferimento seguente in un elemento `<script>` nell&#39;elemento `<head>`. Quindi, aprite la pagina in un browser e utilizzate la finestra di ispezione Web del browser per confermare che Livefyre sia caricato.

   ```
   <head> 
      <script src='@{livefyre_js}'></script> 
   </head> 
   ```

1. Create l’app Livefyre.

   Utilizzate `Livefyre.require` per creare sia app core che SDK trasmettendo i pacchetti Livefyre che pianificate di utilizzare.

   1. Create un&#39;app di base.

      Per creare un&#39;app di base (commenti, blog dal vivo o chat), utilizzate la struttura seguente:

      ```
      Livefyre.require(['fyre.conv#@{fyre_conv_version_prod}'], function(Conv) { 
           new Conv(networkConfig, [convConfig], function(widget) {});  
      });  
      ```

   1. Creare un&#39;app SDK.

      Per creare un&#39;app SDK, ad esempio una bacheca o un feed, usa la struttura seguente:

      ```
             Livefyre.require(['app#{version_number}'], 
         function (App, SDK) { 
            var app = new App({ 
            el: document.getElementById('app'), 
         }); 
         var collection = new SDK.Collection({ 
            network: "`labs.fyre.co`", 
            environment: "livefyre.com", 
            siteId: "315833", 
            articleId: 'livefyre-tweets' 
         }); 
         collection.pipe(feed); 
      }); 
      ```

      Vedere [ulteriori informazioni su specifiche app](/help/using/c-about-apps/c-about-apps.md). Si consiglia di fissare l&#39;ultima versione principale del pacchetto (disponibile tramite [Livefyre.request](https://cdn.livefyre.com/packages.html)), per evitare integrazioni interrotte impreviste.

Avanti: Aggiungete l&#39;autenticazione al sito per consentire agli utenti di pubblicare commenti.
