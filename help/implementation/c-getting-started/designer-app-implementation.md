---
description: Utilizza l’API Bootstrap e Stream con le app Livefyre.
title: Implementazione app
uuid: null
exl-id: f1edef86-491d-4f8e-8ce5-f6e019d057ec
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# Implementazione app {#appimplementation}

Caso d’uso: In qualità di cliente, voglio integrare Livefyre nel mio CMS di terze parti utilizzando il metodo Livefyre.js .

Sono disponibili tre modi per implementare Livefyre in un componente AEM personalizzato o in altri CMS come WordPress, Sitecore o DemandWare: Implementazione, API, implementazione e integrazione dell’autenticazione di terze parti di Designer.

## Implementazione app di Designer {#designerapp}

Cosa: Il modo più semplice e veloce per integrare un’app Livefyre. Puoi progettare, configurare e generare un codice di incorporamento Javascript personalizzato per integrare un’app Live su una pagina in pochi minuti.

Come: [Creare, visualizzare in anteprima, pubblicare e incorporare un&#39;app Livefyre](/help/using/c-about-apps/c-create-an-app.md)

Esempio: [https://codepen.io/dharafyre/pen/bvGrLo](https://codepen.io/dharafyre/pen/bvGrLo)

### Implementazione di Livefyre.js {#livefyrejsimp}

Cosa: [Livefyre.js](/help/implementation/c-livefyre.js.md) è la libreria principale che abilita App e Auth in un sito. Definisce l’oggetto globale `window.Livefyre` e un singolo metodo pubblico, Livefyre.required, che può essere utilizzato per caricare altre librerie JavaScript Livefyre che consentono di incorporare le app Livefyre e di integrarle con piattaforme User Auth di terze parti.

Come:

* [Creare una raccolta utilizzando il token CollectionMeta](/help/implementation/t-create-a-collectionmeta-token.md)

* Integrare le app in CMS di terze parti utilizzando le integrazioni di app

Esempi:

* App commenti: [https://codepen.io/dharafyre/pen/oYoJdP](https://codepen.io/dharafyre/pen/oYoJdP)

* App recensioni: [https://codepen.io/dharafyre/pen/GXgvvd](https://codepen.io/dharafyre/pen/GXgvvd)

* Media Wall: [https://codepen.io/dharafyre/pen/dNMPvM](https://codepen.io/dharafyre/pen/dNMPvM)

* Per le personalizzazioni avanzate che utilizzano l’SDK, consulta SDK di StreamHub.

## Implementazione API {#apiimplementation}

Per creare esperienze personalizzate e visualizzazioni di dati, le app Livefyre possono essere create da zero utilizzando Livefyre e dati social tramite l’API Bootstrap e Stream.

## Integrazione dell&#39;autenticazione di terze parti {#thirdpartyauth}

Per le app Livefyre che richiedono l’autenticazione, consulta [Integrazione delle identità](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) per le piattaforme di autenticazione di terze parti.

## Esempi cliente {#customerexamples}

I seguenti clienti hanno implementato Livefyre con integrazioni CMS di terze parti:

* [Parete multimediale PGA Tour](https://www.pgatour.com/social-hub.html)

* [TimeOut](https://www.timeout.com/london/restaurants/forest-bar-kitchen#tab_panel_3)
