---
description: Potete inserire in una whitelist il dominio del video utilizzando .
seo-description: Potete inserire in una whitelist il dominio del video utilizzando .
seo-title: userPrivacyVideoWhitelist
solution: Experience Manager
title: userPrivacyVideoWhitelist
uuid: adfead18-b73b-4ac4-97a0-d39f528b7606
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# userPrivacyVideoWhitelist{#userprivacyvideowhitelist}

Se utilizzate video e lettori personalizzati come parte dei video visualizzati in un’app di visualizzazione Livefyre, potete inserire il dominio del video nella whitelist. Quando si inserisce un dominio video, la maschera video viene rimossa per i video e i lettori personalizzati.

>[!NOTE]
>
>Usate percorsi specifici per garantire che vengano inseriti nella white list solo i video sicuri. Se inserite un percorso ampio (ad esempio, sampledomain.com), potete inserire in una whitelist i video non sicuri.

* Aggiungi `userPrivacyVideoWhitelist` dopo `userPrivacyOptOut`. Potete aggiungere tutti i flag di privacy di Livefyre contemporaneamente come parte di un oggetto Livefyre.
* `userPrivacyVideoWhitelist` si applica solo ai contenuti non incorporati dai social media.

Nell'esempio seguente, i video visualizzati in App con il `sampledomain.com/cdn/videos` percorso vengono inseriti nella white list:

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
