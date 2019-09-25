---
description: Aggiungi Livefyre alle tue app mobili native.
seo-description: Aggiungi Livefyre alle tue app mobili native.
seo-title: Kit di sviluppo software per dispositivi mobili (Mobile SDK)
solution: Experience Manager
title: Kit di sviluppo software per dispositivi mobili (Mobile SDK)
uuid: 84c7ca1c-3401-492a-bfa5-62b996947a44
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# SDK per dispositivi mobili{#mobile-sdks}

Aggiungi Livefyre alle tue app mobili native.

Sono disponibili diverse opzioni per le implementazioni per dispositivi mobili, a seconda dell’entità di personalizzazione che pianificate di eseguire:

* App Web per dispositivi mobili
* SDK Livefyre Android o iOS
* API HTTP

## App Web per dispositivi mobili {#section_t2k_vpb_11b}

I clienti che aprono una pagina Web su un dispositivo mobile ricevono automaticamente un flusso di contenuti Livefyre ottimizzato per i dispositivi mobili, compreso lo stile per adattarlo alle dimensioni ridotte dello schermo e le modifiche per gestire gli eventi di tocco.

>[!NOTE]
>
>Quando si utilizza un'app Livefyre in una visualizzazione Web Android, il parametro Android [WebSettings.setDomStorageEnabled](https://developer.android.com/reference/android/webkit/WebSettings.html) deve essere impostato su true. Se localStorage non è abilitato, Livefyre non sarà in grado di registrare un utente nell'app Livefyre.

Per ottimizzare l'app per dispositivi mobili, Livefyre limita le funzioni Commenti, Blog dal vivo e App chat impostate in modo da includere:

* Post
* Modificare      
* Contrassegna
* Mi piace
* Rispondi
* Numero listener
* Conteggio commenti
* Moderazione in sospeso in linea
* Hovercard
* Commenti principali
* Thread sensibili
* Commenti coda

Nelle app Web per dispositivi mobili, facendo clic sul nome di un autore si aprono le informazioni del carrello in una nuova pagina.

## Livefyre Android SDK o iOS SDK {#section_zdz_spb_11b}

Livefyre fornisce anche due SDK per dispositivi mobili: un SDK iOS e un SDK Android. Questi SDK sono racchiusi intorno ai nostri endpoint HTTP, creati per fornire un metodo più semplice per inviare e ricevere dati. Con questi SDK non viene fornita alcuna interfaccia, per una maggiore flessibilità nella visualizzazione e nell'utilizzo del contenuto all'interno dell'app mobile.

Gli SDK per Android e iOS supportano le seguenti funzionalità per Commenti, Blog dal vivo e Chat:

| Funzioni iOS: | Funzioni Android: |
|--- |--- |
| <ul><li> Post </li><li>Modificare       </li><li>Contrassegna </li><li>Mi piace </li><li>Rispondi </li><li>Thread sensibili</li></ul> | <ul><li>Post </li><li>Modificare       </li><li>Mi piace </li><li>Rispondi </li><li>Thread sensibili</li></ul> |

## API HTTP {#section_yqb_qpb_11b}

Le API HTTP sono il gruppo di endpoint che consente di creare conversazioni e contenuti sulla piattaforma Livefyre. Inoltre, alimenta tutti i flussi di Livefyre. Sebbene questa soluzione richieda più tempo per lo sviluppo da parte del team di progettazione, offre maggiore flessibilità quando si utilizza la suite di prodotti Livefyre e consente l'integrazione mobile nativa.

>[!IMPORTANT]
>
>**Non** create token di autenticazione utente all'interno del client mobile, perché ciò richiederebbe l'esposizione della chiave di rete segreta Livefyre all'interno di un'app non protetta. Per una soluzione più solida e sicura, consultate la sezione Token di autenticazione utente.

