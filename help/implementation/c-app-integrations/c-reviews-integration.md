---
description: Consentite ai clienti di valutare e rivedere le offerte dei prodotti.
seo-description: Consentite ai clienti di valutare e rivedere le offerte dei prodotti.
seo-title: Recensioni
solution: Experience Manager
title: Recensioni
uuid: b 740 ee 28-f 6 f 9-4 ae 7-9 fe 7-61 a 5 cde 97 bbb
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934

---


# Recensioni {#reviews}

Consentite ai clienti di valutare e rivedere le offerte dei prodotti.

Le revisioni consentono ai membri della community di fornire valutazioni a stelle e recensioni qualitative per qualsiasi prodotto o servizio.

## Integrazione {#section_kk5_15b_c1b}

Per integrare un'app reviews, segui la procedura per Integrazione di un'app di conversazione. Consultate [Incorporare un'app](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md). Esempio di un'app recensioni incorporata.

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

Come indicato nella `CollectionMeta` sezione Creazione, `CollectionMeta` è un oggetto JSON codificato. Nell'esempio precedente, l'oggetto JSON prende il seguente formato prima che sia codificato in JWT:

```
{ 
"url": "https://www.directv.com/person/Anna-Paquin-b2FSL0drK3NubWc9-reviews",  
"siteId": "304059",  
"articleId": "sh_col_22_1373478370_reviews",  
"type": "reviews",  
"title": "TB_Paquin_ratings_reviews" 
}
```

## Oggetto convconfig {#section_pzv_ytb_c1b}

Se avete già completato la sezione Guida introduttiva, dovreste avere familiarità con l'oggetto Convconfig. Per abilitare le revisioni, aggiorna convconfig con i campi seguenti:

* **Alwaysshoweditor** *facoltativo* : Per impostazione predefinita, l'editor delle revisioni viene visualizzato solo dopo che l'utente preme il pulsante «Revisione in scrittura». Impostate questo parametro su true per visualizzare sempre l'editor.

* **stringa** *richiesta* dall'app: Nome app da usare per le revisioni. Devono essere «recensioni».

* **Stringa** *opzionale* defaultsort: Consente di selezionare l'opzione di ordinamento predefinita per Recensioni. I valori possibili sono: Mosthelpful, highestrated, lowestrated, newest e older.

* **Disabletitle***:* booleano opzionale: Disattiva e nasconde il campo titolo nell'editor delle revisioni, richiesto e visibile per impostazione predefinita. Il valore predefinito è true.

* **Enablehalfrating** *optional* booleano: Utilizzato per abilitare le metà valutazioni sul modulo di selezione stella predefinito. Il valore predefinito è true.

* **Hideshowreviewbutton** *opzionale* : Controlla se visualizzare [!UICONTROL Show My Review] il pulsante. Impostare su true per consentire agli utenti di selezionare o visualizzare le proprie revisioni.

* **Numero intero** *facoltativo:* numero intero utilizzato per impostare il numero di stelle visualizzate nel modulo di selezione stella predefinito. Il valore predefinito è 5. Può essere configurato fino a 100.

* **booleano** *opzionale* ratingsunyenabled: Utilizzato per mostrare la visualizzazione di riepilogo valutazioni sopra l'app Recensioni. Questa operazione deve essere attivata per utilizzare il riepilogo di ratingsummar. Il valore predefinito è true.

## Rivedi metadati raccolta {#section_k1s_sqb_c1b}

* **type:***stringa richiesta* : Definisce il tipo di raccolta. `reviews`Deve essere.

* **Matrice** *opzionale* ratingdimensions: Un array di stringhe per ogni tipo di dimensione utilizzato da questa raccolta. Se non viene specificata, sarà consentita solo la dimensione 1.

   Ad esempio, per consentire agli utenti di classificare il prodotto su «design», «features» e «performance», impostate l'array su: `ratingDimensions: [‘design’, ‘features’, ‘performance’]`

* **Numero intero** *facoltativo ratingsubparts* : Numero di partizioni da visualizzare nella casella di testo della revisione. Le etichette secondarie vengono trasmesse con il parametro come illustrato di seguito.

   >[!NOTE]
   >È necessario definire le etichette per ogni sottoparte.

* **Matrice** *opzionale* ratingsubpartsids: Consente di definire un ID per ogni sottoparte nella raccolta valutazioni, che può essere utilizzata per eseguire il targeting di tali elementi secondari in CSS e javascript. Quando gli utenti pubblicano revisioni, ciascuno `ratingSubpart` di essi dispone dell'attributo « `data-lf-subpart-id`», compilato con questo ID.

>[!NOTE]
>
>Per utilizzare `ratingSubpartsIds`, è `ratingSubparts` necessario definire anche il parametro param e la lunghezza dei due array deve corrispondere.

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
>In caso di utilizzo `ratingDimensions`, devi utilizzare l' `ratingSelectionDelegate`e `ratingDisplayDelegate``ratingSummaryDelegate` (per mostrare il riepilogo di valutazione).

## Personalizzazione revisioni {#section_khz_xmb_c1b}

### Configurare le immagini stella

Per modificare l'immagine per le stelle intere, la classe è `goog-ratings-star`. Cambia l'immagine di sfondo in qualsiasi immagine desiderata. Per impostazione predefinita, le stelle sono di 28 x 28 pixel.

### Configura immagini stella con mezza stella

Con metà stelle, sono disponibili due classi, una per ogni lato della stella. Il lato sinistro della mezza stella è `fyre-rating-half-odd` e il lato destro `fyre-rating-half-even`è. Per impostazione predefinita, le metà delle stelle sono 28 x 14 pixel.

### Configurare i valori delle descrizioni per le stelle

Per configurare i valori delle descrizioni comandi per le stelle, seguire il testo personalizzato descritto in Personalizzazione stringa. Una volta configurato, utilizzate la chiave `ratingValues` e il valore un array contenente le stringhe di descrizione comando. Se avete disattivato metà stelle, il numero di elementi nell'array deve essere uguale a `maxRating` (sopra). Se sono abilitate metà stelle, il numero di elementi deve essere pari a 2 x `maxRating`. Il primo elemento dell'array corrisponde all'elemento più a sinistra (o a mezza stella) e continua da sinistra a destra.

### Attiva/disattiva l'opzione Mostra revisione personale

Per attivare o disattivare l' [!UICONTROL Show My Review] opzione, eseguite il targeting del `hideShowReviewButton` parametro nella configurazione App.

### Mostra editor di testo per impostazione predefinita

L'editor delle revisioni viene visualizzato solo dopo che l'utente preme il [!UICONTROL write review] pulsante. Per visualizzare questo modulo per impostazione predefinita, eseguite il targeting del `alwaysShowEditor` parametro nella configurazione App.
