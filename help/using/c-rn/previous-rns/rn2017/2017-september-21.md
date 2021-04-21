---
description: Note sulla versione per la versione del 21 settembre 2017.
title: 21 settembre 2017
exl-id: 6d01710e-dab4-4065-85c5-b00f45d8d4fd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 5%

---

# 21 settembre 2017{#september}

Note sulla versione per la versione del 21 settembre 2017.

## Versione di produzione

| **Tipo di problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Miglioramento | Commenti | Ora i clienti possono impostare la lunghezza massima per i commenti come parte della configurazione di rete. |
| Bug | App mobile | Questo bug corregge un problema relativo al rendering delle risposte nidificate in Mobile quando gli avatar sono disattivati. |
| Bug | Mosaico | È stato corretto un bug di produzione che rendeva Mosaic display Gray Boxes in IE11 in UGC. |
| Miglioramento | Mosaico | Ora i clienti possono specificare il numero di schede da visualizzare nell’app di visualizzazione Mosaic. |
| Bug | Rights Management | È stato corretto un bug che impediva a un utente di Studio di richiedere diritti sul contenuto di Instagram Carousel. |
| Bug | Studio | Sono stati aggiunti messaggi di errore più chiari durante la creazione di nuovi siti. |

## Versione UAT

| **Tipo di problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Miglioramento | App | Ora i clienti possono creare una singola app Livefyre (Mosaic, Filmstrip o Media Wall) e incorporarla in più pagine di prodotto, che filtrano dinamicamente l’UGC appropriato per ogni pagina di prodotto (ad esempio, UGC tagged for shoes display on the shoe product page). |
| Miglioramento | Filmstrip | Nell’app Filmstrip è presente un banner &quot;Nuovo&quot; che contrassegna i nuovi contenuti nell’app in modo che gli utenti finali possano identificare rapidamente i nuovi contenuti. |
| Miglioramento | Identità Livefyre | I clienti possono ora utilizzare le proprie credenziali Github per accedere all’identità Livefyre e partecipare alle nostre app di commento. |
| Bug | Rights Management | È stato corretto un bug che consentiva l’inserimento di caratteri unicode nei messaggi di richiesta dei diritti di ignorare la convalida. |
| Miglioramento | Studio | È stato aggiornato il collegamento della Guida di Livefyre nella barra di navigazione superiore. |
| Miglioramento | Commerce UGC | Ora i clienti possono caricare manualmente un catalogo di prodotti Google in LF studio utilizzando un’esportazione di file JSON. Questo consente al cliente di associare UGC ai prodotti di quel catalogo e visualizzarli nelle nostre app abilitate per l’e-commerce. |
| Miglioramento | Commerce UGC | I clienti possono selezionare le cartelle di prodotti che desiderano utilizzare per filtrare l’app di e-commerce in base all’ID prodotto. Ad esempio, voglio che il mio nuovo Filmstrip appaia nelle pagine dei prodotti per le mie scarpe e le mie borse da donna, quindi selezionerò solo le cartelle dei prodotti &quot;Women&#39;s shoes collection&quot; e &quot;Women&#39;s bag&quot;. |
| Miglioramento | Commerce UGC | I clienti Livefyre ora possono filtrare l’UGC pubblicato nelle loro app solo se dispongono dei diritti concessi. Ad esempio, un cliente può curare e pubblicare una selezione di elementi, ma questi verranno riprodotti nell’app solo dopo che l’autore avrà concesso loro i diritti. Ciò è particolarmente importante per i casi d&#39;uso del commercio elettronico, in cui l&#39;UGC viene utilizzato a fini commerciali. |
