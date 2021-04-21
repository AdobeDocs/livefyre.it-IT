---
description: È possibile modificare il testo di avviso visualizzato sulle maschere video utilizzando .
title: userPrivacyMaskDelegate
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---


# userPrivacyMaskDelegate{#userprivacymaskdelegate}

È possibile modificare il testo di avviso visualizzato sulle maschere video utilizzando .

Questo testo è conforme al regolamento RGPD. Se una sorgente non supporta un proxy, allora Livefyre visualizza questo testo e una maschera sul contenuto a meno che un utente non clicchi sul video e approvi il potenziale tracciamento da quella sorgente.

Se non si utilizza `userPrivacyMaskDelegate`, viene visualizzato il seguente testo predefinito:

Aggiungi `userPrivacyMaskDelegate` dopo `userPrivacyOptOut`. È possibile aggiungere tutti i flag per la privacy di Livefyre contemporaneamente come parte di un oggetto Livefyre.

Ecco un esempio di come utilizzare `userPrivacyMaskDelegate`:

```
userPrivacyMaskDelegate: function () { 
    var container = document.createElement('div'); 
    var firstParagraph = document.createElement('p'); 
    firstParagraph.innerHTML = 'Text of first paragraph'; 
    var secondParagraph = document.createElement('p'); 
    secondParagraph.innerHTML = 'Text of second paragraph'; 
    container.appendChild(firstParagraph); 
    container.appendChild(secondParagraph); 
    return container; 
}
```
