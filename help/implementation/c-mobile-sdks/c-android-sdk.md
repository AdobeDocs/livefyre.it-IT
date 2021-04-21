---
description: Crea app Android con tecnologia Livefyre.
title: Android SDK
exl-id: 54ea6537-5f27-4174-af25-d17257f23e48
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# Android SDK{#android-sdk}

Crea app Android con tecnologia Livefyre.

Utilizza questa libreria per integrare i servizi Livefyre nella tua app nativa Android. L’ [Livefyre StreamHub Android SDK](https://github.com/Livefyre/StreamHub-Android-SDK) fornisce un livello sottile intorno ai nostri comuni meccanismi API, in base all’ambiente di sviluppo Gradle/Android Studio.

Livefyre fornisce anche un&#39;app di esempio [Reviews](https://github.com/Livefyre/StreamHub-iOS-Reviews-App), basata su questo SDK.

Questo SDK per Android Livefyre può essere utilizzato sia in Eclipse che in Android Studio.

>[!NOTE]
>
>Prima di installare l&#39;SDK per Android Livefyre è necessario che nel tuo ambiente sia installato [Android SDK](https://developer.android.com/sdk/index.html) . Devi includere anche alcuni pacchetti SDK Android aggiuntivi, come descritto nei documenti per sviluppatori Android > .
>[Aggiunta di pacchetti SDK](https://developer.android.com/sdk/installing/adding-packages.html)

Utilizza Android SDK Manager (disponibile dalla barra degli strumenti Android Studio o Eclipse) per installare tutti i pacchetti consigliati. Accertati di includere anche l’archivio del supporto Android.

## Eclipse {#section_dtm_slv_zz}

Per aggiungere Livefyre Android SDK al tuo progetto in Eclipse:

1. Scarica la versione più recente [StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) da GitHub.
1. Inizia con un progetto esistente o creane uno nuovo.
1. Per importare l’SDK di StreamHub-Android-nell’area di lavoro, vai a **[!UICONTROL File > Import > General > Existing Project into Workspace]**.
1. Sfoglia e seleziona StreamHub-Android-SDK; dovrebbe ora essere visualizzato nell&#39;explorer del pacchetto.
1. Fai clic con il pulsante destro del mouse sul progetto e seleziona **[!UICONTROL Properties,]** , quindi la scheda Android .
1. Nella sezione Libreria, seleziona **[!UICONTROL Add button,]** , quindi seleziona StreamHub-Android-SDK dall’elenco delle librerie.
1. Fai clic su **[!UICONTROL Apply]** e **[!UICONTROL OK]**.

## Android Studio {#section_vpw_klv_zz}

Per aggiungere Livefyre Android SDK al tuo progetto in Android Studio:

1. Scarica la versione più recente [StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) da GitHub.
1. Inizia con un progetto esistente o creane uno nuovo.
1. Fai clic con il pulsante destro del mouse sul progetto e seleziona **[!UICONTROL Open Module Settings]**.
1. Seleziona il pulsante **[!UICONTROL +]** nell’angolo in alto a sinistra della finestra.
1. Seleziona **[!UICONTROL Import Existing Project.]** (Nella nuova versione di Android Studio, è possibile trovare **[!UICONTROL Import Existing Project]** in **[!UICONTROL More Modules]**).

1. Sfoglia e seleziona StreamHub-Android-SDK.

Android Studio potrebbe richiedere la conversione dell&#39;SDK in versione gradle; in questo caso, selezionare **[!UICONTROL next]**, quindi **[!UICONTROL finish]**.

Vai al file **project folder > app folder > build.gradle** sotto dipendenze per aggiungere la seguente dipendenza:

```
dependencies {   compile project(':streamHubAndroidSDK') } 
```

Assicurati che la seguente riga sia nel file **project folder > settings.gradle** :

```
include ':streamHubAndroidSDK' 
```

>[!NOTE]
>
>Puoi personalizzare le configurazioni da Config.java.

## Client {#section_yfq_blv_zz}

L’SDK per Android StreamHub espone diverse classi client che possono essere utilizzate per richiedere gli endpoint API Livefyre:

* **** AdminClientExchange un token di autenticazione utente per informazioni utente, chiavi e altri metadati.

* **** BootstrapClientOttieni contenuti recenti e metadati su una raccolta particolare.

* **** StreamClientPoll un flusso per una raccolta per recuperare contenuto nuovo, aggiornato ed eliminato.

* **** WriteClientPost, flag e contenuti simili in una raccolta.
