---
description: Eseguire stress test sulla piattaforma Livefyre.
seo-description: Eseguire stress test sulla piattaforma Livefyre.
seo-title: Criterio test di stress
solution: Experience Manager
title: Criterio test di stress
uuid: f2d49b55-f4fc-485f-9aea-a17ce64813ee
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Criterio test di stress{#stress-test-policy}

Eseguire stress test sulla piattaforma Livefyre.

Questo documento fornisce indicazioni sull'esecuzione di stress test sulla piattaforma Livefyre. I test ad hoc effettuati dai clienti senza notifica sono severamente vietati. Per ulteriori informazioni sulle attività [vietate e consentite](#c_stress_test_policy/section_mhs_bfz_vdb).

>[!NOTE]
>
>I test di stress sono facoltativi. Non è necessario o previsto eseguire una prova di stress. Adobe Livefyre esegue regolarmente stress test e convalide nell'ambito del processo di rilascio. Se si sceglie di eseguire i test, in questo documento vengono delineati i requisiti e i vincoli per l'esecuzione dei test di stress.

## Notifica {#section_ihs_bfz_vdb}

Devi comunicare al tuo Specialista del successo dei clienti Livefyre e al Consulente tecnico Adobe che hai pianificato i test tre o più settimane prima di quando intendi iniziare.

Per inviare una notifica a Livefyre, inviate le seguenti informazioni al vostro consulente tecnico Livefyre e specialista del successo dei clienti:

* Finalità e descrizione della prova
* Caso di utilizzo per il quale state eseguendo il test
* Elenco delle eventuali API Livefyre che prevedete di utilizzare nel test
* Data, ora e durata del test
* Indirizzi IP da cui inizierete i test

## Requisiti {#section_khs_bfz_vdb}

Potete eseguire i test solo se soddisfano i seguenti requisiti:

* Prima di iniziare il test, è necessario ricevere l'approvazione scritta e esplicita da un consulente tecnico Adobe per almeno 3 settimane.
* **È possibile eseguire test solo sulla rete UAT.**
* È necessario eseguire il test in base a scenari realistici. Ad esempio, è possibile che non si supponga che la proprietà servirà *milioni* di richieste di post ogni giorno, perché non si tratta di uno scenario realistico. Se avete bisogno di assistenza per determinare se lo scenario è realistico o meno, chiedete al vostro consulente tecnico Livefyre o al vostro consulente tecnico Adobe.
* Le prove devono essere eseguite durante le ore lavorative per il fuso orario standard del Pacifico \(UTC -7\).
* Potrebbe essere necessario produrre i dati e il ragionamento per il test.

## Governance {#section_mhs_bfz_vdb}

Livefyre si riserva il diritto di terminare un test in qualsiasi momento se si esegue un test:

* Sulla rete di produzione.
* Senza l’approvazione scritta e esplicita di un consulente tecnico Adobe con almeno tre settimane di anticipo.
* Contro scenari irreali.

Livefyre interrompe i test bloccando l'accesso alle API, disattivando le reti Livefyre e rifiutando una richiesta di test di carico se non soddisfa i requisiti.
