---
description: Creare app Android basate su Livefyre.
seo-description: Creare app Android basate su Livefyre.
seo-title: Android SDK
solution: Experience Manager
title: Android SDK
uuid: 68793 fa 9-3 ea 1-4890-b 36 d-b 631 f 1 c 6 f 7 de
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Android SDK{#android-sdk}

Creare app Android basate su Livefyre.

Utilizzate questa libreria per integrare i servizi Livefyre nell&#39;app Android nativa. [Livefyre streamhub Android SDK](https://github.com/Livefyre/StreamHub-Android-SDK) fornisce un livello sottile intorno ai nostri meccanismi API comuni, basati sull&#39;ambiente di sviluppo di Gradle/Android Studio.

Livefyre fornisce anche un [&#39;app](https://github.com/Livefyre/StreamHub-iOS-Reviews-App) di esempio Reviews, basata su questo SDK.

Questo SDK di Livefyre Android può essere usato sia in Eclipse che in Android Studio.

>[!NOTE]
>
>Prima di installare l&#39;SDK di Livefyre per Android devi disporre dell&#39;SDK [Android](https://developer.android.com/sdk/index.html) installato nell&#39;ambiente. Dovete includere anche alcuni pacchetti Android SDK aggiuntivi, come descritto nei documenti per sviluppatori Android.
>[Aggiunta di pacchetti SDK](https://developer.android.com/sdk/installing/adding-packages.html)

Utilizzate Android SDK Manager (disponibile dalla barra degli strumenti di Android Studio o Eclipse) per installare tutti i pacchetti raccomandati. Assicuratevi di includere anche l&#39;archivio di supporto Android.

## Eclipse {#section_dtm_slv_zz}

Per aggiungere l&#39;SDK di Livefyre Android al progetto in Eclipse:

1. Ottenete l&#39;ultimo [streamhub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) da github.
1. Iniziate con un progetto esistente o createne uno nuovo.
1. Per importare l&#39;SDK streamhub-Android-SDK nell&#39;area di lavoro **[!UICONTROL File > Import > General > Existing Project into Workspace]**.
1. Sfogliate e selezionate streamhub-Android-SDK; dovrebbe essere visualizzato in Esplora pacchetti.
1. Fai clic con il pulsante destro del mouse sul progetto e seleziona **[!UICONTROL Properties,]** la scheda Android.
1. Nella sezione Libreria, seleziona **[!UICONTROL Add button,]** quindi streamhub-Android-SDK dall&#39;elenco delle librerie.
1. Fate clic su **[!UICONTROL Apply]** e **[!UICONTROL OK]**.

## Android Studio {#section_vpw_klv_zz}

Per aggiungere l&#39;SDK di Livefyre Android al tuo progetto in Android Studio:

1. Ottenete l&#39;ultimo [streamhub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) da github.
1. Iniziate con un progetto esistente o createne uno nuovo.
1. Fai clic con il pulsante destro del mouse sul progetto e seleziona **[!UICONTROL Open Module Settings]**.
1. Selezionate il **[!UICONTROL +]** pulsante nell&#39;angolo in alto a sinistra della finestra.
1. Seleziona **[!UICONTROL Import Existing Project.]** (in nuova versione di Android Studio, puoi trovarlo **[!UICONTROL Import Existing Project]** . **[!UICONTROL More Modules]**)

1. Individua e seleziona streamhub-Android-SDK.

Android Studio potrebbe richiedere di convertire l&#39;SDK in una versione gradle; Se ciò si verifica, seleziona **[!UICONTROL next]** quindi **[!UICONTROL finish]**.

Andate alla **cartella del progetto &gt; cartella dell&#39;app &gt; build. gradle** in dipendenze per aggiungere la seguente dipendenza:

```
dependencies {   compile project(':streamHubAndroidSDK') } 
```

Accertatevi che la riga seguente sia presente nella cartella **del progetto &gt; settings. gradle** :

```
include ':streamHubAndroidSDK' 
```

>[!NOTE]
>
>Potete personalizzare le configurazioni dall&#39;interno di Config. java.

## Client {#section_yfq_blv_zz}

L&#39;SDK streamhub Android espone diverse classi client che possono essere utilizzate per richiedere endpoint API di Livefyre:

* **Adminclient** Exchange un token di autenticazione utente per informazioni utente, chiavi e altri metadati.

* **Bootstrapclient** : consente di ottenere contenuto recente e metadati su una particolare raccolta.

* **Streamclient** Poll un flusso per una raccolta per recuperare contenuti nuovi, aggiornati ed eliminati.

* **Writeclient** Post, flag, and like content in a Collection.

