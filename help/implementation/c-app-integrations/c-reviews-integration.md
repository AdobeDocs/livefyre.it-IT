---
description: Consente ai clienti di valutare e rivedere le offerte di prodotti.
seo-description: Consente ai clienti di valutare e rivedere le offerte di prodotti.
seo-title: Recensioni
solution: Experience Manager
title: Recensioni
uuid: b740ee28-f6f9-4ae7-9fe7-61a5cde97bbb
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934
workflow-type: tm+mt
source-wordcount: '692'
ht-degree: 0%

---


# Recensioni {#reviews}

Consente ai clienti di valutare e rivedere le offerte di prodotti.

Le recensioni consentono ai membri della tua community di contribuire con valutazioni a stella e valutazioni qualitative per qualsiasi prodotto o servizio.

## Integrazione {#section_kk5_15b_c1b}

Per integrare un&#39;app di revisione, seguite la procedura per l&#39;integrazione di un&#39;app di conversazione. Consultate [Incorporare un&#39;app](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md). Di seguito è riportato un esempio di app di revisione incorporate.

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

Come indicato nella sezione Building `CollectionMeta`, `CollectionMeta` è un oggetto JSON codificato. Nell&#39;esempio precedente, l&#39;oggetto JSON ha il formato seguente prima che sia codificato JWT:

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

Se hai già completato la sezione Guida introduttiva, devi avere familiarità con l’oggetto convConfig. Per abilitare Revisioni, aggiorna convConfig con i campi seguenti:

* **** ** alwaysShowEditoroptionalboolean: Per impostazione predefinita, l&#39;editor delle revisioni viene visualizzato solo dopo che l&#39;utente ha premuto il pulsante &quot;revisione scrittura&quot;. Impostate questo parametro su true per visualizzare sempre l&#39;editor.

* **** ** apprquiredstring: Nome app da utilizzare per le revisioni. Deve essere &quot;recensioni&quot;.

* **** ** defaultSortoptionalstring: Consente di selezionare l&#39;opzione di ordinamento predefinita per Recensioni. I valori possibili sono: mostHelpful, mostRated, lowerRated, newest e old.

* **** ** disableTitleoptionalboolean: Disattiva e nasconde il campo titolo nell’editor delle revisioni, che per impostazione predefinita è obbligatorio e visibile. Il valore predefinito è true.

* **** ** enableHalfRatingoptionalboolean: Utilizzato per abilitare metà delle valutazioni nel modulo di selezione a stella predefinito. Il valore predefinito è true.

* **** ** hideShowReviewButtonoptionalboolean: Controlla se il  [!UICONTROL Show My Review] pulsante verrà visualizzato o meno. Impostate questa opzione su true per consentire agli utenti di scegliere se mostrare o visualizzare le proprie revisioni.

* **** ** maxRatingoptionalinteger Utilizzato per impostare il numero di stelle visualizzate nel modulo di selezione a stella predefinito. Il valore predefinito è 5. Può essere configurato fino a 100.

* **** ** ratingSummaryEnabledoptionalboolean: Utilizzato per mostrare la vista di riepilogo delle valutazioni sopra l&#39;app di revisione. Deve essere attivato per utilizzare la classe ratingSummaryDelegate. Il valore predefinito è true.

## Rivedi metadati raccolta {#section_k1s_sqb_c1b}

* **type:** ** requiredstring: Definisce il tipo di raccolta. Deve essere `reviews`.

* **** ** ratingDimensionsoptionalarray: Un array di stringhe per ciascun tipo di dimensione che verrà utilizzato da questa raccolta. Se non viene specificato, sarà consentita solo una dimensione.

   Ad esempio, per consentire agli utenti di valutare il prodotto in base a &quot;progettazione&quot;, &quot;caratteristiche&quot; e &quot;prestazioni&quot;, impostare l&#39;array su: `ratingDimensions: [‘design’, ‘features’, ‘performance’]`

* **** ** ratingSubpartsoptionalinteger: Numero di partizioni da visualizzare nella casella di testo della revisione. Le etichette dei sottomoduli vengono trasmesse con il parametro come illustrato di seguito.

   >[!NOTE]
   >È necessario definire etichette per ogni sottoparte.

* **** ** ratingSubpartArgomento facoltativo: Consente di definire un ID per ogni sottoparte della raccolta Valutazioni, che può essere utilizzata per eseguire il targeting di questi elementi di sottoparte nel CSS e in JavaScript. Quando gli utenti pubblicano le revisioni, ogni `ratingSubpart` avrà l&#39;attributo &quot;`data-lf-subpart-id`&quot; inserito con questo ID.

>[!NOTE]
>
>Per utilizzare `ratingSubpartsIds`, è necessario definire anche il parametro `ratingSubparts` e la lunghezza delle due matrici deve corrispondere.

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
>Se si utilizza `ratingDimensions`, è NECESSARIO utilizzare `ratingSelectionDelegate`, `ratingDisplayDelegate` e `ratingSummaryDelegate` (se si desidera visualizzare il riepilogo delle valutazioni).

## Revisioni Personalizzazione {#section_khz_xmb_c1b}

### Configura immagini stella

Per modificare l&#39;immagine per le stelle intere, la classe è `goog-ratings-star`. Modificate l’immagine di sfondo impostandola come desiderate. Per impostazione predefinita, le stelle sono 28 x 28 pixel.

### Configurare le immagini con stella con le stelle

Con mezza stella, ci sono due classi, una per ogni lato della stella. Il lato sinistro della mezza stella è `fyre-rating-half-odd` e il lato destro è `fyre-rating-half-even`. Per impostazione predefinita, le mezza stella sono 28 x 14 pixel.

### Configurare i valori delle descrizioni comandi per le stelle

Per configurare i valori delle descrizioni comandi per le stelle, seguite il testo personalizzato descritto in Personalizzazioni stringa. Una volta impostata, utilizzare la chiave `ratingValues` e il valore di un array che contiene le stringhe delle descrizioni comandi. Se la metà delle stelle è disattivata, il numero di elementi nell&#39;array deve essere uguale a `maxRating` (sopra). Se la metà delle stelle è attivata, il numero di elementi deve essere 2x `maxRating`. Il primo elemento dell&#39;array corrisponde all&#39;elemento a stella (o a mezza stella) più a sinistra e continua da sinistra a destra.

### Attiva/disattiva l&#39;opzione &quot;Mostra revisione personale&quot;

Per attivare o disattivare l&#39;opzione [!UICONTROL Show My Review], eseguite il targeting del parametro `hideShowReviewButton` nella configurazione dell&#39;app.

### Mostra editor di testo per impostazione predefinita

L&#39;editor delle recensioni viene visualizzato solo dopo che l&#39;utente ha premuto il pulsante [!UICONTROL write review]. Per visualizzare questo modulo per impostazione predefinita, eseguite il targeting del parametro `alwaysShowEditor` nella configurazione dell&#39;app.
