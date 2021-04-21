---
description: Consenti ai clienti di valutare e rivedere le offerte di prodotti.
title: Recensioni
exl-id: 2f10646e-59c4-459c-ae1b-749f951a06d2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# Recensioni {#reviews}

Consenti ai clienti di valutare e rivedere le offerte di prodotti.

Revisioni consente ai membri della tua comunità di contribuire stelle valutazioni e valutazioni qualitative per qualsiasi prodotto o servizio.

## Integrazione {#section_kk5_15b_c1b}

Per integrare un’app di revisione, segui la procedura per l’integrazione di un’app di conversazione . Consulta [Incorporare un&#39;app](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md). Di seguito è riportato un esempio di app di revisione incorporate.

### Esempio 

```
var networkConfig = { 
   network: "client-solutions-uat.fyre.co" 
}; 
  
var convConfig = { 
   siteId: '304059', 
   articleId: 'sh_col_22_1373478370_reviews', 
   el: 'livefyre-comments', 
   app: 'reviews', 
   ratingSummaryEnabled: true, 
   maxRating: 5, 
   collectionMeta: 'eyJhbGciOiAiSFMyNTYiLCAidHlwIjogIkpXVCJ9.eyJ1cmwiOiAiaHR0cDovL3d3dy5kaXJlY3R2LmNvbS9wZXJzb24vQW5uYS1QYXF1aW4tYjJGU0wwZHJLM051YldjOS1yZXZpZXdzIiwgInNpdGVJZCI6ICIzMDQwNTkiLCAiYXJ0aWNsZUlkIjogInNoX2NvbF8yMl8xMzczNDc4MzcwX3Jldmlld3MiLCAidHlwZSI6ICJyZXZpZXdzIiwgInRpdGxlIjogIlRCX1BhcXVpbl9yYXRpbmdzX3Jldmlld3MifQ.hes3KMwygCG-fFDQlkaB-XlxGjW6-iZ68xA4RRGqUl0' 
}; 
  
Livefyre.require(['fyre.conv#3'], function (Review) { 
   new Review(networkConfig, [convConfig], function (reviewWidget) {}); 
   auth.delegate({ 
      login: function (callback) { 
         callback(null,{livefyre:'<userauthtoken>'}); 
      }, 
   }); 
});
```

Come indicato nella sezione Generazione `CollectionMeta` , `CollectionMeta` è un oggetto JSON codificato. Nell’esempio precedente, l’oggetto JSON assume il formato seguente prima della codifica JWT:

```
{ 
"url": "https://www.directv.com/person/Anna-Paquin-b2FSL0drK3NubWc9-reviews",  
"siteId": "304059",  
"articleId": "sh_col_22_1373478370_reviews",  
"type": "reviews",  
"title": "TB_Paquin_ratings_reviews" 
}
```

## oggetto convConfig {#section_pzv_ytb_c1b}

Se hai già completato la sezione Introduzione, devi avere familiarità con l’oggetto convConfig. Per abilitare le revisioni, aggiorna la configurazione convConfig con i campi seguenti:

* **** ** alwaysShowEditoroptionalboolean: Per impostazione predefinita, l&#39;editor delle revisioni viene visualizzato solo dopo che l&#39;utente ha premuto il pulsante &quot;write review&quot;. Imposta questo parametro su true per visualizzare sempre l&#39;editor.

* **** ** apprquiredstring: Nome app da utilizzare per le revisioni. Devono essere &quot;recensioni&quot;.

* **** ** defaultSortoptionalstring: Consente di selezionare l&#39;opzione di ordinamento predefinita per Revisioni. I valori possibili sono: mostHelpful, più altaRated, più bassaRated, più recente e più vecchia.

* **** ** disableTitleoptionalboolean: Disattiva e nasconde il campo titolo nell&#39;editor delle revisioni, obbligatorio e visibile per impostazione predefinita. Il valore predefinito è true.

* **** ** enableHalfRatingoptionalboolean: Utilizzato per abilitare metà delle valutazioni nel modulo di selezione a stella predefinito. Il valore predefinito è true.

* **** ** hideShowReviewButtonoptionalboolean: Controlla se verrà visualizzato il  [!UICONTROL Show My Review] pulsante. Imposta su true per consentire agli utenti di selezionare se mostrare o visualizzare le proprie revisioni.

* **** ** maxRatingoptionalinteger Utilizzato per impostare il numero di stelle visualizzate nel modulo di selezione della stella predefinito. Il valore predefinito è 5. Può essere configurato fino a 100.

* **** ** ratingSummaryEnabledoptionalboolean: Utilizzato per mostrare la vista di riepilogo delle valutazioni sopra l&#39;app Reviews. Deve essere abilitato per utilizzare la classe ratingSummaryDelegate. Il valore predefinito è true.

## Verifica metadati raccolta {#section_k1s_sqb_c1b}

* **type:** ** requiredstring: Definisce il tipo di raccolta. Deve essere `reviews`.

* **** ** ratingDimensionsoptionalarray: Matrice di stringhe per ogni tipo di dimensione che verrà utilizzata dalla raccolta. Se non viene specificato, sarà consentita solo una dimensione.

   Ad esempio, per consentire agli utenti di valutare il prodotto in base a &quot;progettazione&quot;, &quot;caratteristiche&quot; e &quot;prestazioni&quot;, impostare l&#39;array su: `ratingDimensions: [‘design’, ‘features’, ‘performance’]`

* **** ** ratingSubpartsoptionalinteger: Numero di partizioni da visualizzare nella casella di testo della revisione. Le etichette della parte secondaria vengono trasmesse con il parametro come illustrato di seguito.

   >[!NOTE]
   >È necessario definire le etichette per ogni sottoparte.

* **** ** ratingSubpartsIdsoptionalarray: Consente di definire un ID per ogni sottoparte della raccolta Valutazioni, che può essere utilizzato per eseguire il targeting di questi elementi secondari nei CSS e JavaScript. Quando gli utenti pubblicano le revisioni, ogni `ratingSubpart` avrà l&#39;attributo &quot;`data-lf-subpart-id`&quot; su di esso, compilato con questo ID.

>[!NOTE]
>
>Per utilizzare `ratingSubpartsIds`, è necessario definire anche il parametro `ratingSubparts` e la lunghezza dei due array deve corrispondere.

```
networkConfig["strings"] = { 
   ratingSubpartPlaceholders: ['Pros...', 'Cons...'], 
   ratingSubpartTitles: ['Pros:', 'Cons:'], 
   ratingSubpartIds: ['pros', 'cons'], 
   reviewStreamTitle: 'Description:' 
} 
fyre.conv.load(networkConfig, [{ 
   app: 'reviews', 
   ratingSubparts: 2, 
    ... // More conv config settings 
}]);
```

>[!NOTE]
>
>Se utilizzi `ratingDimensions`, devi utilizzare i valori `ratingSelectionDelegate`, `ratingDisplayDelegate` e `ratingSummaryDelegate` (se desideri visualizzare il riepilogo delle valutazioni).

## Revisioni Personalizzazione {#section_khz_xmb_c1b}

### Configurare le immagini a stella

Per modificare l’immagine per le stelle intere, la classe è `goog-ratings-star`. Cambia l’immagine di sfondo in qualsiasi immagine desideri. Per impostazione predefinita, le stelle sono 28 x 28 pixel.

### Configurare le immagini a stella con Mezza stella

Con mezza stella ci sono due classi, una per ogni lato della stella. Il lato sinistro della mezza stella è `fyre-rating-half-odd` e il lato destro è `fyre-rating-half-even`. Per impostazione predefinita, metà stelle sono 28 x 14 pixel.

### Configura i valori della descrizione comando per le stelle

Per configurare i valori della descrizione comando per le stelle, segui il testo personalizzato descritto in Personalizzazione stringhe. Una volta configurata, utilizza la chiave `ratingValues` e il valore di una matrice che contiene le stringhe della descrizione comando. Se la metà delle stelle è disattivata, il numero di elementi nella matrice deve essere lo stesso di `maxRating` (sopra). Se la metà delle stelle è abilitata, il numero di elementi deve essere 2x `maxRating`. Il primo elemento dell’array corrisponde all’elemento a stella (o a mezza stella) più a sinistra e continua da sinistra a destra.

### Attiva/disattiva l&#39;opzione &quot;Mostra revisione personale&quot;

Per attivare o disattivare l&#39;opzione [!UICONTROL Show My Review] , esegui il targeting del parametro `hideShowReviewButton` nella configurazione dell&#39;app.

### Mostra l’Editor di testo per impostazione predefinita

L&#39;editor delle recensioni viene visualizzato solo dopo che l&#39;utente ha premuto il pulsante [!UICONTROL write review] . Per visualizzare questo modulo per impostazione predefinita, esegui il targeting del parametro `alwaysShowEditor` nella configurazione dell’app.
