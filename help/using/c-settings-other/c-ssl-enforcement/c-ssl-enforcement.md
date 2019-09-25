---
description: nulle
seo-description: nulle
seo-title: Applicazione SSL
solution: Experience Manager
title: Applicazione SSL
uuid: e64af8c2-3ab6-4034-b385-0e552d828c6e
translation-type: tm+mt
source-git-commit: 7dc3ac6725a27460cecfa6051549da85370ca053

---


# Applicazione SSL{#ssl-enforcement}

Per garantire che i dati restino protetti, il protocollo HTTP diventa obsoleto a favore di HTTPS. Adobe Livefyre disattiverà completamente tutti i crittografia SSL/TLS HTTP e non sicuri entro la fine di agosto 2018. Si tratta di un Adobe Standard progettato per proteggere la privacy dell'utente e degli utenti.

## Chi è interessato? {#section_jf2_4yz_kcb}

Questo potrebbe avere un impatto sui clienti Livefyre che hanno:

* Chiamate server-to-server da CRM, CMS, WordPress o altro client.
* Integrazioni mobili (app Android e iOS)
* Applicazioni personalizzate o codice personalizzato

## Cosa devo fare? {#section_unv_dc5_kcb}

1. Tutti i clienti Livefyre devono comunicare con tutte le API tramite HTTPS per tutto il traffico, inclusi:

   * Integrazioni tra server (CRM, CMS, WordPress, ecc.)
   * Integrazioni mobili (app Android e iOS)
   * Applicazioni personalizzate (Streamhub SDK o direttamente codificate).

1. I client HTTP Server e Mobile devono supportare TLS 1.2
1. Cambia i nomi host da `{*}.<network>.fyre.co` a `<network>.{*}.fyre.co`. Ad esempio, il nome host `example.network.fyre.co` diventa `network.`example.fyre.co". Ad esempio:

   * `bootstrap.<network_name>.fyre.co` in `<network_name>.bootstrap.fyre.co`

   * `quill.<network_name>.fyre.co` in `<network_name>.quill.fyre.co`

   * `admin.<network_name>.fyre.co` in `<network_name>.admin.fyre.co`

## Come faccio a sapere se ho effettuato le modifiche? {#section_sqk_5d5_kcb}

Potete già utilizzare HTTPS, ma Livefyre consiglia di eseguire un doppio controllo, soprattutto se si dispone di:

* Chiamate server-to-server da CMS o CRM.
* Codice personalizzato o usa SDK per app personalizzate in JavaScript o Mobile.
* Se l'integrazione ha più di un anno.
* Se la tecnologia presente nello stack è superiore a un anno.

Anche se utilizzate già HTTPS, dovete verificare che i client API supportino TLS 1.2.

## Come posso verificare che i miei client API supportino TLS 1.2? {#section_nd1_j25_kcb}

Una persona che lavora nello sviluppo del sito può:

* Identificare il software client.
* Identificate la versione.
* Leggete la documentazione per assicurarvi che il client API supporti TLS 1.2.
* Se necessario, attivate la modalità di debug.

## Supporto Java per TLS 1.2 {#section_lwn_rwk_ycb}

Le JVM Oracle e OpenJDK per Java 8 e versioni successive sono configurate per utilizzare TLS 1.2, per impostazione predefinita, per tutte le connessioni SSL. Se si utilizza Java 8 o versione successiva, non è necessario intraprendere alcuna azione aggiuntiva.

Gli utenti di Java 7 o versioni precedenti devono consultare la documentazione pubblica su come abilitare TLS 1.2.

## Perché è necessario cambiare i nomi degli host? {#section_d5q_p25_kcb}

Livefyre non dispone di certificati SSL sui `{*}.<network>.fyre.co` domini. La semplice modifica dell'URL in HTTPS interrompe l'applicazione.

## Devo effettuare l’aggiornamento all’ultima versione degli SDK Livefyre? {#section_dw5_s25_kcb}

No. È invece possibile applicare la patch al codice. Per applicare la patch al codice, è necessario modificare alcune stringhe statiche e ricreare il codice. Se il client HTTP non è aggiornato, sarà necessario aggiornare anche quello o utilizzare uno diverso.

## Quanto tempo ci vorrà? {#section_lgd_v25_kcb}

Il tempo richiesto dipende dalla configurazione. Se hai una semplice implementazione, la conferma potrebbe richiedere poco tempo. Se disponete di numerose personalizzazioni, dovrete testare e distribuire il codice aggiornato ai vostri server o alle nuove app negli App Store. Per risultati ottimali, si consiglia di eseguire un audit iniziale del lavoro in modo da poter pianificare qualsiasi lavoro a lungo termine.

## Qual è il calendario per completare questo lavoro? {#section_kgk_w25_kcb}

Livefyre disattiverà la porta 80 (HTTP) per i nostri servizi entro la fine di agosto 2018 e supporterà solo le connessioni a 443 (HTTPS). I browser e altri client che tentano di utilizzare HTTP avranno esito negativo.

## Quando devo finire questo lavoro? {#section_rvb_x25_kcb}

Tutti i clienti devono utilizzare HTTPS entro la fine di luglio 2018. Se non riesci a rispettare questa scadenza, contatta il nostro team all'indirizzo prioritysupport@livefyre.com.
