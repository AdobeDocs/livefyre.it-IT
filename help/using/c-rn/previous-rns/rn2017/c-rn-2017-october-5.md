---
description: Note sulla versione del 5 ottobre 2017.
title: 5 ottobre 2017
exl-id: 6e39a86e-82dd-47ff-ad68-2b483f8b1921
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 3%

---

# 5 ottobre 2017{#october}

Note sulla versione del 5 ottobre 2017.

## Versione di produzione

| **Tipo di problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Bug | Identità Livefyre | I clienti che utilizzano l’identità Livefyre per effettuare l’accesso riscontravano problemi durante la visualizzazione o l’aggiornamento degli avatar durante la pubblicazione nelle app di commento. Questo problema è stato risolto ora, in quanto gli avatar sono visibili e disponibili per l’aggiornamento. |
| Bug | Rights Management | È stato corretto un bug a causa del quale venivano visualizzati nomi utente lunghi nella scheda Modale diritti . |
| Miglioramento | Flussi | Aggiunta la possibilità di premere il tasto Tab in un campo di testo Streams per completare un termine di ricerca. |

## Versione UAT

| **Tipo di problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Miglioramento | Filmstrip | Quando un cliente distribuisce un’app a strisce di film, l’UGC appena inviato avrà accanto un’etichetta &quot;nuova&quot; per identificarli rapidamente. |
| Miglioramento | Filmstrip | Filmstrip è una nuova app di visualizzazione, progettata principalmente per mostrare gli UGC in scenari di e-commerce, come pagine di prodotto o siti web transazionali. La striscia di lastra allinea orizzontalmente l&#39;UGC per essere visualizzato come un rullo della telecamera, un pezzo alla volta. Gli utenti finali possono navigare in Filmstrip facendo clic sulle frecce laterali per scorrere il contenuto disponibile. |
| Miglioramento | Libreria | I file caricati nella libreria da un cliente ricevono automaticamente i diritti. Questa è una funzione utile quando gli utenti hanno attivato il filtro &quot;Richiedi diritti concessi&quot; nelle loro app. |
| Miglioramento | Identità Livefyre | I clienti possono ora utilizzare le proprie credenziali Github per accedere a Identità LIvefyre e partecipare alle nostre app di commento. |
| Bug | Rights Management | È stato corretto un bug che consentiva l’inserimento di caratteri unicode nei messaggi di richiesta dei diritti di ignorare la convalida. |
| Miglioramento | SICURO | Sono stati aggiunti miglioramenti minori al rilevamento di spam SAFE. |
| Bug | Servizio | Gli utenti che non dispongono di e-mail valide dispongono di e-mail costruite per loro. È stato risolto un problema relativo ai registri di produzione a causa del quale il sistema non inviava e-mail a tali utenti. |
| Miglioramento | Studio | È stato aggiornato il collegamento della Guida di Livefyre nella barra di navigazione superiore. |
| Miglioramento | Commerce UGC | Come cliente ora posso creare una singola app Livefyre (Mosaic, FilmStrip o Media Wall) e incorporarla in più pagine di prodotto, che filtra dinamicamente l’UGC appropriato per ogni pagina di prodotto (ad esempio UGC con scarpe per una pagina di prodotto Scarpe). |
| Miglioramento | Commerce UGC | Ora i clienti possono caricare manualmente un catalogo di prodotti google in Livefyre studio utilizzando un’esportazione di file JSON. Questo consente al cliente di associare UGC ai prodotti di quel catalogo e visualizzarli nelle nostre app abilitate per l’e-commerce. |
| Miglioramento | Commerce UGC | I clienti possono selezionare le cartelle di prodotti che desiderano utilizzare per filtrare l’app di e-commerce in base all’ID prodotto. Per esempio voglio che il mio nuovo filmstrip appaia nelle mie pagine di prodotti scarpe e borse da donna, quindi selezionerò solo le cartelle di prodotti &quot;Women&#39;s shoes collection&quot; e &quot;Women&#39;s bag&quot;. |
| Miglioramento | Commerce UGC | I clienti Livefyre ora possono filtrare l’UGC pubblicato nelle loro app solo se dispongono dei diritti concessi. Ad esempio, un cliente può curare e pubblicare una selezione di elementi, ma questi saranno sottoposti a rendering nell’app solo dopo che l’autore avrà concesso loro i diritti. Ciò è particolarmente importante per i casi d&#39;uso dell&#39;e-commerce, in cui l&#39;UGC viene utilizzato a fini commerciali. |
