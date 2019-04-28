---
description: Aggiungete il flag userprivacyoptout alla pagina per consentire a un visitatore del sito di rifiutare il tracciamento.
seo-description: Aggiungete il flag userprivacyoptout alla pagina per consentire a un visitatore del sito di rifiutare il tracciamento.
seo-title: Userprivacyoptout
title: Userprivacyoptout
uuid: a 043 c 50 e -0 a 02-4 c 83-bbce -54 b 9 b 51316 a 5
translation-type: tm+mt
source-git-commit: 097321964ff078bac83c4674100f8c62a8f3a1af

---


# Userprivacyoptout{#userprivacyoptout}

Aggiungete il `userPrivacyOptOut` flag alla pagina per consentire al visitatore di un sito di rifiutare il tracciamento.

Livefyre fornisce eventi javascript per tenere traccia dell&#39;attività utente nelle app di Livefyre.

Se incorporate Livefyre Apps e un visitatore non accetta il consenso, potete configurare in modo dinamico Livefyre per disabilitare la funzionalità per garantire la privacy del visitatore.

Una volta configurato, Livefyre sarà in grado di:

* Disabilitare il supporto dell&#39;autenticazione nelle app.
* Disattivazione della generazione di Livecount e eventi
* Eliminare i cookie esistenti creati da qualsiasi app presente nella pagina
* File multimediali proxy con immagini di domini di terze parti per impedire ai terze parti di creare cookie
* Abilita click-through maschera video per video di terze parti che richiedono un clic aggiuntivo per la visualizzazione

## Configurare una pagina per la rinuncia

Le integrazioni integrative Livefyre Apps possono configurare Livefyre quando un visitatore del sito non ha concesso il consenso utilizzando una sola variabile javascript.

Istruzioni:

1. Aggiungere il `userPrivacyOptOut` flag alla pagina prima di `Livefyre.js` javascript:

   ```
   window.Livefyre = {userPrivacyOptOut: true};
   ```

1. Aggiungete `Livefyre.js` alla pagina ovunque dopo `userPrivacyOptOut`.

   Livefyre Apps crea un&#39;istanza delle impostazioni di privacy avanzate.

   >[!NOTE]
   >
   >Non modificate il valore di `userPrivacyOptOut` una volta caricata Livefyre Apps.

Assicurati che il flusso di lavoro del consenso imposti su `userPrivacyOptOut` true se un visitatore sceglie di rifiutare.
