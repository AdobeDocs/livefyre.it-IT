---
description: Potete modificare il testo di avviso visualizzato sulle maschere video utilizzando .
seo-description: Potete modificare il testo di avviso visualizzato sulle maschere video utilizzando .
seo-title: userPrivacyMaskDelegate
solution: Experience Manager
title: userPrivacyMaskDelegate
uuid: 8e5a2750-bf45-4e70-a5f9-37f5e7c61f8e
translation-type: tm+mt
source-git-commit: 9e01dd4515c01154e3566a39b367b8efa4ec082a
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---


# userPrivacyMaskDelegate{#userprivacymaskdelegate}

Potete modificare il testo di avviso visualizzato sulle maschere video utilizzando .

Questo testo è conforme al regolamento GDPR. Se un&#39;origine non supporta un proxy, Livefyre visualizza questo testo e una maschera sul contenuto a meno che un utente non faccia clic sul video e approvi il potenziale tracciamento da tale origine.

Se non si utilizza `userPrivacyMaskDelegate`, viene visualizzato il seguente testo predefinito:

Aggiungere `userPrivacyMaskDelegate` dopo `userPrivacyOptOut`. Potete aggiungere tutti i flag di privacy di Livefyre contemporaneamente come parte di un oggetto Livefyre.

Esempio di utilizzo di `userPrivacyMaskDelegate`:

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
