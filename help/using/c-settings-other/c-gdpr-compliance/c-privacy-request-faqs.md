---
description: Risposte alle domande frequenti (FAQ) sulle richieste sulla privacy GDPR-Ready.
seo-description: Risposte alle domande frequenti (FAQ) sulle richieste sulla privacy GDPR-Ready.
seo-title: Domande frequenti sulla privacy
solution: Experience Manager
title: Domande frequenti sulla privacy
uuid: 0 cd 6 f 0 d 2-504 d -46 e 9-ac 46-070536 cda 086
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Domande frequenti sulla privacy{#privacy-request-faqs}

Risposte alle domande frequenti (FAQ) sulle richieste sulla privacy GDPR-Ready.

* **In che modo i visitatori del sito rifiutano di essere tracciati su un sito che utilizza Livefyre Apps?** Quando un visitatore del sito esce, l&#39;implementazione del cliente deve indicare a Livefyre che l&#39;utente ha acconsentito prima di creare un&#39;istanza di un&#39;app. Livefyre has created a way to do this with the JavaScript option, `userPrivacyOptOut`. Per ulteriori informazioni sull&#39;utilizzo `userPrivacyOptOut`, consultate [userprivacyoptout](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md).

   Quando `userPrivacyOptOut` il flag è impostato su true, tutte le app nella pagina non trasmettono i dati ai server Livefyre utilizzando cookie o un altro metodo. Livefyre non aggiornerà quindi l&#39;archiviazione locale con i dati che potevano essere utilizzati per tenere traccia dei visitatori del sito. Se un&#39;origine non supporta un proxy, Livefyre visualizza una maschera sul contenuto a meno che un utente non faccia clic sul video e approvi il potenziale tracciamento da tale origine.

   Se utilizzate Livefyre Identity, gli utenti possono scegliere di eliminare il proprio profilo o di creare un rapporto dei dati tracciati per il loro account utente.

* **Come si evita di raccogliere contenuto futuro da un visitatore che ha acconsentito?** Utilizzate `userPrivacyOptOut` con una `livefyre.js` pagina Web che utilizza Livefyre Apps. Per ulteriori informazioni `userPrivacyOptOut`, consulta [userprivacyoptout](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md).

* **Come si genera un rapporto ed elimina i dati per gli utenti delle app o i proprietari degli account social?**[Richieste sulla privacy](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) per generare un rapporto ed eliminare dati utente da App.

* **Come si rimuove tutto il contenuto per un visitatore?** Livefyre non mantiene le informazioni persistenti sui visitatori del sito, fatta eccezione per i cookie che identificano in modo univoco le funzioni di Livecount. Livecount è un conteggio transitorio e in tempo reale dei visitatori sul sito. Una cronologia non viene conservata dopo che il visitatore lascia o cancella i cookie.

   Create una [richiesta sulla privacy](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) per eliminare l&#39;account. Livefyre elimina o rende anonimo il profilo utente e tutti i record associati.

* **Come si rimuove il contenuto per un utente registrato?** Create un&#39;richiesta [privacy](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) per eliminare l&#39;account. Il profilo utente e tutti i record associati verranno eliminati completamente.

   >[!NOTE]
   >
   >Questa azione non può essere annullata.

* **Come si genera un rapporto sui dati tracciati di un dipendente corrente o precedente?**[Visualizzare un Rapporto](../../c-settings-other/c-gdpr-compliance/c-view-a-privacy-report.md#c_view_a_privacy_report) sulla privacy per generare un rapporto sui dati tracciati per un account utente.

* **Livefyre è conforme allo standard social?** Quando un utente elimina un post o un tweet dal loro social network, entro 24 ore anche il contenuto viene eliminato da tutte le origini di Livefyre. Ciò si applica a Twitter e Facebook.

