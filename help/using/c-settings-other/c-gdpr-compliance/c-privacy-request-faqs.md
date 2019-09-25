---
description: Risposte alle domande frequenti sulle richieste di privacy GDPR.
seo-description: Risposte alle domande frequenti sulle richieste di privacy GDPR.
seo-title: Domande frequenti sulla richiesta di privacy
solution: Experience Manager
title: Domande frequenti sulla richiesta di privacy
uuid: 0cd6f0d2-504d-46e9-ac46-070536cda086
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Domande frequenti sulla richiesta di privacy{#privacy-request-faqs}

Risposte alle domande frequenti sulle richieste di privacy GDPR.

* **In che modo i visitatori del sito possono scegliere di non essere tracciati su un sito che utilizza le app Livefyre?** Quando un visitatore del sito rinuncia, l'implementazione del cliente deve indicare a Livefyre che l'utente ha rinunciato prima di creare un'istanza dell'app. Livefyre ha creato un modo per farlo con l'opzione JavaScript, `userPrivacyOptOut`. Per ulteriori informazioni sull'utilizzo `userPrivacyOptOut`, vedere [userPrivacyOptOut](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md).

   Quando il `userPrivacyOptOut` flag è impostato su true, qualsiasi app sulla pagina non trasmetterà dati ai server Livefyre utilizzando cookie o un altro metodo. Livefyre non aggiornerà quindi l'archiviazione locale con i dati che potrebbero essere utilizzati per monitorare i visitatori del sito. Se una sorgente non supporta un proxy, Livefyre visualizza una maschera sul contenuto a meno che un utente non faccia clic sul video e approvi il potenziale tracciamento da tale origine.

   Se utilizzate Identità Livefyre, gli utenti possono scegliere di eliminare il proprio profilo o creare un rapporto dei dati tracciati per il proprio account utente.

* **Come posso impedire la raccolta di contenuti futuri da un visitatore del sito che ha rinunciato?** Utilizzate `userPrivacyOptOut` con `livefyre.js` una pagina Web che utilizza le app Livefyre. Per ulteriori informazioni su `userPrivacyOptOut`userPrivacyOptOut [](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md).

* **Come posso generare un rapporto ed eliminare i dati per gli Utenti app o i proprietari di account social?** Richieste [di](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) privacy per generare un rapporto ed eliminare i dati utente dalle app.

* **Come si rimuove tutto il contenuto per un visitatore?** Livefyre non mantiene informazioni persistenti sui visitatori del sito, tranne che sotto forma di cookie per identificarli in modo univoco per le funzioni Livecount. Livecount è un conteggio transitorio e in tempo reale dei visitatori sul sito. Non viene conservata alcuna cronologia dopo che il visitatore lascia o cancella i cookie.

   Create una richiesta [di](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) privacy per eliminare l'account. Livefyre elimina o rende anonimi il profilo utente e tutti i record associati.

* **Come si rimuove il contenuto per un utente registrato?** Create una richiesta di [privacy](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) per eliminare l'account. Il profilo utente ed eventuali record associati verranno eliminati completamente.

   >[!NOTE]
   >
   >Questa azione non può essere annullata.

* **Come si crea un rapporto dei dati tracciati da un dipendente corrente o ex?** [Visualizzare un rapporto](../../c-settings-other/c-gdpr-compliance/c-view-a-privacy-report.md#c_view_a_privacy_report) sulla privacy per generare un rapporto dei dati tracciati per un account utente.

* **Livefyre è compatibile con il flusso sociale?** Quando un utente elimina un post o un tweet dal social network, entro 24 ore il contenuto viene eliminato anche da tutte le fonti in Livefyre. Questo vale per Twitter e Facebook.

