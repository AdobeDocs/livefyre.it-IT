---
description: Creare app Android con tecnologia Livefyre.
seo-description: Creare app Android con tecnologia Livefyre.
seo-title: Android SDK
solution: Experience Manager
title: Android SDK
uuid: 68793fa9-3ea1-4890-b36d-b631f1c6f7de
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Android SDK{#android-sdk}

Creare app Android con tecnologia Livefyre.

Utilizzate questa libreria per integrare i servizi Livefyre nella vostra app Android nativa. L'SDK [per Android](https://github.com/Livefyre/StreamHub-Android-SDK) Livefyre StreamHub offre un livello sottile attorno ai nostri comuni meccanismi API, basati sull'ambiente di sviluppo Gradle/Android Studio.

Livefyre fornisce anche un’app di esempio per [recensioni](https://github.com/Livefyre/StreamHub-iOS-Reviews-App) , in base a questo SDK.

Questo Android SDK Livefyre può essere utilizzato sia in Eclipse che in Android Studio.

>[!NOTE]
>
>Prima di installare l’SDK per Android Livefyre è necessario che nell’ambiente in uso sia installato l’SDK [per](https://developer.android.com/sdk/index.html) Android. Dovete includere anche alcuni pacchetti SDK Android aggiuntivi, come descritto nei documenti per sviluppatori Android &gt; .
>[Aggiunta di pacchetti SDK](https://developer.android.com/sdk/installing/adding-packages.html)

Utilizzate Android SDK Manager (disponibile dalla barra degli strumenti Android Studio o Eclipse) per installare tutti i pacchetti consigliati. Accertatevi anche di includere l'archivio del supporto Android.

## Eclipse {#section_dtm_slv_zz}

Per aggiungere l’SDK Livefyre Android al progetto in Eclipse:

1. Ottieni la versione più recente di [StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) da GitHub.
1. Iniziate con un progetto esistente o createne uno nuovo.
1. Per importare StreamHub-Android-SDK nell'area di lavoro, andate a **[!UICONTROL File > Import > General > Existing Project into Workspace]**.
1. Sfoglia e seleziona StreamHub-Android-SDK; dovrebbe ora essere visualizzato in Esplora pacchetti.
1. Fai clic con il pulsante destro del mouse sul progetto e seleziona **[!UICONTROL Properties,]** la scheda Android.
1. Nella sezione Libreria, seleziona **[!UICONTROL Add button,]** quindi StreamHub-Android-SDK dall'elenco delle librerie.
1. Fate clic su **[!UICONTROL Apply]** e **[!UICONTROL OK]**.

## Android Studio {#section_vpw_klv_zz}

Per aggiungere Livefyre Android SDK al progetto in Android Studio:

1. Ottieni la versione più recente di [StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) da GitHub.
1. Iniziate con un progetto esistente o createne uno nuovo.
1. Fai clic con il pulsante destro del mouse sul progetto e seleziona **[!UICONTROL Open Module Settings]**.
1. Selezionare il **[!UICONTROL +]** pulsante nell'angolo superiore sinistro della finestra.
1. Selezionate **[!UICONTROL Import Existing Project.]** (nella nuova versione di Android studio, si trova **[!UICONTROL Import Existing Project]** sotto **[!UICONTROL More Modules]**).

1. Sfoglia e seleziona StreamHub-Android-SDK.

Android Studio potrebbe richiedere la conversione dell’SDK in versione gradle; in tal caso, selezionate **[!UICONTROL next]** quindi **[!UICONTROL finish]**.

Andate alla cartella **progetto &gt; cartella app &gt; file build.gradle** in dipendenze per aggiungere la seguente dipendenza:

```
dependencies {   compile project(':streamHubAndroidSDK') } 
```

Accertatevi che la riga seguente sia nella cartella **del progetto &gt; file settings.gradle** :

```
include ':streamHubAndroidSDK' 
```

>[!NOTE]
>
>È possibile personalizzare le configurazioni dall'interno di Config.java.

## Client {#section_yfq_blv_zz}

L’SDK per Android StreamHub espone diverse classi client che possono essere utilizzate per richiedere gli endpoint API Livefyre:

* **AdminClient** Exchange un token di autenticazione utente per informazioni utente, chiavi e altri metadati.

* **BootstrapClient** Ottenete contenuto recente e metadati su una raccolta particolare.

* **StreamClient** Consente di analizzare un flusso per una raccolta per recuperare contenuto nuovo, aggiornato ed eliminato.

* **WriteClient** Post, flag e contenuti simili in una raccolta.

