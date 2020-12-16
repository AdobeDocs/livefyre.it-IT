---
description: Note sulla versione per la versione del 5 ottobre 2017.
seo-description: Note sulla versione per la versione del 5 ottobre 2017.
seo-title: 5 ottobre 2017
title: 5 ottobre 2017
uuid: 62e9e4ee-1644-4d22-9589-2e208a68aaeb
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 3%

---


# 5 ottobre 2017{#october}

Note sulla versione per la versione del 5 ottobre 2017.

## Release produzione

| **Tipo problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Bug | Identità Livefyre | I clienti che utilizzavano l&#39;identità Livefyre per accedere non riuscivano a vedere o aggiornare gli avatar durante la pubblicazione nelle app di commenti. Questo è stato corretto ora, poiché gli avatar sono ora visibili e disponibili per l&#39;aggiornamento. |
| Bug | Rights Management | È stato corretto un bug a causa del quale venivano visualizzati nomi utente lunghi nella scheda Rights Modal. |
| Miglioramento | Streams | Aggiunta la possibilità di premere il tasto di tabulazione in un campo di testo Streams per completare un termine di ricerca. |

## Rilascio UAT

| **Tipo problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Miglioramento | Filmstrip | Quando un cliente distribuisce un’app per strisce di film, l’UGC di recente streaming avrà una &quot;nuova&quot; etichetta accanto a esso per identificarli rapidamente. |
| Miglioramento | Filmstrip | Filmstrip è una nuova app di visualizzazione, progettata principalmente per mostrare gli UGC negli scenari di e-commerce, come pagine di prodotti o siti Web transazionali. La striscia di pellicola allinea orizzontalmente l&#39;UGC da visualizzare come rullino, un pezzo alla volta. Gli utenti finali possono spostarsi nell’area Filmstrip facendo clic sulle frecce laterali per scorrere il contenuto disponibile. |
| Miglioramento | Libreria | I file caricati nella libreria da un cliente ricevono automaticamente i diritti. Si tratta di una funzione utile quando gli utenti hanno attivato il filtro &quot;Richiedi diritti concessi&quot; nelle loro app. |
| Miglioramento | Identità Livefyre | Adesso, i clienti possono utilizzare le proprie credenziali Github per accedere all&#39;Identità LIVYRE e partecipare alle nostre app di commenti. |
| Bug | Rights Management | È stato corretto un bug che consentiva l’inserimento di caratteri Unicode nei messaggi di richiesta dei diritti di ignorare la convalida. |
| Miglioramento | SICURO | Miglioramenti minori aggiunti al rilevamento di spam SAFE. |
| Bug | Servizio | Gli utenti che non dispongono di e-mail valide dispongono di e-mail costruite per loro. È stato risolto un problema relativo ai registri di produzione a causa del quale il sistema non inviava e-mail a tali utenti. |
| Miglioramento | Studio | È stato aggiornato il collegamento della guida di Livefyre nella barra di navigazione superiore. |
| Miglioramento | Commerce UGC | Come cliente ora posso creare una singola app Livefyre (Mosaic, FilmStrip o Media Wall) e incorporarla in più pagine di prodotto, che filtra dinamicamente l&#39;UGC appropriato per ogni pagina di prodotto (ad esempio UGC con shoes per una pagina di prodotto Shoe). |
| Miglioramento | Commerce UGC | Adesso, i clienti possono caricare manualmente un catalogo di prodotti Google nello studio Livefyre utilizzando un&#39;esportazione di file JSON. Questo consente al cliente di associare UGC ai prodotti di quel catalogo e visualizzarli nelle app abilitate per il commercio. |
| Miglioramento | Commerce UGC | I clienti possono selezionare le cartelle di prodotti che desiderano utilizzare per filtrare l&#39;app di e-commerce in base all&#39;ID prodotto. Ad esempio, voglio che il mio nuovo filmstrip venga visualizzato nelle pagine di prodotto delle mie scarpe da donna e borse da donna, quindi selezionerò solo le cartelle di prodotti &quot;Women&#39;s shoes collection&quot; e &quot;Women&#39;s bag&quot;. |
| Miglioramento | Commerce UGC | I clienti Livefyre ora possono filtrare l&#39;UGC pubblicato nelle loro app solo se dispongono dei diritti concessi. Ad esempio, un cliente può curare e pubblicare una selezione di elementi, ma il rendering di tali elementi sarà eseguito nell&#39;app solo dopo che l&#39;autore avrà concesso loro i diritti. Ciò è particolarmente importante per i casi di utilizzo del commercio elettronico, in cui l&#39;UGC è utilizzato a fini commerciali. |

