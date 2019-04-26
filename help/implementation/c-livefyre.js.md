---
description: La libreria di base Livefyre utilizzata per abilitare Livefyre sul sito.
seo-description: La libreria di base Livefyre utilizzata per abilitare Livefyre sul
  sito.
seo-title: Livefyre. js
solution: Experience Manager
title: Livefyre. js
uuid: 7 b 3 eca 57-d 5 e 8-416 d-badf-a 9 c 51 d 10 dadd
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre. js {#livefyre-js}

La libreria di base Livefyre utilizzata per abilitare Livefyre sul sito.

`Livefyre.js` è la libreria di base che puoi installare in tutte le pagine Web abilitate per Livefyre. Definisce l'oggetto globale `window.Livefyre` e un singolo metodo pubblico, `Livefyre.require`che può essere utilizzato per caricare altre librerie Jvefyre Javfyre con l'Aiuto [di Livefyre Apps](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md), [integrazione del provider di autenticazione con Livefyre](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) e altro.

## Aggiungi al sito {#section_cst_twg_xz}

Aggiungi il `<script>` seguente tag al modello Web o pagina Web. Se possibile, aggiungetela alla `<head>` sezione del documento HTML in modo che venga caricata rapidamente.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

>[!NOTE]
>
>Questo script incorpora un file molto piccolo (~ 1 Kb) denominato Livefyre. js scout che caricherà successivamente la versione più recente di Livefyre. js sul protocollo con cui è stata acceduta la pagina Web (HTTP o HTTPS).

## Livefyre. require {#section_ipq_hwg_xz}

`Livefyre.require` è un loader javascript personalizzato come [curl. js](https://github.com/cujojs/curl) o [requirejs](https://requirejs.org/). Può essere utilizzato per caricare la maggior parte dei pacchetti pubblicati da Livefyre e presentare un percorso di integrazione pratico e intuitivo.

I pacchetti accessibili tramite vengono `Livefyre.require` distribuiti tramite [la versione Semantic Versioning](https://semver.org/). I pacchetti possono essere richiesti a una versione specifica o a una serie di versioni, in modo che la pagina Web possa trarre automaticamente vantaggio dalle nuove funzioni di bug. con la flessibilità di integrare Livefyre sul sito. Sono disponibili tre livelli di fissaggio della versione `Livefyre.require`.

* **package-name # 1:** Fissa alla versione principale v 1. Riceverai tutti i nuovi aggiornamenti che mantengono un'API compatibile con le versioni precedenti. Passa a una versione principale per ricevere correzioni di bug e miglioramenti minori delle funzioni per quella versione.
* **package-name # 1.1:** Fissa alla versione secondaria v 1.1. Avrai tutti i bug a questa versione secondaria. Livefyre Engineering rimuove sempre la versione secondaria di un pacchetto se il comportamento predefinito o l'ambito funzionale cambia in modo da causare un comportamento nuovo e imprevisto sulla pagina Web. Scorrete su una versione secondaria se desiderate ricevere correzioni di bug automatizzate, ma nessuna funzionalità aggiuntiva o modifiche al comportamento predefinito.
* **package-name # 1.1.1:** Fissa alla patch v 1.1.1. Il comportamento di questa incorporazione non cambia mai, anche in presenza di bug. Aggiungete a una versione patch se disponete di sofisticate personalizzazioni CSS per il sito che dipendono dalla struttura di marcatura di un pacchetto, o se avete altri motivi per preferire che la versione Livefyre in esecuzione non cambi in alcun modo.

Un esempio di integrazione con l'esempio `Livefyre.require` potrebbe essere simile al seguente:

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

Wondering which Livefyre javascript packages are available through `Livefyre.require`? Puoi sempre trovare un elenco aggiornato dei pacchetti supportati e delle relative versioni più recenti: [packages.html](https://cdn.livefyre.com/packages.html).

## Verifica delle versioni pre-release dei pacchetti {#section_pgm_dpg_xz}

A volte potrebbe essere utile testare una versione imminente di un pacchetto Livefyre per accertarvi che funzionerà sul sito Web o sul test di accettazione a una funzione sviluppata su richiesta. Oltre a includere un intervallo di versione Semantica, è possibile specificare l'ambiente UAT prerelease.

Ad esempio, la versione UAT di `fyre.conv`, i Commenti, il Blog live e le applicazioni Chat.

```
Livefyre.require(['fyre.conv#uat'], callback); 
```
