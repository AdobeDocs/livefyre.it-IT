---
description: Aggiungete il flag userPrivacyOptOut alla pagina per consentire al visitatore del sito di rifiutare questo tracciamento.
seo-description: Aggiungete il flag userPrivacyOptOut alla pagina per consentire al visitatore del sito di rifiutare questo tracciamento.
seo-title: userPrivacyOptOut
title: userPrivacyOptOut
uuid: a043c50e-0a02-4c83-bbce-54b9b51316a5
translation-type: tm+mt
source-git-commit: 9e01dd4515c01154e3566a39b367b8efa4ec082a
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---


# userPrivacyOptOut{#userprivacyoptout}

Aggiungete il flag `userPrivacyOptOut` alla pagina per consentire al visitatore del sito di rinunciare a questo tracciamento.

Livefyre fornisce eventi JavaScript per monitorare l&#39;attività degli utenti nelle app Livefyre.

Se incorporate le app Livefyre e un visitatore non accetta il tracciamento, potete configurare Livefyre in modo dinamico per disattivare la funzionalità per garantire la privacy del visitatore.

Una volta configurato, Livefyre:

* Disattiva il supporto dell&#39;autenticazione nelle app.
* Disattivazione della generazione di eventi e Livecount
* Elimina i cookie esistenti creati da qualsiasi app presente sulla pagina
* Proxy media con immagini da domini di terze parti per impedire a terzi di creare cookie
* Abilita click-through maschera video per video di terze parti che richiedono un clic aggiuntivo per visualizzare

## Configurare una pagina per il rifiuto

Le integrazioni che incorporano le app Livefyre possono configurare Livefyre quando un visitatore del sito non ha concesso il consenso utilizzando una singola variabile JavaScript.

Istruzioni:

1. Aggiungete il flag `userPrivacyOptOut` alla pagina prima del `Livefyre.js` JavaScript:

   ```
   window.Livefyre = {userPrivacyOptOut: true};
   ```

1. Aggiungete `Livefyre.js` alla pagina dopo `userPrivacyOptOut`.

   Le app Livefyre creano un&#39;istanza con le impostazioni di privacy elevate.

   >[!NOTE]
   >
   >Non modificate il valore di `userPrivacyOptOut` dopo il caricamento delle app Livefyre.

Assicurati che il flusso di lavoro di consenso imposti il valore `userPrivacyOptOut` su true se un visitatore del sito sceglie di rifiutare.
