---
description: nulle
seo-description: nulle
seo-title: Aggiunta di Filienotes a una pagina
solution: Experience Manager
title: Aggiunta di Filienotes a una pagina
uuid: 6499 c 45 a -3773-4 adb-a 6 c 7-22 a 628309 afd
translation-type: tm+mt
source-git-commit: bd989c97ae5cf06a5ac3deec215f865b0fe95d16

---


# Aggiunta di Filienotes a una pagina {#adding-sidenotes-to-a-page}

Livefyre offre diverse opzioni di configurazione per la posizione di Sidenotes sulla pagina:

* L&#39;opzione Selettori definisce gli elementi su cui dovrebbe essere visualizzato Sidenotes.
* Gli ancoraggi rappresentano elementi che possono essere separati.
* Il contenitore di thread personalizzato consente di definire dove si trova il thread Sidenotes rispetto al contenuto in uso.
* L&#39;opzione Conteggio Sidenotes consente di visualizzare il numero di filienalità aggiunte nel percorso specificato.
* Utilizzate più `ConvConfig` oggetti per aggiungere Filienotes a più brani su una singola pagina.

## Selettori {#section_wyj_4sv_sy}

L&#39;opzione selettori consente a Sidenotes di trovare contenuto sulla pagina. Il valore di questa opzione consente di determinare in modo dinamico gli elementi che verranno utilizzati. Può trattarsi di una stringa di selezione (ad esempio,&#39;# content p, # content img &#39;), un oggetto jquery (ad esempio `$(‘#content’)`), un array di elementi DOM o un oggetto con due proprietà: includere ed escludere. L&#39;app Sidenotes utilizzerà quindi gli elementi specificati o gli elementi corrispondenti sulla pagina. Se includete ed escludete le proprietà, Sidenotes analizzerà prima la pagina per trovare tutti gli elementi sulla proprietà Includi, quindi rimuovete gli elementi trovati nella proprietà exclude.

## Ancoraggi {#section_ehq_psv_sy}

Gli ancoraggi rappresentano un elemento il cui contenuto può essere dichiarato sidencato. Un elemento di ancoraggio può contenere testo o un&#39;immagine. L&#39;opzione selettori passata durante la creazione dell&#39;app determinerà gli elementi di ancoraggio.

## ID di ancoraggio {#section_rsb_rsv_sy}

Anchors on the page are identified using a `data-lf-anchor-id`.

Per impostare l&#39;ID di un ancoraggio, aggiungi l&#39;attributo `data-lf-custom-anchor-id` all&#39;elemento da mappare su un ancoraggio. Ciò è utile qualora il rilevamento automatico degli ancoraggi non riesca.

Ad esempio, se pianificate di utilizzare un URL diverso per le versioni desktop e mobili di un&#39;immagine, due URL diversi potrebbero essere mappati su diversi ancoraggi. Se, invece, gli articoli HTML sono `data-lf-custom-anchor-id` identici sia su dispositivi mobili che su desktop, l&#39;elemento immagine verrà trattato come un singolo ancoraggio.

Gli ancoraggi hanno un tipo determinato in modo dinamico, ma possono anche essere impostati in modo esplicito mediante l&#39; `data-lf-custom-anchor-type` attributo.

>[!NOTE]
>
>È necessario utilizzare il valore del numero di enumerazione.

I tipi disponibili sono:

* **Testo:** 1
* **Immagine:** 2
* **File multimediali:** 3
* **Rich:** 4

Per [ulteriori informazioni](/help/implementation/c-app-integrations/c-sidenotes-integration/update-anchors-method.md) sull&#39;utilizzo del `updateAnchors` metodo per aggiungere contenuti Sidenote alla pagina, consultate il metodo updateanchors.

## Contenitore thread personalizzato {#section_jdh_btv_sy}

Utilizzate `threadContainerEl` l&#39;opzione per specificare una posizione per un thread Sidenotes, diverso dalla posizione predefinita. Per impostazione predefinita, quando viene attivato un ancoraggio, le Filienotes vengono visualizzate accanto o sotto i contenuti pertinenti. Per modificare questa impostazione predefinita, usate l&#39;elemento `threadContainerEl` per specificare l&#39;elemento in cui dovrebbe essere visualizzato il thread.

Questo valore per questa opzione funziona come l&#39;opzione selettori, fatta eccezione per il primo elemento valido.

## Conteggio utenti {#section_pld_ntv_sy}

Utilizzate `numSidenotesEl` l&#39;opzione per incorporare nella pagina un widget Conteggio Sidenotes facoltativo. Questa opzione accetta lo stesso input dell&#39;opzione selettori ma utilizza solo il primo elemento valido nell&#39;array di input.

Il widget decorerà l&#39;elemento fornito o corrispondente e includerà l&#39;icona di immissione Sidenotes, il numero di Sidenotes immesso in questa posizione e un&#39;icona di aiuto.

Facendo clic sul widget viene visualizzato un contenitore con una breve spiegazione di Sidenotes.

Sia la spiegazione che il testo di esempio sono configurabili mediante stringhe personalizzate ( `questionExplanation` e `questionMockText`, rispettivamente). L&#39;aspetto del widget del conteggio e del contenitore può anche essere configurato mediante stili personalizzati ( `numSidenotes` e `numSidenotesPopover`, rispettivamente).

## Aggiunta di raccolte Sidenotes a una singola pagina {#section_pjl_ptv_sy}

Livefyre consente di aggiungere più raccolte Sidenotes a una singola pagina. Ad esempio, se la pagina include tre testimonianze di notizie, potreste voler includere tre iterazioni distinte dell&#39;app Sidenotes. A tal fine, è necessario definire un `ConvConfig` oggetto separato per ogni istanza di Sidenotes che si desidera creare. Ad esempio:

```
<html> 
   <head> 
      <script src="//cdn.livefyre.com/Livefyre.js"></script> 
   </head> 
<body> 
   <h2>Story #1</h2> 
   <div id="story1"> 
      <p class="sidenotes">stuff #1</p> 
      <p class="sidenotes">more stuff #1</p> 
   </div> 
   <hr /> 
   <h2>Story #2</h2> 
   <div id="story2"> 
      <p class="sidenotes">stuff #2</p> 
      <p class="sidenotes">more stuff #2</p> 
      <p class="sidenotes">more and more stuff</p> 
   </div> 
   <hr /> 
   <script type="text/javascript"> 
      var convConfig_story1 = { 
         network: '<Your Network>', 
         siteId: '<Site ID>', 
         articleId: '<Your Article ID>', 
         selectors: '#story1 > p.sidenotes', 
         collectionMeta: '<First collectionMeta>' 
      }; 
  
      var convConfig_story2 = { 
         network: '<Your Network>', 
         siteId: '<Site ID>', 
         articleId: '<Your Second Article ID>', 
         selectors: '#story2 > p.sidenotes', 
         collectionMeta: '<Second collectionMeta>' 
      }; 
  
      Livefyre.require(['sidenotes#1', 'auth'], function(Sidenotes, auth) { 
         new Sidenotes(convConfig_story1); 
         new Sidenotes(convConfig_story2); 
         auth.delegate({ 
            login: function (callback) { 
               callback(null,{livefyre: '<Login Token>'}); 
            } 
         }); 
      }); 
   </script> 
</body> 
</html>
```
