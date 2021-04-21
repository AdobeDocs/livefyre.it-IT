---
title: Incorporare un’app
description: Incorporare un’app
exl-id: 12f75093-1b4d-4cf1-8593-dbd17ff33872
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Incorpora un&#39;app{#embed-an-app}

Aggiungi le app Livefyre alle tue pagine web utilizzando la struttura del codice di incorporamento Livefyre.js .

Questa documentazione è destinata a un pubblico tecnico. Per [informazioni non tecniche sulle app](/help/using/c-about-apps/c-about-apps.md).

Questa sezione descrive la struttura del codice che dovrai includere nel modello di pagina per incorporare le app Livefyre sul sito.

1. Crea un file .html con un segnaposto Livefyre.

   Crea un nuovo file .html nell’editor di testo desiderato. Crea un elemento Livefyre segnaposto `<div>` in cui l’app verrà incorporata.

   ```
   <html> 
      <head> </head> 
      <body> 
         <div id='livefyre'> </div> 
      </body> 
   </html>
   ```

1. Includi la libreria Livefyre.js .

   Quindi, includi la libreria JS Livefyre. Inserisci il seguente riferimento in un elemento `<script>` nel tuo elemento `<head>` . Quindi, apri la pagina in un browser e utilizza l’ispettore web del browser per confermare che Livefyre è caricato.

   ```
   <head> 
      <script src='@{livefyre_js}'></script> 
   </head> 
   ```

1. Crea l’app Livefyre.

   Utilizza `Livefyre.require` per creare entrambe le app Core e SDK trasmettendo i pacchetti Livefyre che intendi utilizzare.

   1. Crea un’app core.

      Per creare un’app core (Commenti, Blog live o Chat), utilizza la seguente struttura:

      ```
      Livefyre.require(['fyre.conv#@{fyre_conv_version_prod}'], function(Conv) { 
           new Conv(networkConfig, [convConfig], function(widget) {});  
      });  
      ```

   1. Crea un’app SDK.

      Per creare un&#39;app SDK, ad esempio Media Wall o Feed, utilizza la seguente struttura:

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

      Consulta [ulteriori informazioni sulle applicazioni specifiche](/help/using/c-about-apps/c-about-apps.md). Si consiglia di fissare l&#39;ultima versione principale del pacchetto (che può essere trovata tramite [Livefyre.required](https://cdn.livefyre.com/packages.html)), per evitare integrazioni interrotte impreviste.

Avanti: Aggiungi l’autenticazione al sito per consentire agli utenti di inviare commenti.
