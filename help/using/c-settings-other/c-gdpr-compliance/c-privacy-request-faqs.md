---
description: Risposte alle domande frequenti sulle richieste di privacy pronte per il RGPD.
title: Domande frequenti sulle richieste di privacy
exl-id: 6d0add45-589a-46d0-b15a-63a7599aad73
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---

# Domande frequenti sulle richieste di privacy{#privacy-request-faqs}

Risposte alle domande frequenti sulle richieste di privacy pronte per il RGPD.

* **Come possono i visitatori del sito rinunciare a essere tracciati su un sito che utilizza le app Livefyre?** Quando un visitatore del sito rinuncia, l’implementazione del cliente deve indicare a Livefyre che l’utente ha rinunciato prima di creare un’istanza di un’app. Livefyre ha creato un modo per farlo con l’opzione JavaScript `userPrivacyOptOut`. Per ulteriori informazioni sull&#39;utilizzo di `userPrivacyOptOut`, consulta [userPrivacyOptOut](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md).

   Quando il flag `userPrivacyOptOut` è impostato su true, qualsiasi app nella pagina non trasmetterà dati ai server Livefyre utilizzando cookie o un altro metodo. Livefyre non aggiornerà quindi l’archiviazione locale con i dati che potrebbero essere utilizzati per tenere traccia dei visitatori del sito. Se una sorgente non supporta un proxy, Livefyre visualizza una maschera sul contenuto a meno che un utente non faccia clic sul video e approvi il potenziale tracciamento da tale sorgente.

   Se utilizzi Livefyre Identity, gli utenti possono scegliere di eliminare il profilo o creare un rapporto dei dati tracciati per il proprio account utente.

* **Come posso evitare di raccogliere contenuti futuri da un visitatore del sito che ha rinunciato?** Utilizza  `userPrivacyOptOut` con  `livefyre.js` in una pagina web che utilizza le app Livefyre. Per ulteriori informazioni su `userPrivacyOptOut`, consulta [userPrivacyOptOut](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md).

* **Come posso generare un rapporto ed eliminare i dati per gli Utenti app o i proprietari di account social?** [Richiesta di privacy ](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) per generare un rapporto ed eliminare i dati utente dalle app.

* **Come posso rimuovere tutto il contenuto per un visitatore?** Livefyre non mantiene informazioni persistenti sui visitatori del sito, eccetto sotto forma di cookie per identificarli in modo univoco per le funzioni di Livecount. Livecount è un conteggio transitorio e in tempo reale dei visitatori sul sito. Non viene conservata alcuna cronologia dopo che il visitatore lascia o cancella i cookie.

   Crea una [richiesta di privacy](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) per eliminare l&#39;account. Livefyre elimina o rende anonimi il profilo utente e tutti i record associati.

* **Come si rimuove il contenuto per un utente registrato?** Crea una  [richiesta di ](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) privacy per eliminare l’account. Il profilo utente ed eventuali record associati verranno completamente distrutti.

   >[!NOTE]
   >
   >Questa azione non può essere annullata.

* **Come si crea un rapporto dei dati tracciati da un dipendente corrente o precedente?** [Visualizzare un ](../../c-settings-other/c-gdpr-compliance/c-view-a-privacy-report.md#c_view_a_privacy_report) rapporto sulla privacy per generare un rapporto sui dati tracciati per un account utente.

* **Livefyre è compatibile con il flusso sociale?** Quando un utente elimina un post o un tweet dal proprio social network, entro 24 ore il contenuto viene anche eliminato da tutte le fonti in Livefyre. Questo vale per Twitter e Facebook.
