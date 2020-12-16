---
description: Il filtro UGC per ID prodotto consente di incorporare la stessa app esattamente su più pagine, mostrando allo stesso tempo UGC per ogni pagina.
seo-description: Il filtro UGC per ID prodotto consente di incorporare la stessa app esattamente su più pagine, mostrando allo stesso tempo UGC per ogni pagina.
seo-title: Filtra UGC per ID prodotto
title: Filtra UGC per ID prodotto
uuid: 98108ddb-5710-4331-891b-7e1bbb106059
translation-type: tm+mt
source-git-commit: 76efa427b59a709009a3c2d3744ea65e0c959816
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---


# Filtra UGC per ID prodotto {#filter-ugc-product-id}

Il filtro UGC per ID prodotto consente di incorporare la stessa app esattamente su più pagine, mostrando allo stesso tempo UGC per ogni pagina.

Per filtrare gli UGC per ID prodotto, attenetevi alla seguente procedura:

1. In Livefyre Studio, andate alla scheda **[!UICONTROL Apps]**.

1. Selezionate l&#39;app da modificare.

1. Selezionare la scheda Designer nella barra a sinistra.

1. Abilita **[!UICONTROL Filter UGC by Product ID]**.

![](assets/filter-ugc-product-id.png)

1. Selezionate le cartelle di prodotti di livello principale che contengono il prodotto o i prodotti per i quali desiderate filtrare l’utilizzo di UGC.
Per selezionare più cartelle, usate Ctrl/Comando + clic.

1. Disattivate **[!UICONTROL Show related content]**.
Quando abilitata, viene visualizzato per primo il contenuto filtrato utilizzando l&#39;attributo `data-lf-attr-product`, seguito da tutti gli altri contenuti nell&#39;app.

1. Clic **[!UICONTROL Publish]**.

1. Inserite gli ID prodotto da filtrare nel codice risultante.

>[!NOTE]
>
>Per individuare gli ID prodotto, andate a **[!UICONTROL Settings > Products]**. Individuate il prodotto desiderato e selezionatelo e viene visualizzato l’ID.

Ad esempio, per un&#39;app Media Wall viene generato il seguente codice:

```
<script type="text/javascript" src="https://cdn.livefyre.com/
Livefyre.js"></script><div class="lf-app-embed" data-lfapp="
59dc41fa-85a5-49ed-8d60-d74616b3ccd1/tagged/published" datalf-
env="prod" data-lf-read-only="" data-lf-attr-product="<product
 1>,<product 2>"></div><script>Livefyre.require(["app-embed#1.0.11"],
 function (appEmbed) {appEmbed.loadAll().done(function(embed)
 {embed = embed[0];if (embed.el.onload && embed.getConfig)
 {embed.el.onload(embed.getConfig());}});});</script>
```

Per assegnare un tag a un prodotto, sostituite `<product 1>` nell&#39;attributo `data-lf-attr-product` con l&#39;ID prodotto desiderato. Potete assegnare tag a uno o più prodotti aggiungendo ID prodotto separati da virgola aggiuntivi. I prodotti devono essere contenuti nella cartella o nelle cartelle di livello superiore selezionate al punto 5.

Il segmento di codice modificato viene visualizzato come segue:

```
<script type="text/javascript" src="https://cdn.livefyre.com/
Livefyre.js"></script><div class="lf-app-embed" data-lfapp="
59dc41fa-85a5-49ed-8d60-d74616b3ccd1/tagged/published"
 data-lf-env="prod" data-lf-read-only="" data-lf-attrproduct="
109,47"></div><script>Livefyre.require(["app-embed#1.0.11"],
 function (appEmbed) {appEmbed.loadAll().done(function(embed)
 {embed = embed[0];if (embed.el.onload && embed.getConfig)
 {embed.el.onload(embed.getConfig());}});});</script>
```

L&#39;app ora visualizzerà solo gli ID prodotto con tag.