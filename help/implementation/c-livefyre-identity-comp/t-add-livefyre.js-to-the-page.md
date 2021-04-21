---
description: Livefyre.js è una piccola libreria di base che fornisce l'autenticazione per le app sul tuo sito.
title: Aggiungi Livefyre.js alla pagina
exl-id: 4c5dfb31-b7e5-48f7-826c-cddbee06d876
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 0%

---

# Aggiungi Livefyre.js alla pagina{#add-livefyre-js-to-the-page}

Livefyre.js è una piccola libreria di base che fornisce l&#39;autenticazione per le app sul tuo sito.

Per abilitare l’autenticazione:

1. Aggiungi Livefyre.js all&#39;elemento `<head>` della pagina web o del modello di sito web.
1. Aggiungi uno dei seguenti elementi alla pagina:

   * `globalwindow.Livefyre` variable
   * `Livefyre.require` per caricare altri pacchetti Livefyre su richiesta

      ```
      <script src="//cdn.livefyre.com/Livefyre.js"></script>
      ```
