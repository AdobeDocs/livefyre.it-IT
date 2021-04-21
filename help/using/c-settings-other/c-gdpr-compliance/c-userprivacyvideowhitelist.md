---
description: Puoi inserire nell’elenco Consentiti il dominio video.
title: userPrivacyVideoWhitelist
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---


# userPrivacyVideoWhitelist{#userprivacyvideowhitelist}

Se utilizzi video e lettori personalizzati come parte dei video visualizzati in un’app di visualizzazione Livefyre, puoi inserire nell’elenco dei domini video consentiti. L’inserimento nell’elenco Consentiti del dominio video rimuove la maschera video per i video e i lettori personalizzati.

>[!NOTE]
>
>Utilizza percorsi specifici per garantire che solo i video sicuri siano inseriti nell’elenco Consentiti. Se inserisci un percorso ampio (ad esempio, sampledomain.com), puoi inserire nell’elenco dei video non sicuri.

* Aggiungi `userPrivacyVideoWhitelist` dopo `userPrivacyOptOut`. È possibile aggiungere tutti i flag per la privacy di Livefyre contemporaneamente come parte di un oggetto Livefyre.
* `userPrivacyVideoWhitelist` si applica solo ai contenuti non incorporati dai social media.

Nell’esempio seguente, i video visualizzati in App con il percorso `sampledomain.com/cdn/videos` sono inseriti nell’elenco Consentiti:

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
