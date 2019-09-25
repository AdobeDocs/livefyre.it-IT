---
description: Non tutti i tweet che corrispondono a una regola vengono visualizzati in un flusso.
seo-description: Non tutti i tweet che corrispondono a una regola vengono visualizzati in un flusso.
seo-title: Limitazione e frequenza dei tweet
solution: Experience Manager
title: Limitazione e frequenza dei tweet
uuid: b9edfb1e-e6cf-4a48-8756-05f5f18d8799
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Limitazione e frequenza dei tweet{#throttling-and-frequency-of-tweets}

Non tutti i tweet che corrispondono a una regola vengono visualizzati in un flusso.

La limitazione delle regole Twitter e le interruzioni dei feed Twitter possono limitare il numero di tweet visibili nel flusso.

>[!NOTE]
>
>Per garantire l’inclusione di specifici tweet nel flusso, usate l’opzione Carica risorsa dalla pagina Tutte le risorse.

* Regole Twitter riducono il contenuto, richiamando 1 tweet per regola ogni 5 secondi. In questo modo il contenuto visualizzato nelle app Livefyre risulta più bilanciato e non viene sopraffatto dai tweet. Limitare i tweet in entrata in questo modo aiuta anche a evitare che il flusso possa essere inondato o illeggibile durante periodi di traffico elevato.

   >[!NOTE]
   >
   >Per garantire che il contenuto degli autori di alto valore venga visualizzato nelle app, anche nei flussi ad alta velocità, le regole per autori specifici non vengono mai limitate.

* Le interruzioni dei feed Twitter possono verificarsi per diversi motivi. In alcuni casi, Twitter non invia i tweet, pertanto Livefyre non riceve la notifica del nuovo contenuto e non può essere visualizzato. Le interruzioni del servizio delle API di Twitter, o il traffico su hashtag/parole chiave ad alto volume, possono causare la perdita di Tweet.

