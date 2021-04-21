---
description: Esegui test di stress contro la piattaforma Livefyre.
title: Criterio test di stress
exl-id: cb87b6ca-4107-46fc-9b1e-dc9399ec6d3a
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Criterio test stress{#stress-test-policy}

Esegui test di stress contro la piattaforma Livefyre.

Questo documento fornisce indicazioni sull&#39;esecuzione di stress test sulla piattaforma Livefyre. È severamente vietato eseguire test ad hoc da parte dei clienti senza notifica. Per ulteriori informazioni su [attività vietate e consentite](#c_stress_test_policy/section_mhs_bfz_vdb).

>[!NOTE]
>
>I test di stress sono facoltativi. Non è necessario o previsto eseguire una prova di stress. Adobe Livefyre effettua test di stress e convalide regolari come parte del processo di rilascio. Se si sceglie di eseguire i test, il presente documento illustra i requisiti e i vincoli per l&#39;esecuzione delle prove di stress.

## Notifica {#section_ihs_bfz_vdb}

Devi comunicare al tuo Specialista del successo cliente Livefyre e al Consulente Tecnico Adobe i test pianificati tre o più settimane prima di quando intendi iniziare.

Per notificare a Livefyre, invia le seguenti informazioni al tuo consulente tecnico specialista del successo del cliente Livefyre e al tuo consulente tecnico Adobe:

* Scopo e descrizione della prova
* Caso di utilizzo su cui si sta eseguendo il test
* Elenco di eventuali API Livefyre che intendi utilizzare nel test
* Data, ora e durata della prova
* Indirizzi IP da cui inizierai i test

## Requisiti {#section_khs_bfz_vdb}

Puoi eseguire i test solo se soddisfano i seguenti requisiti:

* È necessario ricevere l&#39;approvazione scritta esplicita da un consulente tecnico Adobe 3 settimane o più prima di iniziare il test.
* **È possibile eseguire i test solo sulla rete UAT.**
* È necessario testare scenari realistici. Ad esempio, potresti non presumere che la tua proprietà soddisfi *milioni* di richieste di post ogni giorno, perché questo non è uno scenario realistico. Se hai bisogno di assistenza per determinare se il tuo scenario è realistico o meno, chiedi al tuo Specialista del successo del cliente Livefyre o al Consulente Tecnico Adobe.
* Le prove devono essere effettuate durante l&#39;orario di lavoro per il fuso orario standard del Pacifico \(UTC -7\).
* Potrebbe essere necessario produrre dati e il ragionamento per il test.

## Governance {#section_mhs_bfz_vdb}

Livefyre si riserva il diritto di terminare un test in qualsiasi momento se si esegue un test:

* Sulla rete di produzione.
* Senza esplicita approvazione scritta da parte di un consulente tecnico Adobe con almeno tre settimane di anticipo.
* Contro scenari irreali.

Livefyre interrompe i test bloccando l’accesso alle API, disabilitando Livefyre Networks e rifiutando una richiesta di test di carico se non soddisfa i requisiti.
