---
description: Note sulla versione per la versione del 23 febbraio 2017.
title: 23 febbraio 2017
exl-id: 3a5708a1-4be6-447f-ae6e-8f5a37171ed7
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 7%

---

# 23 febbraio 2017{#february}

Note sulla versione per la versione del 23 febbraio 2017.

## Versione di produzione

| **Tipo di problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Miglioramento | Android SDK | SDK per Android riorganizzato per garantire che le directory di implementazione di esempio e di riferimento siano più chiaramente identificabili dalla loro posizione. |
| Miglioramento | SDK per Android | SDK per Android modificato per supportare ora una versione SDK minima di 14 (rispetto a 16). |
| Bug | App di conversazione | App di conversione migliorate per collegare sempre i profili utente, anche senza un’integrazione completa delle autorizzazioni. |
| Bug | Mosaico | È stato corretto un bug a causa del quale ora vengono distribuite tutte le immagini Twitter tramite HTTPS. |
| Miglioramento | Ricerca e flussi | È stata aggiunta la possibilità di eseguire ricerche per Instagram Places (check-in) nella libreria Instagram Search e nelle regole di flusso di Instagram. |
| Bug | Impostazioni | È stato corretto un bug che impediva il salvataggio degli account Twitter Social . |
| Bug | Ricerca social | È stato corretto un bug a causa del quale l’opzione &quot;Conceal esplicito images&quot; non funzionava correttamente. |
| Miglioramento | Memorizza 2 | È stata migliorata la funzione Storify 2 per supportare i permalink che aprono un modale (in precedenza l’app scorreva fino alla posizione del post sulla pagina). In Designer di Storify 2 è stata aggiunta una configurazione per alternare tra il comportamento di scorrimento e quello di collegamento permanente modale. Il comportamento del permalink modale sarà il comportamento predefinito. |
| Miglioramento | Memorizza 2 | Migliorata l’integrazione di Storify 2 Google AMP per produrre un file CSS più piccolo. |
| Miglioramento | Flussi | È stato corretto un bug nelle regole di Facebook a causa del quale il contenuto veniva inviato con metadati incompleti. |
| Bug | Flussi | Contenuto avanzato (immagini e video) dalle regole di flusso e-mail che sarà disponibile tramite HTTPS. |
| Bug | Flussi | È stata aggiunta un’etichetta per il valore del raggio mobile nelle mappe di Twitter Stream Rules. |
| Bug | Flussi | È stato corretto un bug relativo alle regole di streaming delle pagine Facebook e Facebook per inserire in modo appropriato i post con più allegati multimediali. |
| Miglioramento | Flussi | È stata aggiunta una nuova funzione per consentire agli utenti di scegliere di applicare o disabilitare le regole SAFE per regola di flusso. |
| Miglioramento | Studio | È stato corretto un bug a causa del quale il contenuto non veniva pubblicato o salvato correttamente se era già presente. |
| Bug | Studio | È stato corretto un bug a causa del quale più &amp;’s venivano aggiunti all’URL quando si utilizzavano i filtri in Studio. |
| Bug | Studio | È stato corretto un bug a causa del quale alcune caselle di controllo nei filtri di Studio non potevano essere deselezionate. |

## Versione UAT

| **Tipo di problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Bug | App | È stato corretto un bug per mostrare il contenuto nei moduli multimediali con le proporzioni corrette. |
| Bug | Parete multimediale | È stato corretto un bug a causa del quale il rendering di Media Walls non veniva eseguito se erano inclusi caratteri stranieri specifici. |
| Bug | Cerca | È stato corretto un bug a causa del quale le pagine venivano caricate in modo errato durante il paging nei risultati della ricerca con l’opzione &quot;Conceal esplicito images&quot; abilitata. |
| Miglioramento | Studio | Tempo di sessione aumentato prima della scadenza delle sessioni di accesso di Studio User . Una volta scaduta la sessione di Studio, l&#39;utente verrà reindirizzato per effettuare di nuovo l&#39;accesso. |
| Bug | Studio | È stato corretto un bug che talvolta impediva agli utenti di salvare le credenziali di Instagram. |
| Bug | Studio | È stato corretto un bug che impediva il salvataggio corretto del &quot;Tag funzione&quot; quando applicato. |
