---
description: Aggiungi Livefyre all'app iOS nativa.
seo-description: Aggiungi Livefyre all'app iOS nativa.
seo-title: Livefyre iOS SDK
solution: Experience Manager
title: Livefyre iOS SDK
uuid: bfdef31a-49fc-4b25-b0c5-300f27067302
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre iOS SDK{#livefyre-ios-sdk}

Aggiungi Livefyre all'app iOS nativa.

Utilizzate questa libreria open-source per integrare i servizi Livefyre nell'app iOS nativa. Livefyre StreamHub iOS SDK fornisce un livello sottile intorno ai nostri comuni meccanismi API, sulla base dell'eccellente libreria AFNetworking.

Livefyre fornisce anche due app di esempio iOS basate su questo SDK: un flusso di commenti e un'app di esempio per le recensioni

## Integrazione dell’SDK nel progetto come contenitore Cocoa (consigliato) {#section_qc5_h3v_zz}

Il modo più conveniente per aggiungere l’SDK StreamHub-iOS al progetto è utilizzare CocoaPods. Se non disponete di CocoaPods, eseguite i cocodec di installazione di Gem e la configurazione del contenitore. Di seguito è riportato un esempio di file di profilo:

```
source 'https://github.com/Livefyre/cocoapods.git' 
source 'https://github.com/CocoaPods/Specs.git' 
  
platform :ios, :deployment_target => '6.0' 
  
pod 'StreamHub-iOS-SDK', '~> 0.3.0'
```

Sarà inoltre necessario aggiungere un repository di specifiche al vostro CocoaPod installazione (questo lo clonerà in `~/.cocoapods/repos` directory):

```
pod repo add livefyre https://github.com/Livefyre/cocoapods.git
```

Dopo aver creato il file Podfile nella directory principale del progetto dell'app e aver aggiunto l'archivio, esegui:

```
pod install
```

Questo scaricherà tutte le dipendenze e creerà un file MyApp.xcworkspace, che dovrebbe essere utilizzato da ora in poi per aprire il progetto dell'app in Xcode.

## Come progetto secondario Xcode {#section_jcm_g3v_zz}

In alternativa, duplicare il repository:

```
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
```

Quindi, aggiungete il progetto Xcode (LFSClient.xcodeproj) all’app come sottoprogetto (facilmente eseguendo semplicemente il trascinamento del file LFSClient.xcodeproj nel riquadro Navigatore progetti in Xcode).

Sarà inoltre necessario fare lo stesso con qualsiasi delle dipendenze ([AFNetworking](https://github.com/AFNetworking/AFNetworking), [JSONKit](https://github.com/escherba/JSONKit)).

## Scarica tutto contemporaneamente (non consigliato) {#section_rpb_f3v_zz}

```
cd ~/dev 
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
cd StreamHub-iOS-SDK 
git submodule init 
git submodule update 
pod repo add livefyre https://github.com/Livefyre/cocoapods.git 
pod install 
cd examples/CommentStream 
pod install 
open CommentStream.xcworkspace
```

>[!NOTE]
>
>Per eseguire i test in Xcode 6, è necessario aggiungere $(PLATFORM_DIR)/Developer/Library/Frameworks a FRAMEWORK_SEARCH_PATHS in Pods-test-XCTest+OHHTTPStubSuiteCleanUp[podhttps://stackoverflow.com/a/24651704](https://stackoverflow.com/a/24651704).

È necessario un file LFSTestConfig.plist da Livefyre, fornito da Livefyre su richiesta.

## Documentazione Xcode {#section_arl_b3v_zz}

È possibile consultare la [documentazione](https://livefyre.github.com/StreamHub-iOS-SDK/) o creare la destinazione "Documentazione" nel codice Xcode (richiede l'installazione di appledoc) nel sistema.

## Requisiti {#section_m5l_13v_zz}

Le versioni SDK di StreamHub per iOS dalla versione v0.2.0 richiedono iOS 6.0 o successiva.

## Appendice (supporto JSON) {#section_pcd_5hv_zz}

Per coloro che guardano gli internali dell’SDK StreamHub-iOS, tenete presente che utilizzeremo una versione modificata di [JSONKit](https://github.com/escherba/JSONKit) come parser JSON predefinito (invece di NSJSONSerialization fornito da Apple). Abbiamo dovuto farlo perché il parser fornito da Apple non supporta la decodifica di file JSON contenenti numeri interi o a virgola mobile più grandi di quelli che possono essere rappresentati dal sistema. La nostra versione modificata di JSONKit tronca i numeri molto grandi al corrispondente massimo del sistema, invece di gettare un'eccezione.
