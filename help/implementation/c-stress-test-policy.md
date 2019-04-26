---
description: Eseguire test di stress rispetto alla piattaforma Livefyre.
seo-description: Eseguire test di stress rispetto alla piattaforma Livefyre.
seo-title: Criterio di stress test
solution: Experience Manager
title: Criterio di stress test
uuid: f 2 d 49 b 55-f 4 fc -485 f -9 aea-a 17 ce 64813 ee
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Criterio di stress test{#stress-test-policy}

Eseguire test di stress rispetto alla piattaforma Livefyre.

Questo documento fornisce indicazioni sull'esecuzione di test di stress rispetto alla piattaforma Livefyre. La verifica ad hoc dei clienti senza notifica è severamente vietata. Per ulteriori informazioni [sulle attività vietate e consentite](#c_stress_test_policy/section_mhs_bfz_vdb).

>[!NOTE]
>
>I test di stress sono facoltativi. Non è necessario o si deve eseguire un test di stress. Adobe Livefyre esegue regolarmente test di stress e convalida come parte del processo di rilascio. Se scegliete di eseguire test, questo documento delinea i requisiti e i vincoli per eseguire test di stress.

## Notifica {#section_ihs_bfz_vdb}

Devi notificare al tuo Specialista di successo clienti Livefyre e alla consulenza tecnica Adobe dei tuoi programmati test tre o più settimane prima di iniziare.

Per inviare una notifica a Livefyre, invia le seguenti informazioni al tuo specialista Customer Success Specire e al consulente tecnico Adobe:

* Finalità e descrizione del test
* Il caso d'uso a cui stai eseguendo il test
* Elenco di tutte le API di Livefyre che pianificate di utilizzare nel test
* Data, ora e durata del test
* Indirizzi IP da cui vengono avviati i test

## Requisiti {#section_khs_bfz_vdb}

È possibile eseguire test solo se soddisfano i seguenti requisiti:

* Dovete ricevere l'approvazione esplicita e scritta da un consulente tecnico Adobe 3 settimane o più prima di iniziare il test.
* **Potete eseguire test solo su UAT Network.**
* È necessario eseguire un test rispetto a scenari realistici. Ad esempio, non si supponga che la tua proprietà metta a servizio *milioni* di richieste di post ogni giorno, perché non si tratta di uno scenario realistico. Se ti serve assistenza per determinare se lo scenario è realistico o meno, chiedi al tuo Customer Success Specialist o consulente tecnico Adobe di Livefyre.
* I test devono essere condotti durante le ore di lavoro per il fuso orario Standard\ (UTC -7\).
* Potrebbe essere necessario produrre dati e il relativo ragionamento.

## Governance {#section_mhs_bfz_vdb}

Livefyre si riserva il diritto di sospendere un test in qualsiasi momento se esegui un test:

* Nella rete di produzione.
* Senza l'approvazione esplicita e scritta di un consulente tecnico Adobe o più settimane in anticipo.
* In situazioni inreali.

Livefyre termina i test bloccando l'accesso alle API, disabilitando Livefyre Networks e rifiutando una richiesta di prova del carico se non soddisfa i requisiti.
