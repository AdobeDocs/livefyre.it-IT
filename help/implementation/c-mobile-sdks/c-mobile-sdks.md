---
description: Aggiungi Livefyre alle tue app mobili native.
seo-description: Aggiungi Livefyre alle tue app mobili native.
seo-title: SDK per dispositivi mobili
solution: Experience Manager
title: SDK per dispositivi mobili
uuid: 84 c 7 ca 1 c -3401-492 a-bfa 5-62 b 996947 a 44
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# SDK per dispositivi mobili{#mobile-sdks}

Aggiungi Livefyre alle tue app mobili native.

Per le implementazioni mobili sono disponibili diverse opzioni, a seconda dell&#39;ambito di personalizzazione che pianifica di effettuare:

* App Web per dispositivi mobili
* Livefyre Android o ios SDK
* API HTTP

## App Web per dispositivi mobili {#section_t2k_vpb_11b}

I clienti che aprono una pagina Web su un dispositivo mobile ricevono automaticamente un flusso di contenuto Livefyre ottimizzato per dispositivi mobili, incluso lo stile per adattarsi alle dimensioni ridotte dello schermo e alle modifiche per gestire gli eventi di tocco.

>[!NOTE]
>
>Quando utilizzate un&#39;app Livefyre in una visualizzazione Webid, il parametro Android [websettings. setdomstorageenabled](https://developer.android.com/reference/android/webkit/WebSettings.html) deve essere impostato su true. Se localstorage non è abilitato, Livefyre non sarà in grado di registrare un utente nell&#39;app Livefyre.

Per ottimizzare per i dispositivi mobili, Livefyre limita i commenti, il blog live e le funzionalità App chat impostate per:

* Post
* Modifica
* Flag
* Come
* Risposta
* Conteggio listener
* Conteggio commenti
* Moderazione in attesa in attesa
* Schede
* Commenti principali
* Hot Thread
* Commenti coda

Nelle app Web per dispositivi mobili, facendo clic sul nome di un autore vengono aperte le informazioni relative alla scheda hovercard in una nuova pagina.

## Livefyre Android SDK o iOS SDK {#section_zdz_spb_11b}

Livefyre fornisce anche due SDK per dispositivi mobili: un SDK per iOS e un Android SDK. Questi SDK avvolgono i nostri endpoint HTTP, creati per fornire un metodo più semplice per inviare e ricevere dati. Con questi SDK non viene fornita alcuna interfaccia, consentendo una flessibilità maggiore con la modalità di visualizzazione e utilizzo del contenuto nell&#39;app mobile.

Gli SDK per Android e iOS supportano le seguenti funzionalità per commenti, blog live e chat:

| Funzioni iOS: | Funzioni per Android: |
|--- |--- |
| <ul><li> Post </li><li>Modifica </li><li>Flag </li><li>Come </li><li>Risposta </li><li>Hot Thread</li></ul> | <ul><li>Post </li><li>Modifica </li><li>Come </li><li>Risposta </li><li>Hot Thread</li></ul> |

## API HTTP {#section_yqb_qpb_11b}

Le API HTTP sono il gruppo di endpoint che consente di creare conversazioni e contenuto sulla piattaforma Livefyre. Inoltre, consente a Livefyre di uscire dai flussi di caselle. Questa soluzione richiede un tempo di sviluppo maggiore dal team tecnico, offre una flessibilità maggiore quando si utilizza la suite di prodotti Livefyre e consente l&#39;integrazione nativa dei dispositivi mobili.

>[!IMPORTANT]
>
>**Non** create token di autenticazione utente all&#39;interno del client mobile, perché questo richiede che la chiave di rete segreta di Livefyre venga esposta all&#39;interno di un&#39;app non sicura. Per una soluzione più solida e sicura, consulta la sezione Token autenticazione utente.

