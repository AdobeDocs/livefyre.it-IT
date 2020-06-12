---
description: Potete consentire l’elenco del dominio video.
seo-description: Potete consentire l’elenco del dominio video.
seo-title: userPrivacyVideoWhitelist
solution: Experience Manager
title: userPrivacyVideoWhitelist
uuid: adfead18-b73b-4ac4-97a0-d39f528b7606
translation-type: tm+mt
source-git-commit: 52f59cd15f315aa93be198f6eb586f008c18a384
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# userPrivacyVideoWhitelist{#userprivacyvideowhitelist}

Se utilizzate video e lettori personalizzati come parte dei video visualizzati in un’app di visualizzazione Livefyre, potete consentire l’elenco del dominio del video. L’elenco dei domini video consente di rimuovere la maschera video per i video e i lettori personalizzati.

>[!NOTE]
>
>Utilizzate percorsi specifici per garantire che siano elencati solo i video sicuri. Se inserite un percorso ampio (ad esempio, sampledomain.com), potete consentire l’utilizzo di elenchi non sicuri per i video.

* Aggiungi `userPrivacyVideoWhitelist` dopo `userPrivacyOptOut`. Potete aggiungere tutti i flag di privacy di Livefyre contemporaneamente come parte di un oggetto Livefyre.
* `userPrivacyVideoWhitelist` si applica solo ai contenuti non incorporati dai social media.

Nell&#39;esempio seguente, i video visualizzati in App con il `sampledomain.com/cdn/videos` percorso sono inclusi nell&#39;elenco:

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
