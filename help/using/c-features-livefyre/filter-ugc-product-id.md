---
description: Il filtro di UGC per ID prodotto consente di incorporare la stessa app su più pagine, visualizzando UGC specifico per ogni pagina.
seo-description: Il filtro di UGC per ID prodotto consente di incorporare la stessa app su più pagine, visualizzando UGC specifico per ogni pagina.
seo-title: Filtrare UGC per ID prodotto
title: Filtrare UGC per ID prodotto
uuid: 98108 ddb -5710-4331-891 b -7 e 1 bbb 106059
translation-type: tm+mt
source-git-commit: 76efa427b59a709009a3c2d3744ea65e0c959816

---


# Filtrare UGC per ID prodotto {#filter-ugc-product-id}

Il filtro di UGC per ID prodotto consente di incorporare la stessa app su più pagine, visualizzando UGC specifico per ogni pagina.

Per filtrare UGC per ID prodotto, effettuate le seguenti operazioni:

1. In Livefyre Studio, passate alla **[!UICONTROL Apps]** scheda.

1. Selezionate l&#39;app da modificare.

1. Selezionare la scheda Designer nella barra a sinistra.

1. Abilita **[!UICONTROL Filter UGC by Product ID]**.

![](assets/filter-ugc-product-id.png)

1. Selezionate le cartelle di prodotto di livello principale contenenti il prodotto o i prodotti di cui desiderate filtrare UGC.
Usate CTRL/Comando + clic per selezionare più cartelle.

1. Disattiva **[!UICONTROL Show related content]**.
Quando abilitato, il contenuto filtrato utilizzando l&#39; `data-lf-attr-product` attributo verrà visualizzato per primo, seguita da tutti gli altri contenuti dell&#39;app.

1. Fate clic **[!UICONTROL Publish]** su.

1. Inserite gli ID prodotto che desiderate filtrare nel codice risultante.

>[!NOTE]
>
>Per individuare gli ID prodotto, andate alla **[!UICONTROL Settings > Products]** pagina. Individua il prodotto desiderato e selezionalo e l&#39;ID viene visualizzato.

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

Per assegnare tag a un prodotto, sostituitelo `<product 1>` nell `data-lf-attr-product` &#39;attributo con l&#39;ID prodotto desiderato. Potete assegnare un tag a un prodotto o più semplicemente aggiungendo altri ID prodotto separati da virgola. I prodotti devono essere contenuti nella cartella di prodotto o cartelle di livello principale selezionate al Passaggio 5.

Il segmento di codice modificato viene visualizzato come:

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

L&#39;app ora visualizza solo gli ID prodotto con tag.