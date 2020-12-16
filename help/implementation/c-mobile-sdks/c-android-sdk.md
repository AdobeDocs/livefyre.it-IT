---
description: Creare app Android con tecnologia Livefyre.
seo-description: Creare app Android con tecnologia Livefyre.
seo-title: Android SDK
solution: Experience Manager
title: Android SDK
uuid: 68793fa9-3ea1-4890-b36d-b631f1c6f7de
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 1%

---


# Android SDK{#android-sdk}

Creare app Android con tecnologia Livefyre.

Utilizzate questa libreria per integrare i servizi Livefyre nella vostra app Android nativa. L&#39; [Livefyre StreamHub Android SDK](https://github.com/Livefyre/StreamHub-Android-SDK) offre un livello sottile intorno ai nostri comuni meccanismi API, basati sull&#39;ambiente di sviluppo Gradle/Android Studio.

Livefyre fornisce anche un&#39;app di esempio [Recensioni](https://github.com/Livefyre/StreamHub-iOS-Reviews-App), in base a questo SDK.

Questo Android SDK Livefyre può essere utilizzato sia in Eclipse che in Android Studio.

>[!NOTE]
>
>Prima di installare l’SDK Livefyre per Android, nell’ambiente in uso deve essere installato [Android SDK](https://developer.android.com/sdk/index.html). Dovete includere anche alcuni pacchetti SDK per Android aggiuntivi, come descritto nei documenti per sviluppatori Android > .
>[Aggiunta di pacchetti SDK](https://developer.android.com/sdk/installing/adding-packages.html)

Utilizzate Android SDK Manager (disponibile dalla barra degli strumenti Android Studio o Eclipse) per installare tutti i pacchetti consigliati. Accertatevi anche di includere l&#39;archivio del supporto Android.

## Eclipse {#section_dtm_slv_zz}

Per aggiungere l’SDK Livefyre Android al progetto in Eclipse:

1. Ottenete la versione più recente di [StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) da GitHub.
1. Iniziate con un progetto esistente o createne uno nuovo.
1. Per importare StreamHub-Android-SDK nell&#39;area di lavoro, andate a **[!UICONTROL File > Import > General > Existing Project into Workspace]**.
1. Sfoglia e seleziona StreamHub-Android-SDK; dovrebbe ora essere visualizzato in Esplora pacchetti.
1. Fai clic con il pulsante destro del mouse sul progetto e seleziona **[!UICONTROL Properties,]**, quindi la scheda Android.
1. Nella sezione Libreria, selezionate **[!UICONTROL Add button,]**, quindi selezionate StreamHub-Android-SDK dall&#39;elenco delle librerie.
1. Fare clic su **[!UICONTROL Apply]** e **[!UICONTROL OK]**.

## Android Studio {#section_vpw_klv_zz}

Per aggiungere l’SDK Livefyre Android al progetto in Android Studio:

1. Ottenete la versione più recente di [StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) da GitHub.
1. Iniziate con un progetto esistente o createne uno nuovo.
1. Fare clic con il pulsante destro del mouse sul progetto e selezionare **[!UICONTROL Open Module Settings]**.
1. Selezionare il pulsante **[!UICONTROL +]** nell&#39;angolo superiore sinistro della finestra.
1. Selezionare **[!UICONTROL Import Existing Project.]** (nella nuova versione dello studio Android, è possibile trovare **[!UICONTROL Import Existing Project]** in **[!UICONTROL More Modules]**.)

1. Sfoglia e seleziona StreamHub-Android-SDK.

Android Studio potrebbe richiedere la conversione dell’SDK in versione gradle; in tal caso, selezionare **[!UICONTROL next]** quindi **[!UICONTROL finish]**.

Andate alla **cartella di progetto > cartella dell&#39;app > file build.gradle** sotto le dipendenze per aggiungere la seguente dipendenza:

```
dependencies {   compile project(':streamHubAndroidSDK') } 
```

Accertatevi che la seguente riga sia presente nella cartella **del progetto > settings.gradle** file:

```
include ':streamHubAndroidSDK' 
```

>[!NOTE]
>
>È possibile personalizzare le configurazioni dall&#39;interno di Config.java.

## Client {#section_yfq_blv_zz}

L’SDK per Android StreamHub espone diverse classi client che possono essere utilizzate per richiedere gli endpoint API Livefyre:

* **** AdminClientExchange un token di autenticazione utente per informazioni utente, chiavi e altri metadati.

* **** BootstrapClientOttenete contenuti recenti e metadati su una raccolta particolare.

* **** StreamClientSondaggio di un flusso per una raccolta per recuperare contenuto nuovo, aggiornato ed eliminato.

* **WriteClientPost, flag e contenuti simili in una raccolta.** 

