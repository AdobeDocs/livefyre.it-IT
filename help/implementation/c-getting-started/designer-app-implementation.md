---
description: Utilizzate l'API Bootstrap e Stream con le app Livefyre.
seo-description: Utilizzate l'API Bootstrap e Stream con le app Livefyre.
seo-title: Implementazione app
solution: Experience Manager
title: Implementazione app
uuid: null
translation-type: tm+mt
source-git-commit: b737f2c6afb03d91041a317cc0afb790c3eadcb1
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---

# Implementazione app {#appimplementation}

Caso di utilizzo: Come cliente, voglio integrare Livefyre nel mio CMS di terze parti utilizzando il metodo Livefyre.js.

Esistono tre modi per implementare Livefyre in un componente AEM personalizzato o in altri CMS come WordPress, Sitecore o DemandWare: Implementazione dell&#39;app di Designer, API, implementazione e integrazione dell&#39;autenticazione di terze parti.

## Implementazione app di Designer {#designerapp}

Cosa: Il modo più semplice e veloce per integrare un&#39;app Livefyre. Potete progettare, configurare e generare un codice da incorporare JavaScript personalizzato per integrare un&#39;app LiveFree su una pagina in pochi minuti.

Procedura: [Creare, visualizzare in anteprima, pubblicare e incorporare un&#39;app Livefyre](/help/using/c-about-apps/c-create-an-app.md)

Esempio: [https://codepen.io/dharafyre/pen/bvGrLo](https://codepen.io/dharafyre/pen/bvGrLo)

### Implementazione di Livefyre.js {#livefyrejsimp}

Cosa: [Livefyre.js](/help/implementation/c-livefyre.js.md) è la libreria di base che abilita App e Auth in un sito. Definisce l&#39;oggetto `window.Livefyre` globale e un singolo metodo pubblico, Livefyre.request, che può essere utilizzato per caricare altre librerie JavaScript Livefyre che consentono di incorporare le app Livefyre e di integrarsi con le piattaforme di autenticazione utente di terze parti.

Procedura:

* [Creare una raccolta utilizzando CollectionMeta Token](/help/implementation/t-create-a-collectionmeta-token.md)

* Integrare le app in CMS di terze parti tramite l&#39;integrazione delle app

Esempi:

* App commenti: [https://codepen.io/dharafyre/pen/oYoJdP](https://codepen.io/dharafyre/pen/oYoJdP)

* Recensioni app: [https://codepen.io/dharafyre/pen/GXgvvd](https://codepen.io/dharafyre/pen/GXgvvd)

* Muro supporto: [https://codepen.io/dharafyre/pen/dNMPvM](https://codepen.io/dharafyre/pen/dNMPvM)

* Per le personalizzazioni avanzate che utilizzano l’SDK, consulta SDK StreamHub.

## Implementazione API {#apiimplementation}

Per creare esperienze personalizzate e visualizzazioni di dati, le app Livefyre possono essere create da zero utilizzando i dati Livefyre e social tramite l&#39;API Bootstrap e Stream.

## Integrazione autenticazione di terze parti {#thirdpartyauth}

Per le app Livefyre che richiedono l&#39;autenticazione, vedere [Integrazione identità](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) per le piattaforme di autenticazione di terze parti.

## Esempi cliente {#customerexamples}

I seguenti clienti hanno implementato Livefyre con integrazioni CMS di terze parti:

* [PGA Tour Media Wall](https://www.pgatour.com/social-hub.html)

* [TimeOut](https://www.timeout.com/london/restaurants/forest-bar-kitchen#tab_panel_3)
