---
description: La libreria Livefyre di base utilizzata per alimentare Livefyre sul sito.
seo-description: La libreria Livefyre di base utilizzata per alimentare Livefyre sul sito.
seo-title: Livefyre.js
solution: Experience Manager
title: Livefyre.js
uuid: 7b3eca57-d5e8-416d-badf-a9c51d10dadd
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre.js {#livefyre-js}

La libreria Livefyre di base utilizzata per alimentare Livefyre sul sito.

`Livefyre.js` è la libreria di base che potete installare su ogni pagina Web abilitata per Livefyre. Definisce l' `window.Livefyre` oggetto globale e un singolo metodo pubblico, `Livefyre.require`che può essere utilizzato per caricare altre librerie JavaScript Livefyre che consentono di [incorporare le app](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)Livefyre, [integrare il provider di autenticazione con Livefyre](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) e altro ancora.

## Aggiungi al tuo sito {#section_cst_twg_xz}

Aggiungete il seguente `<script>` tag alla pagina Web o al modello di sito Web. Se possibile, aggiungetelo alla `<head>` sezione del documento HTML in modo che venga caricato rapidamente.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

>[!NOTE]
>
>Questo script incorporerà un file molto piccolo (~1 Kb) denominato Livefyre.js scout che in seguito caricherà l'ultima versione di Livefyre.js sul protocollo con cui è stato effettuato l'accesso alla pagina Web (HTTP o HTTPS).

## Livefyre.request {#section_ipq_hwg_xz}

`Livefyre.require` è un caricatore di moduli JavaScript personalizzato come [curl.js](https://github.com/cujojs/curl) o [RequireJS](https://requirejs.org/). Può essere utilizzato per caricare la maggior parte dei pacchetti pubblicati da Livefyre e presenta un percorso di integrazione pratico e intuitivo.

I pacchetti accessibili tramite `Livefyre.require` le versioni vengono controllati mediante il controllo delle versioni [semantiche](https://semver.org/). I pacchetti possono essere richiesti in una versione specifica o in una serie di versioni, in modo che la pagina Web possa beneficiare automaticamente delle nuove funzioni di risoluzione dei bug. Questo offre flessibilità nell'integrazione di Livefyre sul sito. È possibile utilizzare tre livelli di blocco della versione con `Livefyre.require`.

* **** package-name#1: Eseguire il pin alla versione principale v1. Avrete a disposizione tutti i nuovi aggiornamenti per mantenere un'API compatibile con le versioni precedenti. Eseguire il pin a una versione principale per ricevere correzioni di bug e miglioramenti di funzionalità secondarie per tale versione.
* **** package-name#1.1: Fissaggio alla versione minore v1.1. Tutte le correzioni di bug verranno apportate a questa versione secondaria. Livefyre Engineering eseguirà sempre il backup della versione secondaria di un pacchetto se il suo comportamento predefinito o l'ambito funzionale cambiano in modo da causare nuovi comportamenti imprevisti sulla pagina Web. Eseguire il pin a una versione secondaria se si desidera ricevere correzioni di bug automatizzate, ma senza ulteriori funzionalità o modifiche al comportamento predefinito.
* **** package-name#1.1.1: Eseguire il pin alla versione della patch v1.1.1. Il comportamento di questo incorporamento non cambierà mai, anche in presenza di correzioni di bug. Fate clic su una versione della patch se disponete di numerose personalizzazioni CSS per il sito che dipendono dalla struttura di marcatura di un pacchetto che potrebbe essere modificata, oppure se avete altri motivi per preferire che la versione di Livefyre in esecuzione non venga modificata in alcun modo.

Un esempio di integrazione con `Livefyre.require` potrebbe essere:

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

Vi state chiedendo quali pacchetti JavaScript Livefyre sono disponibili tramite `Livefyre.require`? Puoi sempre trovare un elenco aggiornato dei pacchetti supportati e delle loro versioni più recenti qui: [packages.html](https://cdn.livefyre.com/packages.html).

## Verifica delle versioni pre-release dei pacchetti {#section_pgm_dpg_xz}

A volte può essere utile testare una versione imminente di un pacchetto Livefyre per essere certi che funzionerà sul sito Web o per testare l’accettazione di una funzione in fase di sviluppo su richiesta. Oltre a includere un intervallo di versioni semantiche, è possibile specificare l’ambiente UAT prerelease.

Ad esempio, quanto segue richiede la versione UAT delle applicazioni `fyre.conv`, Commenti, Live Blog e Chat.

```
Livefyre.require(['fyre.conv#uat'], callback); 
```
