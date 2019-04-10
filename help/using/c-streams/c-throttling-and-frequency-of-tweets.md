---
description: Non tutti i tweet che corrispondono a una regola vengono visualizzati
  in un flusso.
seo-description: Non tutti i tweet che corrispondono a una regola vengono visualizzati
  in un flusso.
seo-title: Caratteristiche e frequenza dei tweet
solution: Experience Manager
title: Caratteristiche e frequenza dei tweet
uuid: b 9 edfb 1 e-e 6 cf -4 a 48-8756-05 f 5 f 18 d 8799
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Caratteristiche e frequenza dei tweet{#throttling-and-frequency-of-tweets}

Non tutti i tweet che corrispondono a una regola vengono visualizzati in un flusso.

L'interpolazione della regola Twitter e le interruzioni di feed Twitter possono limitare il numero di tweet visibili nel flusso.

>[!NOTE]
>
>Per verificare che i tweet specifici siano inclusi nel flusso, utilizzate l'opzione Carica risorsa dalla pagina Tutte le risorse.

* Regole Twitter rallentano il contenuto, richiamando 1 tweet per regola ogni 5 secondi. Questo consente di visualizzare in modo più bilanciato il contenuto in Livefyre Apps e non viene sostituito con tweet. La limitazione dei tweet in arrivo consente anche di impedire che il flusso diventi inaccessibile o non leggibile durante un periodo di traffico elevato.

   >[!NOTE]
   >
   >Per garantire che il contenuto degli autori di alto valore venga visualizzato nelle app, anche nei flussi ad alta velocità, le regole per gli autori specifici non vengono mai rallentate.

* Le interruzioni dei feed Twitter possono verificarsi per diversi motivi. In alcuni casi, Twitter non invia i tweet, pertanto Livefyre non riceve la notifica del nuovo contenuto e non può essere visualizzato. Le interruzioni del servizio delle API di Twitter, o il traffico su hashtag/parole chiave ad alto volume, possono anche dare luogo a tweet mancanti.

