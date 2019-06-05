---
description: nulle
seo-description: nulle
seo-title: SSL Enforcement
solution: Experience Manager
title: SSL Enforcement
uuid: e 64 af 8 c 2-3 ab 6-4034-b 385-0 e 552 d 828 c 6 e
translation-type: tm+mt
source-git-commit: 7dc3ac6725a27460cecfa6051549da85370ca053

---


# SSL Enforcement{#ssl-enforcement}

Per assicurare che i dati rimangano protetti, non si verifica più l&#39;errore HTTP a favore di HTTPS. Adobe Livefyre disabiliterà completamente i cifrer HTTP e SSL/TLS non sicuri alla fine di agosto 2018. Questo è un Adobe Standard progettato per proteggere la privacy di voi e dei vostri utenti.

## Chi è interessato? {#section_jf2_4yz_kcb}

Questo potrebbe interessare i clienti Livefyre che hanno:

* Chiamate server-to-server dai propri CRM, CMS, wordpress o altro client.
* Integrazioni per dispositivi mobili (app Android e iOS)
* Applicazioni personalizzate o codice personalizzato

## Cosa devo fare? {#section_unv_dc5_kcb}

1. Tutti i clienti Livefyre devono comunicare con tutte le API tramite HTTPS per tutto il traffico, incluso:

   * Server to Server Integrations (CRM, CMS, wordpress, etc.)
   * Integrazioni per dispositivi mobili (app Android e iOS)
   * Applicazioni personalizzate (Streamhub SDK o direttamente codificate).

1. Server to Server and Mobile HTTP Client must support TLS 1.2
1. Change hostnames from `{*}.<network>.fyre.co` to `<network>.{*}.fyre.co`. Ad esempio, il nome host `example.network.fyre.co` diventa `network.`example. fyre. co &quot;. Ad esempio:

   * `bootstrap.<network_name>.fyre.co` a `<network_name>.bootstrap.fyre.co`

   * `quill.<network_name>.fyre.co` a `<network_name>.quill.fyre.co`

   * `admin.<network_name>.fyre.co` a `<network_name>.admin.fyre.co`

## Come faccio per sapere se le modifiche sono state apportate? {#section_sqk_5d5_kcb}

Potresti già usare HTTPS, ma Livefyre consiglia di controllare due volte, soprattutto se hai:

* Chiamate server-to-server dal CMS o CRM.
* Codice personalizzato o usa SDK per app personalizzate in Javascript o Mobile.
* Se l&#39;integrazione è superiore a un anno precedente.
* Se la tecnologia dello stack è precedente a un anno.

Anche se utilizzi già HTTPS, devi verificare che i client API supportino TLS 1.2.

## Come posso verificare che i client API supportino TLS 1.2? {#section_nd1_j25_kcb}

Gli utenti che lavorano allo sviluppo del sito possono:

* Identificare il software client.
* Identificare la versione.
* Leggi la documentazione per verificare che il client API supporti TLS 1.2.
* Se necessario, attiva la modalità di debug.

## Supporto Java per TLS 1.2 {#section_lwn_rwk_ycb}

Per tutte le connessioni SSL, Oracle e openjdk jvms per Java 8 e versioni successive sono configurati per utilizzare TLS 1.2. Non è necessario intraprendere ulteriori azioni se si utilizza Java 8 o versione successiva.

Gli utenti di Java 7 o versioni precedenti devono consultare la documentazione pubblica su come abilitare TLS 1.2.

## Perché devo cambiare i nomi degli host? {#section_d5q_p25_kcb}

Livefyre non dispone di certificati SSL sui `{*}.<network>.fyre.co` domini. Se si modifica semplicemente l&#39;URL in HTTPS, l&#39;applicazione viene interrotta.

## Devo effettuare l&#39;aggiornamento all&#39;ultima versione degli SDK di Livefyre? {#section_dw5_s25_kcb}

No. È invece possibile riparare il codice. Per riparare il codice, modificate alcune stringhe statiche e ricreate il codice. Se il client HTTP non è aggiornato, dovrete aggiornarlo anche o utilizzarne uno diverso.

## Quanto tempo sarà necessario per questa operazione? {#section_lgd_v25_kcb}

Il tempo necessario dipende dalla configurazione. Se si dispone di una semplice implementazione, il tempo richiesto dovrebbe richiedere poco tempo. Se avete numerose personalizzazioni, dovrete sottoporre a test e distribuire il codice aggiornato sui server o sulle nuove app agli App Store. Per risultati ottimali, è consigliabile eseguire un controllo iniziale del lavoro, in modo da pianificare un lavoro a più condizioni.

## Qual è la timeline per completare il lavoro? {#section_kgk_w25_kcb}

Livefyre disabiliterà la porta 80 (HTTP) ai nostri servizi entro la fine di agosto 2018 e supporterà solo le connessioni a 443 (HTTPS). I browser e altri client, che tentano di utilizzare HTTP, non riescono.

## Quando devo terminare questo lavoro? {#section_rvb_x25_kcb}

Tutti i clienti devono utilizzare HTTPS entro la fine di luglio 2018. Se non riuscite a rispettare questa scadenza, contattate il nostro team all&#39;indirizzo prioritysupport@livefyre.com.
