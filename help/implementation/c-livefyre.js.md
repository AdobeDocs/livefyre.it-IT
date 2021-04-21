---
description: La libreria principale Livefyre utilizzata per alimentare Livefyre sul tuo sito.
title: Livefyre.js
exl-id: 82083dc0-3b4a-467c-bad7-dbf242ab5bbd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 0%

---

# Livefyre.js {#livefyre-js}

La libreria principale Livefyre utilizzata per alimentare Livefyre sul tuo sito.

`Livefyre.js` è la libreria principale che puoi installare su ogni pagina web abilitata per Livefyre. Definisce l&#39;oggetto globale `window.Livefyre` e un singolo metodo pubblico, `Livefyre.require`, che può essere utilizzato per caricare altre librerie JavaScript Livefyre che aiutano con [Embedding Livefyre Apps](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md), [Integrazione del provider di autenticazione con Livefyre](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) e altro ancora.

## Aggiungi al tuo sito {#section_cst_twg_xz}

Aggiungi il seguente tag `<script>` alla pagina web o al modello di sito web. Se possibile, aggiungilo alla sezione `<head>` del documento HTML in modo che venga caricato rapidamente.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

>[!NOTE]
>
>Questo script incorporerà un file molto piccolo (~1 Kb) chiamato scout Livefyre.js che in seguito caricherà la versione più recente di Livefyre.js sul protocollo con cui è stato effettuato l’accesso alla tua pagina web (HTTP o HTTPS).

## Livefyre.required {#section_ipq_hwg_xz}

`Livefyre.require` è un caricatore di moduli JavaScript personalizzato come  [curl.](https://github.com/cujojs/curl) jsor  [RequireJS](https://requirejs.org/). Può essere utilizzato per caricare la maggior parte dei pacchetti pubblicati da Livefyre e presenta un percorso di integrazione comodo e intuitivo.

Le versioni dei pacchetti accessibili tramite `Livefyre.require` vengono impostate utilizzando [Controllo delle versioni semantiche](https://semver.org/). I pacchetti possono essere richiesti in una versione specifica o in una serie di versioni in modo che la tua pagina web possa beneficiare automaticamente delle nuove funzioni di bugfix. Questo offre flessibilità durante l’integrazione di Livefyre sul sito. È possibile utilizzare tre livelli di creazione versioni con `Livefyre.require`.

* **nome-pacchetto#1:** Fissa alla versione principale v1. Otterrai tutti i nuovi aggiornamenti che mantengono un’API compatibile con le versioni precedenti. Aggiungi a una versione principale per ricevere correzioni di bug e miglioramenti di funzioni minori per quella versione.
* **package-name#1.1:** Pin alla versione minore v1.1. Tutti i bugfix a questa versione secondaria. Livefyre Engineering eseguirà sempre il backup della versione secondaria di un pacchetto se il suo comportamento predefinito o l’ambito funzionale cambia in modo da causare un comportamento nuovo e imprevisto sulla tua pagina web. Esegui il ping a una versione secondaria se desideri ricevere correzioni di bug automatizzati, ma non sono presenti funzionalità aggiuntive o modifiche al comportamento predefinito.
* **nome-pacchetto#1.1.1:** Effettua il ping alla versione v1.1.1 della patch. Il comportamento di questo incorporamento non cambierà mai, anche in presenza di bug fix. Aggiungi a una versione della patch se disponi di personalizzazioni CSS estese per il tuo sito che dipendono dalla struttura di markup di un pacchetto che può cambiare, o se hai altri motivi per preferire che la versione Livefyre in esecuzione non venga modificata in alcun modo.

Un esempio di integrazione con `Livefyre.require` potrebbe essere il seguente:

```
<!-- First add Livefyre.js to the page --> 
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
  
<!-- Then load up all the desired Livefyre packages and Do Stuff in the callback --> 
<script> 
Livefyre.require([ 
    'lfawesome#1', 
    'lfsuperawesome#2.1.2' 
], function (LFAwesome, LFSuperAwesome) { 
    var greatness = new LFAwesome(); 
    // etc.. 
}); 
</script>
```

## Pacchetti disponibili {#section_ygd_dwg_xz}

Ti stai chiedendo quali pacchetti JavaScript Livefyre sono disponibili tramite `Livefyre.require`? Qui puoi sempre trovare un elenco aggiornato dei pacchetti supportati e delle loro versioni più recenti: [packages.html](https://cdn.livefyre.com/packages.html).

## Verifica delle versioni precedenti dei pacchetti {#section_pgm_dpg_xz}

A volte può essere utile testare una prossima versione di un pacchetto Livefyre per assicurarti che funzioni sul tuo sito web o per testare l&#39;accettazione di una funzione che è in fase di sviluppo su tua richiesta. Oltre a includere un intervallo di versioni semantiche, è possibile specificare l’ambiente UAT prerelease.

Ad esempio, per richiedere la versione UAT di `fyre.conv`, le applicazioni Commenti, Blog live e Chat.

```
Livefyre.require(['fyre.conv#uat'], callback); 
```
