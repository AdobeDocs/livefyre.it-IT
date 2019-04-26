---
description: Utilizzate l'API Bootstrap e Stream con Livefyre Apps.
seo-description: Utilizzate l'API Bootstrap e Stream con Livefyre Apps.
seo-title: Implementazione app
solution: Experience Manager
title: Implementazione app
uuid: null
translation-type: tm+mt
source-git-commit: b737f2c6afb03d91041a317cc0afb790c3eadcb1

---

# Implementazione app {#appimplementation}

Caso d'uso: Come cliente, desidero integrare Livefyre nel mio CMS di terze parti utilizzando il metodo Livefyre. js.

Esistono tre modi per implementare Livefyre in un componente AEM personalizzato o in altri CMS, come wordpress, Sitecore o demandware: Implementazione dell'app di Designer, API, implementazione e integrazione autenticazione di terze parti.

## Implementazione app di Designer {#designerapp}

Cosa: Metodo più semplice e veloce per integrare un'app Livefyre. Potete progettare, configurare e generare un codice Javascript personalizzato per integrare un'app Liveyfre su una pagina in minuti.

Come: [Creare, visualizzare in anteprima, pubblicare e incorporare un'app Livefyre](/help/using/c-about-apps/c-create-an-app.md)

Esempio: [https://codepen.io/dharafyre/pen/bvGrLo](https://codepen.io/dharafyre/pen/bvGrLo)

### Implementazione di Livefyre. js {#livefyrejsimp}

Cosa: [Livefyre. js](/help/implementation/c-livefyre.js.md) è la libreria di base che potenzia app e autenticazione su un sito. Definisce l'oggetto globale `window.Livefyre` e un singolo metodo pubblico Livefyre. require, che può essere utilizzato per caricare altre librerie Javfyre Javfyre con cui incorporare Livefyre Apps e integrazione con piattaforme autenticazione utente di terze parti.

Come:

* [Creare una raccolta utilizzando il token collectionmeta](/help/implementation/t-create-a-collectionmeta-token.md)

* Integrare app in CMS di terze parti mediante integrazioni app

Esempi:

* App commenti: [https://codepen.io/dharafyre/pen/oYoJdP](https://codepen.io/dharafyre/pen/oYoJdP)

* Leggi app: [https://codepen.io/dharafyre/pen/GXgvvd](https://codepen.io/dharafyre/pen/GXgvvd)

* Media Wall: [https://codepen.io/dharafyre/pen/dNMPvM](https://codepen.io/dharafyre/pen/dNMPvM)

* Per personalizzazioni avanzate con l'SDK, consulta SDK streamhub.

## Implementazione API {#apiimplementation}

Per creare esperienze personalizzate e visualizzazioni dati, Livefyre Apps può essere creato utilizzando Livefyre e i dati social utilizzando l'API Bootstrap e Flusso.

## Integrazione autenticazione di terze parti {#thirdpartyauth}

Per le app Livefyre che richiedono l'autenticazione, consultate [Integrazione identità](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) per piattaforme di autenticazione di terze parti.

## Esempi dei clienti {#customerexamples}

I clienti seguenti implementavano Livefyre con le integrazioni CMS di terze parti:

* [PGA Tour Media Wall](https://www.pgatour.com/social-hub.html)

* [Timeout](https://www.timeout.com/london/restaurants/forest-bar-kitchen#tab_panel_3)
