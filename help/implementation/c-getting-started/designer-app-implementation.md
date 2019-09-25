---
description: Utilizzate l'API Bootstrap e Stream con le app Livefyre.
seo-description: Utilizzate l'API Bootstrap e Stream con le app Livefyre.
seo-title: Implementazione app
solution: Experience Manager
title: Implementazione app
uuid: null
translation-type: tm+mt
source-git-commit: b737f2c6afb03d91041a317cc0afb790c3eadcb1

---

# App Implementation {#appimplementation}

Caso di utilizzo: Come cliente, voglio integrare Livefyre nel mio CMS di terze parti utilizzando il metodo Livefyre.js.

Esistono tre modi per implementare Livefyre in un componente AEM personalizzato o in altri CMS come WordPress, Siteore o DemandWare: Implementazione dell'app di Designer, API, implementazione e integrazione dell'autenticazione di terze parti.

## Designer App Implementation {#designerapp}

What: Simplest and fastest way of integrating a Livefyre App. You can design, configure, and generate a customized Javascript embed code to integrate a Liveyfre App on a page in minutes.

How: Create, Preview, Publish, and Embed a Livefyre App[](/help/using/c-about-apps/c-create-an-app.md)

Esempio: https://codepen.io/dharafyre/pen/bvGrLo[](https://codepen.io/dharafyre/pen/bvGrLo)

### Livefyre.js Implementation {#livefyrejsimp}

What: Livefyre.js is the core library that powers Apps and Auth on a site. [](/help/implementation/c-livefyre.js.md) It defines the global  object and a single public method, Livefyre.require, which can be used to load other Livefyre JavaScript libraries that help with embedding Livefyre Apps and integrating with third party User Auth platforms.`window.Livefyre`

How:

* [Create a Collection Using the CollectionMeta Token](/help/implementation/t-create-a-collectionmeta-token.md)

* Integrate Apps into third party CMS using App Integrations

Esempi:

* Comments App: https://codepen.io/dharafyre/pen/oYoJdP[](https://codepen.io/dharafyre/pen/oYoJdP)

* Reviews App: https://codepen.io/dharafyre/pen/GXgvvd[](https://codepen.io/dharafyre/pen/GXgvvd)

* Muro supporto: [https://codepen.io/dharafyre/pen/dNMPvM](https://codepen.io/dharafyre/pen/dNMPvM)

* For advanced customizations using the SDK, see StreamHub SDKs.

## API Implementation {#apiimplementation}

For creating customized experiences and data visualizations, Livefyre Apps can be created from scratch by consuming Livefyre and social data using the Bootstrap and Stream API.

## Third Party Authentication Integration {#thirdpartyauth}

Per le app Livefyre che richiedono l'autenticazione, consultate Integrazione [](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) delle identità per le piattaforme di autenticazione di terze parti.

## Esempi di clienti {#customerexamples}

I seguenti clienti hanno implementato Livefyre con integrazioni CMS di terze parti:

* [PGA Tour Media Wall](https://www.pgatour.com/social-hub.html)

* [TimeOut](https://www.timeout.com/london/restaurants/forest-bar-kitchen#tab_panel_3)
