---
title: Aggiunta di note a una pagina
description: Aggiunta di note a una pagina
exl-id: 3ec089d0-3d51-4918-b510-d30ef645c9c2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 0%

---

# Aggiunta di note a una pagina {#adding-sidenotes-to-a-page}

Livefyre fornisce diverse opzioni di configurazione per posizionare Note a margine sulla pagina:

* L’opzione Selettori definisce gli elementi sui quali devono essere visualizzate le note a margine.
* Gli ancoraggi rappresentano elementi che possono essere affiancati.
* Il contenitore di thread personalizzato ti consente di definire dove si troverà il thread Sidenotes in relazione al contenuto basato su barre.
* L’opzione di conteggio delle note consente di visualizzare il numero di note aggiunte nella posizione specificata.
* Utilizzare più oggetti `ConvConfig` per aggiungere note a più brani in una singola pagina.

## Selettori {#section_wyj_4sv_sy}

L’opzione selettori consente alle note a margine di trovare il contenuto nella pagina. Il valore di questa opzione ti consente di determinare in modo dinamico gli elementi da utilizzare. Può trattarsi di una stringa di selettore (ad esempio &quot;#content p, #content img&quot;), di un oggetto jQuery (ad esempio `$(‘#content’)`), di una matrice di elementi DOM o di un oggetto con due proprietà: includere ed escludere. L’app Note a margine utilizzerà quindi gli elementi specificati o quelli corrispondenti nella pagina. Se si utilizzano le proprietà di inclusione ed esclusione, le note analizza prima la pagina per trovare tutti gli elementi nella proprietà include , quindi rimuovi eventuali elementi trovati nella proprietà exclude.

## Ancoraggi {#section_ehq_psv_sy}

I punti di ancoraggio rappresentano un elemento il cui contenuto può essere collegato. Un elemento di ancoraggio può contenere testo o immagine. L’opzione dei selettori che viene passata durante la costruzione dell’app determinerà gli elementi di ancoraggio.

## ID ancoraggio {#section_rsb_rsv_sy}

Gli ancoraggi nella pagina vengono identificati utilizzando un `data-lf-anchor-id`.

Per impostare l’ID per un ancoraggio, aggiungi l’attributo `data-lf-custom-anchor-id` all’elemento da mappare su un ancoraggio. Questa funzione è utile nei casi in cui il rilevamento automatico degli ancoraggi potrebbe non riuscire.

Ad esempio, se prevedi di utilizzare un URL diverso per le versioni desktop e mobili di un’immagine, due URL diversi possono essere mappati su ancoraggi diversi. Se invece il codice HTML fornisce un elemento `data-lf-custom-anchor-id` uguale sia per i dispositivi mobili che per quelli desktop, l’elemento immagine verrà trattato come un singolo ancoraggio.

Gli ancoraggi hanno un tipo determinato dinamicamente, ma possono anche essere impostati esplicitamente utilizzando l&#39;attributo `data-lf-custom-anchor-type` .

>[!NOTE]
>
>È necessario utilizzare il valore del numero di enumerazione.

I tipi disponibili sono:

* **Testo:** 1
* **Immagine:** 2
* **File multimediali:** 3
* **Rich:** 4

Per ulteriori informazioni su come utilizzare il metodo `updateAnchors` per aggiungere in modo dinamico contenuto Sidenote alla pagina, consulta [updateAnchors method](/help/implementation/c-app-integrations/c-sidenotes-integration/update-anchors-method.md) .

## Contenitore di thread personalizzato {#section_jdh_btv_sy}

Utilizzare l&#39;opzione `threadContainerEl` per specificare una posizione per un thread Sidenotes, diversa dalla posizione predefinita. Per impostazione predefinita, quando viene attivato un ancoraggio, le note vengono visualizzate accanto o sotto il contenuto pertinente. Per modificare questa impostazione predefinita, utilizza `threadContainerEl` per specificare l&#39;elemento in cui deve essere visualizzato il thread.

Questo valore per questa opzione funziona come l’opzione selettori, tranne che verrà utilizzato solo il primo elemento valido.

## Conteggio note {#section_pld_ntv_sy}

Utilizza l’opzione `numSidenotesEl` per incorporare un widget di conteggio delle note facoltativo nella pagina. Questa opzione accetta lo stesso input dell’opzione selettori ma utilizza solo il primo elemento valido nell’array di input.

Il widget decorerà l&#39;elemento fornito o corrispondente e includerà l&#39;icona di input Note a margine, il numero di Note a margine inserito in questa posizione e un&#39;icona di aiuto.

Facendo clic sul widget verrà visualizzato un pover con una breve spiegazione delle Note a margine e come usarle.

Sia la spiegazione che il testo di esempio sono configurabili utilizzando stringhe personalizzate ( `questionExplanation` e `questionMockText` rispettivamente). L’aspetto del widget di conteggio e del pover possono essere configurati anche utilizzando stili personalizzati ( `numSidenotes` e `numSidenotesPopover`, rispettivamente).

## Aggiunta di più raccolte di note a una singola pagina {#section_pjl_ptv_sy}

Livefyre consente di aggiungere più raccolte di note a margine a una singola pagina. Ad esempio, se la pagina include tre news, è possibile includere tre iterazioni separate dell’app Sidenotes. A questo scopo, devi definire un oggetto `ConvConfig` separato per ogni istanza di Note a margine che desideri creare. Ad esempio:

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
