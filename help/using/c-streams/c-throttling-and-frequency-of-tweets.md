---
description: Non tutti i tweet che corrispondono a una regola vengono visualizzati in un flusso.
title: Limitazione e frequenza dei tweet
exl-id: 6b963f8a-1b61-4252-866b-567d7f556aca
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# Limitazione e frequenza dei tweet{#throttling-and-frequency-of-tweets}

Non tutti i tweet che corrispondono a una regola vengono visualizzati in un flusso.

La limitazione delle regole di twitter e le interruzioni dei feed Twitter possono limitare il numero di tweet visibili nel flusso.

>[!NOTE]
>
>Per garantire che nel flusso siano inclusi tweet specifici, utilizza l’opzione Carica risorsa dalla pagina Tutte le risorse .

* Le regole di twitter riducono il contenuto, richiamando 1 tweet per regola ogni 5 secondi. Questo consente di ottenere contenuti più bilanciati nelle app Livefyre e non essere sopraffatti dai tweet. Limitare i tweet in arrivo in questo modo aiuta anche a evitare che il flusso diventi invariato o illeggibile durante periodi di traffico elevato.

   >[!NOTE]
   >
   >Per garantire che il contenuto degli autori di alto valore sia visualizzato nelle app, anche nei flussi ad alta velocità, le regole per autori specifici non vengono mai limitate.

* Le interruzioni dei feed twitter possono verificarsi per diversi motivi. In alcuni casi, Twitter non invia i tweet, quindi Livefyre non riceve la notifica del nuovo contenuto e non può essere visualizzato. Le interruzioni del servizio delle API di Twitter, o il traffico su hashtag/parole chiave ad alto volume, possono causare la perdita di Tweet.
