---
description: Potete modificare il testo di avviso visualizzato sulle maschere di video utilizzando.
seo-description: Potete modificare il testo di avviso visualizzato sulle maschere di video utilizzando.
seo-title: Userprivacymaskdelegate
solution: Experience Manager
title: Userprivacymaskdelegate
uuid: 8 e 5 a 2750-bf 45-4 e 70-a 5 f 9-37 f 5 e 7 c 61 f 8 e
translation-type: tm+mt
source-git-commit: 097321964ff078bac83c4674100f8c62a8f3a1af

---


# Userprivacymaskdelegate{#userprivacymaskdelegate}

Potete modificare il testo di avviso visualizzato sulle maschere di video utilizzando.

Questo testo esiste per conformità al regolamento GDPR. Se un&#39;origine non supporta un proxy, Livefyre visualizza il testo e una maschera sul contenuto a meno che un utente non faccia clic sul video e approvi il potenziale tracciamento da tale origine.

Se non utilizzate `userPrivacyMaskDelegate`, viene visualizzato il seguente testo predefinito:

Aggiungi `userPrivacyMaskDelegate` dopo `userPrivacyOptOut`. Potete aggiungere tutti i flag sulla privacy di Livefyre contemporaneamente come parte di un unico oggetto Livefyre.

Esempio di utilizzo `userPrivacyMaskDelegate`:

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
