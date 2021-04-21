---
description: L’oggetto di configurazione Note è un oggetto JSON utilizzato per specificare il contenuto di cui l’app Livefyre esegue il rendering sulla pagina.
title: Opzioni di configurazione delle note elenco
exl-id: efebf9e5-6623-4953-a8f6-c58495304ac1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 1%

---

# Opzioni di configurazione note{#sidenotes-configuration-options}

L’oggetto di configurazione Note è un oggetto JSON utilizzato per specificare il contenuto di cui l’app Livefyre esegue il rendering sulla pagina.

L&#39;oggetto contiene i seguenti parametri:

| Parametro | Tipo | Descrizione |
|--- |--- |--- |
| authDelegate | ** requiredobject | Delegato di autenticazione inizializzato nuovo o vecchio stile. |
| collectionMeta | ** requiredobject | Per ulteriori informazioni, consulta token collectionMeta . |
| customIcon | ** optionalstring | Imposta l’URL di un’icona di avvio personalizzata. Valori predefiniti della bolla Livefyre. |
| customStyles | ** optionalobject | Aggiunge stili personalizzati per modificare l’aspetto delle note a margine. Per ulteriori informazioni, consulta Stili personalizzati . |
| disableStream | ** optionalBoolean | Se true, disabilita lo streaming in tempo reale in questa istanza di Sidenotes (non in altri flussi di commenti). Il valore predefinito è false. |
| ambiente | ** optionalstring | Specifica l’ambiente UAT di Livefyre. L’unico valore possibile è `t402.livefyre.com`. Per la produzione questo parametro deve essere rimosso. |
| iconVisibility | ** optionalobject o string | Definisce se l’icona Note a forma di barra laterale sarà visibile al passaggio del mouse o in modalità statica. Se si tratta di una stringa, verrà utilizzata per entrambe le versioni dell’icona del blocco (vuota e con Note a margine). Se si tratta di un oggetto, è necessario specificare ogni tipo: {vuoto: &quot;hover&quot;, num: &quot;static&quot;}. Il valore predefinito è statico. |
| inlineThreads | ** optionalboolean | Se true, i thread Sidenote vengono inseriti direttamente dopo il blocco a cui sono associati. Il valore predefinito è false. |
| numSidenotesEl | ** optionalobject, string o array | Specifica quale elemento verrà decorato dal widget di conteggio Note a margine. (Questo widget mostra il numero di note sulla pagina e le informazioni sulle note a margine.) Se il selettore di stringhe corrisponde a più di un elemento, verrà scelto il primo. (utilizza le specifiche del selettore DOM CSS3.) |
| position | ** optionalstring | Determina la posizione della finestra a comparsa quando si fa clic su un elemento con Note a comparsa abilitato. I valori possibili sono &quot;smart&quot;, &quot;left&quot;, &quot;right&quot;, &quot;bottom&quot;. L’impostazione predefinita è &quot;intelligente&quot;, che allinea la finestra a comparsa a destra della pagina a meno che non vi sia spazio sufficiente (in tal caso si sposterà sotto il contenuto). |
| selettori | ** required, string o array | Specifica gli elementi su cui devono essere visualizzate le icone del modulo di avvio. (utilizza le specifiche del selettore DOM CSS3.) Se si tratta di un oggetto, include una sezione &quot;include&quot; e una sezione &quot;Escludi&quot; che applicheranno il selettore CSS per eventuali inclusioni corrispondenti e rimuovono tutti gli elementi che corrispondono alle esclusioni. Se stringa, includerà eventuali elementi corrispondenti nella pagina. Se array, elenca gli elementi da includere. |
| stringhe | ** optionalobject | Aggiunge stringhe di testo personalizzate per modificare qualsiasi lingua o testo in tutta l&#39;applicazione. Per ulteriori informazioni, vedere Stringhe personalizzate. |
| threadContainerEl | ** optionalobject, string o array | Specifica un elemento in cui verrà visualizzato il thread delle note di margine. Questo parametro consente di riposizionare il thread. Se il selettore di stringhe corrisponde a più di un elemento, verrà scelto il primo. (utilizza le specifiche del selettore DOM CSS3.) |
