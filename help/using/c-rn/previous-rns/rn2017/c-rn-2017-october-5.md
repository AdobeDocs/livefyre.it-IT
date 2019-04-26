---
description: Note sulla versione del 5 ottobre 2017.
seo-description: Note sulla versione del 5 ottobre 2017.
seo-title: 5 ottobre 2017
title: 5 ottobre 2017
uuid: 62 e 9 e 4 ee -1644-4 d 22-9589-2 e 208 a 68 aaeb
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# 5 ottobre 2017{#october}

Note sulla versione del 5 ottobre 2017.

## Versione produzione

| **Tipo di edizione** | **Componente** | **Nota sulla versione** |
|---|---|---|
| Bug | Livefyre Identity | I clienti che utilizzano Livefyre identità per effettuare l'accesso riscontravano dei problemi durante la visualizzazione o l'aggiornamento dei loro avatar quando si pubblicavano le app per commenti. Ora è stato corretto, poiché gli avatar sono ora visibili e disponibili per l'aggiornamento. |
| Bug | Rights Management | È stato corretto un bug con la visualizzazione dei nomi utente lunghi nella scheda Rights Modmodal. |
| Miglioramento | Flussi | Aggiunta la capacità di accedere al tasto di tabulazione in un campo di testo Flussi per completare un termine di ricerca. |

## Versione UAT

| **Tipo di edizione** | **Componente** | **Nota sulla versione** |
|---|---|---|
| Miglioramento | Filmstrip | Quando un cliente distribuisce un'app filmstrip, la nuova etichetta dell'UGC in streaming avrà un'etichetta "nuova", pronta per essere identificata rapidamente. |
| Miglioramento | Filmstrip | Filmstrip è una nuova app di visualizzazione, progettata principalmente per mostrare UGC negli scenari di e-commerce, ad esempio pagine di prodotti o siti web transazionali. Filmstrip allinea in orizzontale l'UGC affinché venga visualizzato come rullino fotografico, un pezzo al momento. Gli utenti finali possono navigare nella striscia facendo clic sulle frecce laterali per scorrere il contenuto disponibile. |
| Miglioramento | Libreria | I file caricati nella libreria da parte di un cliente verranno automaticamente concessi. Questa funzione è utile quando gli utenti hanno attivato il filtro «Richiedi diritti autorizzati» nelle app. |
| Miglioramento | Livefyre Identity | I clienti possono ora utilizzare le credenziali Github per accedere a livefyre Identity e partecipare alle nostre app di commenti. |
| Bug | Rights Management | Risoluzione di un bug che consentiva l'inserimento di caratteri unicode nei messaggi Request Request (Richiesta diritti) per aggirare la convalida. |
| Miglioramento | SAFE | Miglioramenti secondari aggiunti al rilevamento SAFE Spam. |
| Bug | Servizio | Gli utenti senza e-mail valide sono dotati di e-mail create. È stato risolto un problema relativo ai registri di produzione in cui il sistema non inviava e-mail a tali utenti. |
| Miglioramento | Studio | È stato aggiornato il collegamento di Livefyre Help nella barra di navigazione superiore. |
| Miglioramento | UGC Commerce | In qualità di cliente posso ora creare una singola app Livefyre (Mosaic, filmstrip o Media Wall) e incorporarla in più pagine di prodotto, che filtra dinamicamente l'UGC appropriato per ogni pagina del prodotto (UGC con scarpe per una pagina di prodotto Shoe). |
| Miglioramento | UGC Commerce | I clienti possono caricare manualmente un catalogo di prodotti Google nel studio Livefyre utilizzando un'esportazione JSON. Questo consente al cliente di accoppiare UGC con i prodotti del catalogo e visualizzarli nelle app abilitate per il commercio. |
| Miglioramento | UGC Commerce | I clienti possono selezionare le cartelle di prodotti che desiderano utilizzare per filtrare l'app per e-commerce in base all'ID prodotto. Ad esempio, desidero che la nuova striscia filmstrip venga visualizzata nelle pagine dei prodotti delle scarpe e dei prodotti da donna, quindi selezionerò solo le cartelle «Raccolta delle scarpe da donna» e «Borse da donna». |
| Miglioramento | UGC Commerce | I clienti Livefyre possono ora filtrare l'UGC pubblicato nelle loro app solo se sono stati concessi loro dei diritti. Ad esempio, un cliente può curare e pubblicare una selezione di elementi, ma solo una volta che tali elementi saranno stati concessi dall'autore. Questo è particolarmente importante per i casi d'uso per e-commerce, dove l'UGC è utilizzato a scopi commerciali. |

