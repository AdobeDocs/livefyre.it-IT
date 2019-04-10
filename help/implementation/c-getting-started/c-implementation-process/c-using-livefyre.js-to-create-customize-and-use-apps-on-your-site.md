---
seo-title: Incorporare un'app
solution: Experience Manager
title: Incorporare un'app
uuid: e 75 caf 0 e -04 ea -4 b 04-89 ed-fea 1183 ecf 63
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Incorporare un'app{#embed-an-app}

Aggiungete Livefyre Apps alle pagine Web utilizzando la struttura di codice di Livefyre. js.

Questa documentazione è destinata a un pubblico tecnico. Per [informazioni non tecniche sulle app](/help/using/c-about-apps/c-about-apps.md).

In questa sezione viene descritta la struttura del codice che sarà necessario includere nel modello di pagina per incorporare le app Livefyre nel sito.

1. Create un file.html con un segnaposto Livefyre.

   Create un nuovo file.html nell'editor di testo desiderato. Create un segnaposto Livefyre `<div>` in cui verrà incorporata l'app.

   ```
   <html> 
      <head> </head> 
      <body> 
         <div id='livefyre'> </div> 
      </body> 
   </html>
   ```

1. Include la libreria Livefyre. js.

   Quindi, includete la libreria Jvefyre JS. Inserite il riferimento seguente in un `<script>` elemento dell `<head>` 'elemento. Quindi, aprite la pagina in un browser e utilizzate il modulo di ispezione Web del browser per confermare che Livefyre è stato caricato.

   ```
   <head> 
      <script src='@{livefyre_js}'></script> 
   </head> 
   ```

1. Create l'app Livefyre.

   Utilizzate `Livefyre.require` per creare app di base e SDK passando i pacchetti Livefyre che pianificate di utilizzare.

   1. Creare un'app di base.

      Per creare un'app di base (Commenti, Blog live o Chat), utilizzate la struttura seguente:

      ```
      Livefyre.require(['fyre.conv#@{fyre_conv_version_prod}'], function(Conv) { 
           new Conv(networkConfig, [convConfig], function(widget) {});  
      });  
      ```

   1. Creare un'app SDK.

      Per creare un'app SDK come Media Wall o Feed, utilizzate la struttura seguente:

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

      Ulteriori [informazioni su app specifiche](/help/using/c-about-apps/c-about-apps.md). Si consiglia di fissare l'ultima versione principale del pacchetto (che è possibile trovare tramite [Livefyre. require](https://cdn.livefyre.com/packages.html)), per evitare integrazioni interrotte impreviste.

Segue: Aggiungete l'autenticazione al sito per consentire agli utenti di pubblicare commenti.
