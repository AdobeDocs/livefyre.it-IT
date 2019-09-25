---
description: nulle
seo-description: nulle
seo-title: Aggiunta di note a una pagina
solution: Experience Manager
title: Aggiunta di note a una pagina
uuid: 6499c45a-3773-4adb-a6c7-22a628309afd
translation-type: tm+mt
source-git-commit: bd989c97ae5cf06a5ac3deec215f865b0fe95d16

---


# Aggiunta di note a una pagina {#adding-sidenotes-to-a-page}

Livefyre offre diverse opzioni di configurazione per posizionare le note sulla pagina:

* L'opzione Selettori definisce gli elementi sui quali devono essere visualizzate le note.
* Gli ancoraggi rappresentano gli elementi che possono essere correlati.
* Il contenitore di thread personalizzato consente di definire la posizione del thread Sidenotes in relazione al contenuto collegato.
* L’opzione di conteggio delle note consente di visualizzare il numero di note aggiunte nella posizione specificata.
* Utilizzare più `ConvConfig` oggetti per aggiungere note a più brani su una singola pagina.

## Selettori {#section_wyj_4sv_sy}

L'opzione dei selettori consente a Note di trovare il contenuto della pagina. Il valore di questa opzione consente di determinare in modo dinamico gli elementi da utilizzare. Può trattarsi di una stringa selettore (ad esempio ‘#content p, #content img’), un oggetto jQuery (ad esempio `$(‘#content’)`), un array di elementi DOM o un oggetto con due proprietà: include ed esclude. L'app Sidenotes utilizzerà quindi gli elementi specificati o gli elementi corrispondenti nella pagina. Se si utilizzano le proprietà include ed exclude, Sidenotes prima analizzerà la pagina per trovare tutti gli elementi nella proprietà include, quindi rimuoverà eventuali elementi trovati nella proprietà exclude.

## Ancoraggi {#section_ehq_psv_sy}

Gli ancoraggi rappresentano un elemento il cui contenuto può essere sezionato. Un elemento di ancoraggio può contenere testo o immagine. L'opzione dei selettori che viene passata durante la creazione dell'app determinerà gli elementi di ancoraggio.

## ID ancoraggio {#section_rsb_rsv_sy}

Gli ancoraggi sulla pagina sono identificati mediante un `data-lf-anchor-id`.

Per impostare l’ID per un ancoraggio, aggiungete l’attributo `data-lf-custom-anchor-id` all’elemento da mappare a un ancoraggio. Ciò è utile nei casi in cui il rilevamento automatico degli ancoraggi potrebbe non riuscire.

Ad esempio, se prevedete di utilizzare un URL diverso per le versioni desktop e mobili di un’immagine, due URL diversi potrebbero essere mappati su ancoraggi diversi. Se, invece, il codice HTML fornisce uno `data-lf-custom-anchor-id` che è lo stesso sia per dispositivi mobili che per computer desktop, l'elemento immagine verrà trattato come un singolo ancoraggio.

Gli ancoraggi hanno un tipo determinato in modo dinamico, ma possono anche essere impostati in modo esplicito utilizzando l' `data-lf-custom-anchor-type` attributo.

>[!NOTE]
>
>È necessario utilizzare il valore del numero di enumerazione.

I tipi disponibili sono:

* **** Testo: 1
* **** Immagine: 2
* **** File multimediali: 3
* **** Rich: 4

Per ulteriori informazioni sull’utilizzo del metodo [updateAnchors, vedere metodo](/help/implementation/c-app-integrations/c-sidenotes-integration/update-anchors-method.md) `updateAnchors` updateAnchors per aggiungerecontenuto Sidenote alla pagina in modo dinamico.

## Contenitore thread personalizzato {#section_jdh_btv_sy}

Utilizzate l' `threadContainerEl` opzione per specificare una posizione per un thread Sidenotes diversa dalla posizione predefinita. Per impostazione predefinita, quando viene attivato un ancoraggio, le note vengono visualizzate accanto o sotto al contenuto corrispondente. Per modificare questa impostazione predefinita, utilizzate `threadContainerEl` per specificare l'elemento in cui deve essere visualizzato il thread.

Questo valore per questa opzione funziona allo stesso modo dell'opzione selettori, eccetto che verrà utilizzato solo il primo elemento valido.

## Numero di note {#section_pld_ntv_sy}

Utilizzate l' `numSidenotesEl` opzione per incorporare un widget di conteggio Sidenotes facoltativo nella pagina. Questa opzione accetta lo stesso input dell'opzione selettori, ma utilizza solo il primo elemento valido nell'array di input.

Il widget decorerà l’elemento fornito o associato e includerà l’icona di input Sidenotes, il numero di note inserite in questa posizione e un’icona di aiuto.

Facendo clic sul widget verrà visualizzato un puntatore con una breve spiegazione dei Sidenotes e di come utilizzarli.

Sia la spiegazione che il testo di esempio possono essere configurati utilizzando stringhe personalizzate ( `questionExplanation` e, rispettivamente, `questionMockText`). L'aspetto del widget di conteggio e del puntatore può essere configurato anche utilizzando stili personalizzati ( `numSidenotes` e, rispettivamente, `numSidenotesPopover`).

## Aggiunta di più raccolte di diapositive a una singola pagina {#section_pjl_ptv_sy}

Livefyre consente di aggiungere più raccolte Sidenotes a una singola pagina. Ad esempio, se la pagina include tre notizie, potete includere tre iterazioni separate dell'app Sidenotes. A questo scopo, è necessario definire un `ConvConfig` oggetto separato per ogni istanza di Note da creare. Ad esempio:

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
