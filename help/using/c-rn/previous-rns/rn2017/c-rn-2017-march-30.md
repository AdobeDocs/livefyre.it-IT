---
description: Note sulla versione del 30 marzo 2017.
title: 30 marzo 2017
exl-id: 44c73ff9-8bc1-49c9-b720-aff425e5cd28
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 5%

---

# 30 marzo 2017{#march}

Note sulla versione del 30 marzo 2017.

## Versione di produzione

| Tipo di problema | Componente | Note sulla versione |
|---|---|---|
| Bug | Ricerca social | È stato corretto un bug che impediva la pubblicazione di risorse Youtube salvate in Social Search. |
| Miglioramento | Sincronizzazione social | Sincronizzazione social di Twitter obsoleta. |
| Miglioramento | Memorizza 2 | È stato aggiunto un miglioramento per visualizzare il messaggio &quot;Nessun risultato trovato&quot; nella ricerca argomento Facebook quando non vengono trovati risultati. |
| Miglioramento | Flussi | Sono state aggiunte delle regole di riepilogo per le regole SAFE nella parte inferiore di una pagina Twitter Stream. |
| Bug | Flussi | È stato aggiunto un miglioramento per disabilitare visibilmente la casella di controllo &quot;Utente verificato&quot; nelle regole di flusso di Twitter quando vengono forniti gli autori esclusi. |
| Bug | Flussi | È stato corretto un bug per consentire l’utilizzo di parole chiave ANDing e di un filtro Posizione in una regola Twitter. |
| Bug | Studio | È stato corretto un bug che impediva il salvataggio corretto del &quot;Tag funzione&quot; quando applicato. |

## Versione UAT

| Tipo di problema | Componente | Note sulla versione |
|---|---|---|
| Bug | Contenuto app | È stato modificato il comportamento di &quot;Ulteriori informazioni&quot; in modo che, se ci sono più eventi di flag Anonymous su un dato contenuto, venga sempre visualizzato il primo evento. |
| Bug | Libreria | È stato corretto un bug a causa del quale le ricerche nella libreria con hashtag non riuscivano a intermittenza. |
| Bug | Mappe | È stato corretto un bug in Mappe per supportare un gran numero di contenuti nei cluster su dispositivi iOS. |
| Miglioramento | Mosaico | Aggiunta la possibilità di configurare le app Mosaic per fare clic in un punto qualsiasi di una scheda di contenuto per aprire il modale in base al tipo di animazione `none` in designer e `cardAnimation: 'off'`se viene creata un&#39;istanza tramite l&#39;SDK. |
| Bug | Mosaico | È stato corretto un bug per consentire agli utenti di apportare modifiche alle app Mosaic in Designer. |
| Miglioramento | Richiesta di diritti | È stato aggiunto il nuovo stato di richiesta di diritti denominato &quot;Richiesta non riuscita&quot; per evidenziare quando i messaggi di richiesta di diritti non vengono inviati. |
| Miglioramento | Impostazioni | Aggiunta la possibilità per i clienti di creare regole di moderazione dello spam in Impostazioni. |
| Miglioramento | Ricerca social | È stato corretto un bug che impediva la visualizzazione dei post VK.com tramite URL Social Searches (Ricerche social URL). |
| Miglioramento | Ricerca social | Durante la ricerca di contenuti Instagram da Studio, se la ricerca è dovuta a un token API Instagram scaduto, il messaggio di errore ora indica come tale. |
| Bug | Flussi | È stato corretto un bug a causa del quale il banner &quot;L’app non accetta nuovi contenuti&quot; veniva visualizzato erroneamente sopra le pagine delle regole di flusso. |
| Miglioramento | Flussi | È stato modificato il valore predefinito delle nuove regole di flusso create per applicare le regole SAFE, se applicabile. |
| Miglioramento | Streams (precedentemente denominato Regole di cura) | È stata rimossa l’opzione &quot;Vines&quot; only (Solo vite) dalle regole Streaming/Cura di Twitter, in quanto ora Vines viene visualizzato come video Twitter. |
| Bug | Shell di Studio | È stato corretto un bug a causa del quale Livefyre Studio veniva caricato se https:// era stato esplicitamente aggiunto all’URL. |
