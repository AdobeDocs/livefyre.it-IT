---
description: Aggiungi il flag userPrivacyOptOut alla pagina per consentire ai visitatori del sito di rinunciare a questo tracciamento.
title: userPrivacyOptOut
exl-id: 1e935e69-60af-4151-905c-93a1cccbeb49
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# userPrivacyOptOut{#userprivacyoptout}

Aggiungi il flag `userPrivacyOptOut` alla pagina per consentire ai visitatori del sito di rinunciare a questo tracciamento.

Livefyre fornisce eventi JavaScript per monitorare l’attività dell’utente nelle app Livefyre.

Se incorpori le app Livefyre e un visitatore non acconsente al tracciamento, puoi configurare in modo dinamico Livefyre per disabilitare la funzionalità per garantire la privacy del visitatore.

Una volta configurata, Livefyre eseguirà le seguenti operazioni:

* Disattiva il supporto dell&#39;autenticazione nelle app.
* Disattiva la generazione di eventi e Livecount
* Elimina i cookie esistenti creati da qualsiasi app presente nella pagina
* Proxy media con immagini da domini di terze parti per impedire a terzi di creare cookie
* Attiva click-through di maschera video per video di terze parti che richiedono un clic aggiuntivo per visualizzare

## Configurare una pagina per la rinuncia

Le integrazioni che incorporano le app Livefyre possono configurare Livefyre quando un visitatore del sito non ha concesso il consenso utilizzando una singola variabile JavaScript.

Istruzioni:

1. Aggiungi il flag `userPrivacyOptOut` alla pagina prima del codice JavaScript `Livefyre.js`:

   ```
   window.Livefyre = {userPrivacyOptOut: true};
   ```

1. Aggiungi `Livefyre.js` alla pagina in un punto qualsiasi dopo `userPrivacyOptOut`.

   Le app Livefyre creano un&#39;istanza con le impostazioni di privacy elevate.

   >[!NOTE]
   >
   >Non modificare il valore di `userPrivacyOptOut` dopo il caricamento delle app Livefyre.

Assicurati che il flusso di lavoro di consenso imposti il valore `userPrivacyOptOut` su true se un visitatore del sito sceglie di rinunciare.
