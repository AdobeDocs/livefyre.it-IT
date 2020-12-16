---
description: Note sulla versione per la versione del 30 marzo 2017.
seo-description: Note sulla versione per la versione del 30 marzo 2017.
seo-title: 30 marzo 2017
title: 30 marzo 2017
uuid: 2adf04a9-6c52-4fa1-a0c9-b2d3886305e9
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 6%

---


# 30 marzo 2017{#march}

Note sulla versione per la versione del 30 marzo 2017.

## Release produzione

| Tipo problema | Componente | Note sulla versione |
|---|---|---|
| Bug | Ricerca social | È stato corretto un bug che impediva la pubblicazione di risorse salvate su YouTube in Social Search. |
| Miglioramento | Social Sync | Sincronizzazione social Twitter obsoleta. |
| Miglioramento | Storify 2 | È stato aggiunto un miglioramento per visualizzare il messaggio &quot;Nessun risultato trovato&quot; nella ricerca dell&#39;argomento Facebook quando non viene trovato alcun risultato. |
| Miglioramento | Streams | Sono state aggiunte le regole di riepilogo per le regole SAFE nella parte inferiore di una pagina di flusso Twitter. |
| Bug | Streams | È stato aggiunto un miglioramento per disattivare visibilmente la casella di controllo &quot;Utente verificato&quot; nelle regole di flusso Twitter quando vengono forniti autori esclusi. |
| Bug | Streams | È stato corretto un bug per consentire l&#39;uso di parole chiave AND e un filtro Posizione in una regola Twitter. |
| Bug | Studio | È stato corretto un bug che impediva il salvataggio corretto di &quot;Feature Tag&quot; quando veniva applicato. |

## Rilascio UAT

| Tipo problema | Componente | Note sulla versione |
|---|---|---|
| Bug | Contenuto app | È stato modificato il comportamento di &quot;Ulteriori informazioni&quot; in modo che, in presenza di più eventi di flag anonimi su un dato contenuto, venga sempre visualizzato il primo evento. |
| Bug | Libreria | È stato corretto un bug a causa del quale le ricerche nella libreria con hashtag non riuscivano in modo intermittente. |
| Bug | Mappe | È stato corretto un bug in Mappe per supportare un gran numero di contenuti nei cluster sui dispositivi iOS. |
| Miglioramento | Mosaico | È stata aggiunta la possibilità di configurare le app Mosaic in modo da fare clic ovunque su una scheda di contenuto per aprire il modale in base al tipo di animazione `none` in Designer e `cardAnimation: 'off'`se creata tramite l&#39;SDK. |
| Bug | Mosaico | È stato corretto un bug per consentire agli utenti di apportare modifiche alle app Mosaic in Designer. |
| Miglioramento | Richiesta diritti | È stato aggiunto un nuovo stato di richiesta di diritti denominato &quot;Richiesta non riuscita&quot; per evidenziare quando i messaggi di richiesta di diritti non vengono inviati. |
| Miglioramento | Impostazioni | Aggiunta la possibilità per i clienti di creare regole per la moderazione dello spam in Impostazioni. |
| Miglioramento | Ricerca social | È stato corretto un bug che impediva la visualizzazione dei post VK.com tramite URL Social Searches. |
| Miglioramento | Ricerca social | Durante la ricerca di contenuto Instagram da Studio, se la ricerca è dovuta a un token API Instagram scaduto, il messaggio di errore ora verrà indicato come tale. |
| Bug | Streams | È stato corretto un bug a causa del quale un banner &quot;App non accetta nuovo contenuto&quot; veniva visualizzato erroneamente sulle pagine Regola di flusso. |
| Miglioramento | Streams | Modificato il valore predefinito delle nuove regole di flusso create per applicare le regole di sicurezza quando applicabile. |
| Miglioramento | Streams (precedentemente, Curate Rules) | È stata rimossa l&#39;opzione &quot;Vine&quot; solo dalle regole Flusso/Cura di Twitter, poiché Vines ora vengono visualizzati come video Twitter. |
| Bug | Studio Shell | È stato corretto un bug a causa del quale Livefyre Studio si caricava se https:// veniva esplicitamente precompilato all’URL. |

