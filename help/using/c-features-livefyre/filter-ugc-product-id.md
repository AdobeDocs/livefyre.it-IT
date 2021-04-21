---
description: Il filtro UGC per ID prodotto consente di incorporare la stessa app esattamente su più pagine e allo stesso tempo di mostrare diversi UGC per ogni pagina specifici del prodotto.
title: Filtra UGC per ID prodotto
exl-id: c98ee899-fcac-45dd-a26a-f678814776fd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Filtra UGC per ID prodotto {#filter-ugc-product-id}

Il filtro UGC per ID prodotto consente di incorporare la stessa app esattamente su più pagine e allo stesso tempo di mostrare diversi UGC per ogni pagina specifici del prodotto.

Per filtrare gli UGC per ID prodotto, procedi come segue:

1. In Livefyre Studio, passa alla scheda **[!UICONTROL Apps]** .

1. Seleziona l’app da modificare.

1. Selezionare la scheda Designer nella barra a sinistra.

1. Abilita **[!UICONTROL Filter UGC by Product ID]**.

![](assets/filter-ugc-product-id.png)

1. Seleziona le cartelle di prodotti di primo livello che contengono il prodotto o i prodotti per i quali desideri filtrare gli UGC.
Utilizza CTRL/Comando + clic per selezionare più cartelle.

1. Disattiva **[!UICONTROL Show related content]**.
Quando abilitato, il contenuto filtrato utilizzando l’attributo `data-lf-attr-product` viene visualizzato per primo, seguito da tutti gli altri contenuti dell’app.

1. Clic **[!UICONTROL Publish]**.

1. Inserisci gli ID prodotto per i quali desideri filtrare nel codice risultante.

>[!NOTE]
>
>Per individuare gli ID prodotto, passa a **[!UICONTROL Settings > Products]**. Individua il prodotto desiderato, selezionalo e visualizzato l’ID.

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

Per assegnare tag a un prodotto, sostituisci `<product 1>` nell’attributo `data-lf-attr-product` con l’ID prodotto desiderato. Puoi assegnare tag a uno o più prodotti aggiungendo ID prodotto aggiuntivi separati da virgole. I prodotti devono essere contenuti nella cartella o nelle cartelle di prodotto di primo livello selezionate al passaggio 5.

Il segmento di codice modificato apparirà come:

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

L’app ora visualizza solo gli ID prodotto con tag.
