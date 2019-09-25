---
description: L'oggetto config Sidenotes è un oggetto JSON utilizzato per specificare il contenuto di cui l'app Livefyre esegue il rendering sulla pagina.
seo-description: L'oggetto config Sidenotes è un oggetto JSON utilizzato per specificare il contenuto di cui l'app Livefyre esegue il rendering sulla pagina.
seo-title: Opzioni di configurazione Sidenotes
solution: Experience Manager
title: Opzioni di configurazione Sidenotes
uuid: 067e51e6-9720-4226-a805-c7a07c8cdaa0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Opzioni di configurazione Sidenotes{#sidenotes-configuration-options}

L'oggetto config Sidenotes è un oggetto JSON utilizzato per specificare il contenuto di cui l'app Livefyre esegue il rendering sulla pagina.

L'oggetto contiene i seguenti parametri:

| Parametro | Tipo | Descrizione |
|--- |--- |--- |
| authDelegate | *oggetto obbligatorio* | Delegato di autenticazione inizializzato nuovo o vecchio stile. |
| collectionMeta | *oggetto obbligatorio* | Consulta collectionMeta token per ulteriori informazioni. |
| customIcon | *stringa facoltativa* | Imposta l'URL di un'icona di avvio personalizzata. Il valore predefinito è la bolla di Livefyre. |
| customStyles | *oggetto facoltativo* | Aggiunge stili personalizzati per modificare l’aspetto delle note. Per ulteriori informazioni, vedere Stili personalizzati. |
| disableStream | *facoltativo* booleano | Se true, disabilita lo streaming in tempo reale in questa istanza di Sidenotes (non in altri flussi di commenti). Il valore predefinito è false. |
| ambiente | *stringa facoltativa* | Specifica l'ambiente Livefyre UAT. L'unico valore possibile è `t402.livefyre.com`. Per la produzione questo parametro deve essere rimosso. |
| iconVisibility | *oggetto o stringa opzionale* | Definisce se l’icona delle note sarà visibile al passaggio del mouse o se sarà statica. Se si tratta di una stringa, verrà utilizzata per entrambe le versioni dell'icona del blocco (vuota e con note). Se si tratta di un oggetto, è necessario specificare ogni tipo: {empty: "hover", num: "static"}. Il valore predefinito è static. |
| inlineThread | *facoltativo* boolean | Se è true, i thread Sidenote vengono inseriti direttamente dopo il blocco a cui sono associati. Il valore predefinito è false. |
| numSidenotesEl | *oggetto, stringa o array facoltativi* | Specifica quale elemento verrà decorato dal widget di conteggio Sidenotes. (Questo widget mostra il numero di barre laterali sulla pagina e informazioni sulle note). Se il selettore delle stringhe corrisponde a più di un elemento, verrà scelto il primo. (utilizza la specifica del selettore DOM CSS3.) |
| position | *stringa facoltativa* | Determina la posizione della finestra a comparsa quando si fa clic su un elemento con le note abilitate. I valori possibili sono "smart", "left", "right", "bottom". Il valore predefinito è "smart", che allinea la finestra a comparsa a destra della pagina, a meno che non vi sia spazio sufficiente (nel qual caso si sposterà sotto il contenuto). |
| selettori | *oggetto, stringa o array richiesti* | Specifica gli elementi sui quali devono essere visualizzate le icone di avvio. (utilizza la specifica del selettore DOM CSS3.) Se si tratta di un oggetto, include una sezione "include" e una sezione "esclude" che applicheranno il selettore CSS per eventuali includenze corrispondenti, e rimuovono eventuali elementi che corrispondono agli esclusi. Se stringa, includerà eventuali elementi corrispondenti nella pagina. Se array, elenca gli elementi da includere. |
| strings | *oggetto facoltativo* | Aggiunge stringhe di testo personalizzate per modificare qualsiasi lingua o testo in tutta l'applicazione. Per ulteriori informazioni, vedere Stringhe personalizzate. |
| threadContainerEl | *oggetto, stringa o array facoltativi* | Specifica un elemento in cui verrà visualizzato il thread di sidenotes. Questo parametro consente di riposizionare il thread. Se il selettore delle stringhe corrisponde a più di un elemento, verrà scelto il primo. (utilizza la specifica del selettore DOM CSS3.) |

