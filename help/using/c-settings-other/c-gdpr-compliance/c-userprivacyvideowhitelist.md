---
description: Puoi inserire in una whitelist il dominio del video utilizzando.
seo-description: Puoi inserire in una whitelist il dominio del video utilizzando.
seo-title: Userprivacyvideowhitelist
solution: Experience Manager
title: Userprivacyvideowhitelist
uuid: adfead 18-b 73 b -4 ac 4-97 a 0-d 39 f 528 b 7606
translation-type: tm+mt
source-git-commit: 097321964ff078bac83c4674100f8c62a8f3a1af

---


# Userprivacyvideowhitelist{#userprivacyvideowhitelist}

Se utilizzate video e lettori personalizzati come parte dei video visualizzati in un&#39;app di visualizzazione Livefyre, potete inserire in una whitelist il vostro dominio video. La whitelist nel dominio video rimuove la maschera video per i video e i lettori personalizzati.

>[!NOTE]
>
>Utilizzate percorsi specifici per garantire che solo i video sicuri siano inseriti nella lista bianca. Se si inserisce un percorso ampio (ad esempio, sampledomain.com), è possibile inserire i video non sicuri.

* Aggiungi `userPrivacyVideoWhitelist` dopo `userPrivacyOptOut`. Potete aggiungere tutti i flag sulla privacy di Livefyre contemporaneamente come parte di un unico oggetto Livefyre.
* `userPrivacyVideoWhitelist` si applica solo al contenuto non incorporato dai social media.

Nell&#39;esempio seguente, i video visualizzati in App con `sampledomain.com/cdn/videos` il percorso vengono inseriti nella lista bianca:

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
