---
title: Applicazione SSL
description: Applicazione SSL
exl-id: 033e15d9-84f6-42d5-8457-04263dcbd11c
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 1%

---

# Applicazione SSL{#ssl-enforcement}

Per garantire che i dati rimangano protetti, è stato dichiarato obsoleto HTTP a favore di HTTPS. Adobe Livefyre disabiliterà completamente tutte le crittografia HTTP e SSL/TLS non sicure entro la fine di agosto 2018. Questo è un Adobe Standard progettato per proteggere la privacy di te e dei tuoi utenti.

## Chi è interessato? {#section_jf2_4yz_kcb}

Questo potrebbe avere un impatto sui clienti Livefyre che hanno:

* Chiamate server-to-server da CRM, CMS, WordPress o altro client.
* Integrazioni mobili (app Android e iOS)
* Applicazioni personalizzate o codice personalizzato

## Cosa devo fare? {#section_unv_dc5_kcb}

1. Tutti i clienti Livefyre devono comunicare con tutte le API tramite HTTPS per tutto il traffico, inclusi:

   * Integrazioni server-to-server (CRM, CMS, WordPress, ecc.)
   * Integrazioni mobili (app Android e iOS)
   * Applicazioni personalizzate (SDK Streamhub o direttamente codificato).

1. I client HTTP da server a server e mobile devono supportare TLS 1.2
1. Modifica i nomi host da `{*}.<network>.fyre.co` a `<network>.{*}.fyre.co`. Ad esempio, il nome host `example.network.fyre.co` diventa `network.`example.fyre.co&quot;. Ad esempio:

   * `bootstrap.<network_name>.fyre.co` in `<network_name>.bootstrap.fyre.co`

   * `quill.<network_name>.fyre.co` in `<network_name>.quill.fyre.co`

   * `admin.<network_name>.fyre.co` in `<network_name>.admin.fyre.co`

## Come faccio a sapere se ho apportato le modifiche? {#section_sqk_5d5_kcb}

Puoi già utilizzare HTTPS, ma Livefyre consiglia di eseguire un doppio controllo, soprattutto se disponi di:

* Chiamate server-to-server da CMS o CRM.
* Codice personalizzato o usa gli SDK per app personalizzate in JavaScript o Mobile.
* Se la tua integrazione ha più di un anno.
* Se la tecnologia nello stack è più vecchia di un anno.

Anche se utilizzi già HTTPS, devi verificare che i clienti API supportino TLS 1.2.

## Come posso verificare che i miei clienti API supportino TLS 1.2? {#section_nd1_j25_kcb}

Una persona che lavora allo sviluppo del sito può:

* Identificare il software client.
* Identifica la versione.
* Leggi la documentazione per assicurarti che il client API supporti TLS 1.2.
* Se necessario, attivare la modalità di debug.

## Supporto Java per TLS 1.2 {#section_lwn_rwk_ycb}

Le JVM Oracle e OpenJDK per Java 8 e versioni successive sono configurate per utilizzare TLS 1.2, per impostazione predefinita, per tutte le connessioni SSL. Non è necessario intraprendere alcuna azione aggiuntiva se si utilizza Java 8 o versione successiva.

Gli utenti di Java 7 o versioni precedenti devono consultare la documentazione pubblica su come abilitare TLS 1.2.

## Perché devo cambiare i nomi host? {#section_d5q_p25_kcb}

Livefyre non dispone di certificati SSL sui domini `{*}.<network>.fyre.co`. La semplice modifica dell’URL a HTTPS interrompe l’applicazione.

## Devo effettuare l’aggiornamento alla versione più recente degli SDK Livefyre? {#section_dw5_s25_kcb}

No. È invece possibile applicare una patch al codice. Per applicare la patch al codice, devi modificare alcune stringhe statiche e ricreare il codice. Se il client HTTP non è aggiornato, dovrai anche aggiornarlo o utilizzarne uno diverso.

## Quanto ci vorrà? {#section_lgd_v25_kcb}

Il tempo necessario dipende dalla configurazione. Se hai un’implementazione semplice, la conferma richiede poco tempo. Se disponi di molte personalizzazioni, dovrai testare e distribuire il codice aggiornato ai tuoi server o nuove app agli App Store. Per ottenere i migliori risultati, ti consigliamo di eseguire un controllo iniziale del lavoro in modo da poter pianificare qualsiasi lavoro a lungo termine.

## Qual è la tempistica per completare questo lavoro? {#section_kgk_w25_kcb}

Livefyre disabiliterà la porta 80 (HTTP) ai nostri servizi entro la fine di agosto 2018 e supporterà solo le connessioni a 443 (HTTPS). I browser e altri client che tentano di utilizzare HTTP avranno esito negativo.

## Quando devo finire questo lavoro? {#section_rvb_x25_kcb}

Tutti i clienti devono utilizzare HTTPS entro la fine di luglio 2018. Se non riesci a rispettare questa scadenza, contatta il nostro team all&#39;indirizzo prioritysupport@livefyre.com.
