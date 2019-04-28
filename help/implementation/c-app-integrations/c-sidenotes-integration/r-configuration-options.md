---
description: L'oggetto configurazione Sidenotes è un oggetto JSON utilizzato per specificare il contenuto renderizzato dall'app Livefyre sulla pagina.
seo-description: L'oggetto configurazione Sidenotes è un oggetto JSON utilizzato per specificare il contenuto renderizzato dall'app Livefyre sulla pagina.
seo-title: Opzioni di configurazione Sidenotes
solution: Experience Manager
title: Opzioni di configurazione Sidenotes
uuid: 067 e 51 e 6-9720-4226-a 805-c 7 a 07 c 8 cdaa 0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Opzioni di configurazione Sidenotes{#sidenotes-configuration-options}

L&#39;oggetto configurazione Sidenotes è un oggetto JSON utilizzato per specificare il contenuto renderizzato dall&#39;app Livefyre sulla pagina.

L&#39;oggetto contiene i seguenti parametri:

| Parametro | Tipo | Descrizione |
|--- |--- |--- |
| Authdelegate | *required* object | Delegato autenticazione inizializzato nuovo o precedente. |
| Collectionmeta | *required* object | Per ulteriori informazioni, consultate Token collectionmeta. |
| Customicon | *optional* string | Imposta l&#39;URL di un&#39;icona di avvio personalizzata. Il valore predefinito è Livefyre. |
| Customstyles | *optional* object | Aggiunge stili personalizzati per modificare l&#39;aspetto di Sidenotes. Per ulteriori informazioni, vedere Stili personalizzati. |
| Disablestream | *optional* Boolean | Se true, disattiva lo streaming in tempo reale in questa istanza Sidenotes (non in altri flussi di commento). Il valore predefinito è false. |
| environment | *optional* string | Specifica l&#39;ambiente UVEFYRE UAT. L&#39;unico valore possibile `t402.livefyre.com`è. Per la produzione, questo parametro deve essere rimosso. |
| Iconvisibility | *oggetto o* stringa opzionale | Definisce se l&#39;icona Sidenotes sarà visibile al passaggio del mouse o statico. Se si tratta di una stringa, verrà utilizzata per entrambe le versioni dell&#39;icona Block (vuoto e con Sidenotes). Se un oggetto è, è necessario specificare ogni tipo: {empty: &#39; hover &#39;, num: &#39; static &#39;}. Il valore predefinito è statico. |
| Inlinethreads | *optional* boolean | Se true, i thread Sidenote vengono inseriti direttamente dopo il blocco a cui sono associati. Il valore predefinito è false. |
| Numsidenotesel | *oggetto,* stringa o matrice opzionale | Specifica quale elemento verrà decorato dal widget Sidenotes. (Questo widget mostra il numero di filiali nella pagina e informazioni su Sidenotes.) Se il selettore stringa corrisponde a più di un elemento, la prima verrà scelta. (utilizza la spec selettore DOM CSS 3). |
| position | *optional* string | Determina la posizione della finestra a comparsa quando si fa clic su un elemento abilitato per Sidenotes. I valori possibili sono «smart», «left», «right», «bottom». Il valore predefinito è «intelligente» che allinea il menu a comparsa a destra della pagina, a meno che non sia sufficiente spazio (nel qual caso si sposta sotto il contenuto). |
| selectors | *oggetto,* stringa o matrice richiesti | Specifica gli elementi in cui devono essere visualizzate le icone di avvio. (utilizza la spec selettore DOM CSS 3). Se l&#39;oggetto include una sezione &quot;include&quot; e una sezione &quot;excludes&quot; che applica il selettore CSS per qualsiasi corrispondenza corrispondente, e rimuove qualsiasi elemento che corrisponda agli esclusivi. Se stringa, includerà qualsiasi elemento corrispondente sulla pagina. Se array, elenca gli elementi da includere. |
| stringhe | *optional* object | Aggiunge stringhe di testo personalizzate per modificare qualsiasi lingua o testo nell&#39;applicazione. Per ulteriori informazioni, consultate Stringhe personalizzate. |
| Threadcontainerel | *oggetto,* stringa o matrice opzionale | Specifica un elemento in cui verrà visualizzato il thread di sidenotes. Questo parametro consente di riposizionare il thread. Se il selettore stringa corrisponde a più di un elemento, la prima verrà scelta. (utilizza la spec selettore DOM CSS 3). |

