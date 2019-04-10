---
description: L'oggetto configurazione Sidenotes è un oggetto JSON utilizzato per specificare
  il contenuto renderizzato dall'app Livefyre sulla pagina.
seo-description: L'oggetto configurazione Sidenotes è un oggetto JSON utilizzato per
  specificare il contenuto renderizzato dall'app Livefyre sulla pagina.
seo-title: Opzioni di configurazione Sidenotes
solution: Experience Manager
title: Opzioni di configurazione Sidenotes
uuid: 067 e 51 e 6-9720-4226-a 805-c 7 a 07 c 8 cdaa 0
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Opzioni di configurazione Sidenotes{#sidenotes-configuration-options}

L'oggetto configurazione Sidenotes è un oggetto JSON utilizzato per specificare il contenuto renderizzato dall'app Livefyre sulla pagina.

L'oggetto contiene i seguenti parametri:

| Parametro | Tipo | Descrizione |
|--- |--- |--- |
| Authdelegate | *required* object | Delegato autenticazione inizializzato nuovo o precedente. |
| Collectionmeta | *required* object | Per ulteriori informazioni, consultate Token collectionmeta. |
| Customicon | *optional* string | Imposta l'URL di un'icona di avvio personalizzata. Il valore predefinito è Livefyre. |
| Customstyles | *optional* object | Aggiunge stili personalizzati per modificare l'aspetto di Sidenotes. Per ulteriori informazioni, vedere Stili personalizzati. |
| Disablestream | *optional* Boolean | Se true, disattiva lo streaming in tempo reale in questa istanza Sidenotes (non in altri flussi di commento). Il valore predefinito è false. |
| environment | *optional* string | Specifica l'ambiente UVEFYRE UAT. L'unico valore possibile `t402.livefyre.com`è. Per la produzione, questo parametro deve essere rimosso. |
| Iconvisibility | *oggetto o* stringa opzionale | Definisce se l'icona Sidenotes sarà visibile al passaggio del mouse o statico. Se si tratta di una stringa, verrà utilizzata per entrambe le versioni dell'icona Block (vuoto e con Sidenotes). Se un oggetto è, è necessario specificare ogni tipo: {empty: ' hover ', num: ' static '}. Il valore predefinito è statico. |
| Inlinethreads | *optional* boolean | Se true, i thread Sidenote vengono inseriti direttamente dopo il blocco a cui sono associati. Il valore predefinito è false. |
| Numsidenotesel | *oggetto,* stringa o matrice opzionale | Specifica quale elemento verrà decorato dal widget Sidenotes. (Questo widget mostra il numero di filiali nella pagina e informazioni su Sidenotes.) Se il selettore stringa corrisponde a più di un elemento, la prima verrà scelta. (utilizza la spec selettore DOM CSS 3). |
| position | *optional* string | Determina la posizione della finestra a comparsa quando si fa clic su un elemento abilitato per Sidenotes. I valori possibili sono «smart», «left», «right», «bottom». Il valore predefinito è «intelligente» che allinea il menu a comparsa a destra della pagina, a meno che non sia sufficiente spazio (nel qual caso si sposta sotto il contenuto). |
| selectors | *oggetto,* stringa o matrice richiesti | Specifica gli elementi in cui devono essere visualizzate le icone di avvio. (utilizza la spec selettore DOM CSS 3). Se l'oggetto include una sezione "include" e una sezione "excludes" che applica il selettore CSS per qualsiasi corrispondenza corrispondente, e rimuove qualsiasi elemento che corrisponda agli esclusivi. Se stringa, includerà qualsiasi elemento corrispondente sulla pagina. Se array, elenca gli elementi da includere. |
| stringhe | *optional* object | Aggiunge stringhe di testo personalizzate per modificare qualsiasi lingua o testo nell'applicazione. Per ulteriori informazioni, consultate Stringhe personalizzate. |
| Threadcontainerel | *oggetto,* stringa o matrice opzionale | Specifica un elemento in cui verrà visualizzato il thread di sidenotes. Questo parametro consente di riposizionare il thread. Se il selettore stringa corrisponde a più di un elemento, la prima verrà scelta. (utilizza la spec selettore DOM CSS 3). |

