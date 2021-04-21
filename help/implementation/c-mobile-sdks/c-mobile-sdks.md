---
description: Aggiungi Livefyre alle tue app mobile native.
title: Kit di sviluppo software per dispositivi mobili (Mobile SDK)
exl-id: e05001a4-6199-4d98-a661-123e031b657b
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 4%

---

# SDK per dispositivi mobili{#mobile-sdks}

Aggiungi Livefyre alle tue app mobile native.

Sono disponibili diverse opzioni per le implementazioni per dispositivi mobili, a seconda dell’estensione della personalizzazione che intendi effettuare:

* App web per dispositivi mobili
* SDK per Livefyre Android o iOS
* API HTTP

## App web mobili {#section_t2k_vpb_11b}

I clienti che aprono una pagina web su un dispositivo mobile ricevono automaticamente uno streaming di contenuti Livefyre ottimizzato per i dispositivi mobili, compreso lo stile per adattarlo alle dimensioni ridotte dello schermo e le modifiche per gestire gli eventi touch.

>[!NOTE]
>
>Quando si utilizza un&#39;app Livefyre in una WebView Android, il parametro Android [WebSettings.setDomStorageEnabled](https://developer.android.com/reference/android/webkit/WebSettings.html) deve essere impostato su true. Se localStorage non è abilitato, Livefyre non sarà in grado di registrare un utente nell’app Livefyre.

Per ottimizzare per i dispositivi mobili, Livefyre limita le funzioni Commenti, Blog in tempo reale e App chat impostate per includere:

* Post
* Modificare      
* Contrassegna
* Mi piace
* Rispondi
* Conteggio listener
* Conteggio commenti
* Moderazione in sospeso in linea
* Hovercard
* Commenti principali
* Thread caldi
* Commenti coda

Nelle app Web per dispositivi mobili, quando si fa clic sul nome di un autore vengono visualizzate le informazioni relative ai biglietti da visita in una nuova pagina.

## SDK per Livefyre Android o SDK per iOS {#section_zdz_spb_11b}

Livefyre fornisce anche due SDK per dispositivi mobili: un SDK per iOS e un SDK per Android. Questi SDK sono wrapper intorno ai nostri endpoint HTTP, costruiti per fornire un metodo più semplice per inviare e ricevere i dati. Non viene fornita alcuna interfaccia con questi SDK, che consentono una maggiore flessibilità nella visualizzazione e nell’utilizzo del contenuto all’interno dell’app mobile.

Gli SDK per Android e iOS supportano le seguenti funzioni per Commenti, Blog live e Chat:

| Funzioni di iOS: | Funzioni Android: |
|--- |--- |
| <ul><li> Post </li><li>Modificare       </li><li>Contrassegna </li><li>Mi piace </li><li>Rispondi </li><li>Thread caldi</li></ul> | <ul><li>Post </li><li>Modificare       </li><li>Mi piace </li><li>Rispondi </li><li>Thread caldi</li></ul> |

## API HTTP {#section_yqb_qpb_11b}

Le API HTTP sono il gruppo di endpoint che ti consente di creare conversazioni e contenuti sulla piattaforma Livefyre. Alimenta anche tutti i flussi di Livefyre fuori dagli schemi. Sebbene questa soluzione richieda più tempo per lo sviluppo per il team di progettazione, offre maggiore flessibilità quando si utilizza la suite di prodotti Livefyre e consente l’integrazione nativa per dispositivi mobili.

>[!IMPORTANT]
>
>**Non** creare token di autenticazione utente all’interno del client mobile, perché questo richiederebbe l’esposizione della chiave di rete segreta Livefyre all’interno di un’app non protetta. Per una soluzione più solida e sicura, consulta la sezione Token di autenticazione utente .
