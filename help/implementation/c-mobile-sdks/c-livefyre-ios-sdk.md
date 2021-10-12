---
description: Aggiungi Livefyre alla tua app nativa iOS.
title: SDK per Livefyre iOS
exl-id: 961c41dc-fee8-480c-a189-a20a689e705f
source-git-commit: 3091db9d7b9611e26ad65c1432856c9465694e92
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# SDK per Livefyre iOS{#livefyre-ios-sdk}

Aggiungi Livefyre alla tua app nativa iOS.

Utilizza questa libreria open-source per integrare i servizi Livefyre nella tua app nativa iOS. L’SDK di Livefyre StreamHub iOS fornisce un livello sottile intorno ai nostri comuni meccanismi API, basato sull’eccellente libreria AFNetworking.

Livefyre fornisce anche due app di esempio di iOS in base a questo SDK: un flusso di commenti e un’app di esempio per le revisioni.

## Integrazione dell’SDK nel progetto come contenitore di cacao (consigliato) {#section_qc5_h3v_zz}

Il modo più conveniente per aggiungere l’SDK StreamHub-iOS al tuo progetto è quello di utilizzare CocoaPods. Se non hai CocoaPods, esegui l’installazione dei cococoapods e la configurazione del pod. Ecco un esempio di Podfile :

```
source 'https://github.com/Livefyre/cocoapods.git' 
source 'https://github.com/CocoaPods/Specs.git' 
  
platform :ios, :deployment_target => '6.0' 
  
pod 'StreamHub-iOS-SDK', '~> 0.3.0'
```

Sarà inoltre necessario aggiungere un archivio delle specifiche all&#39;installazione di CocoaPod (questo lo clonerà nella directory `~/.cocoapods/repos`):

```
pod repo add livefyre https://github.com/Livefyre/cocoapods.git
```

Una volta creato il Podfile nella directory principale del progetto dell&#39;app e nell&#39;archivio qui sopra aggiunto, esegui:

```
pod install
```

Questo scarica tutte le dipendenze e crea un file MyApp.xcworkspace, che devi utilizzare da ora in poi per aprire il progetto dell&#39;app in Xcode.

## Come sottoprogetto Xcode {#section_jcm_g3v_zz}

In alternativa, duplica l’archivio:

```
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
```

Quindi, aggiungi il progetto Xcode (LFSClient.xcodeproj) all’app come sottoprogetto (facilmente eseguibile trascinando il file LFSClient.xcodeproj nel riquadro Navigatore progetti in Xcode).

Sarà inoltre necessario fare lo stesso con una qualsiasi delle dipendenze ([AFNetworking](https://github.com/AFNetworking/AFNetworking), [JSONKit](https://github.com/escherba/JSONKit)).

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
>Per eseguire i test in Xcode 6, devi aggiungere $(PLATFORM_DIR)/Developer/Library/Frframework a FRAMEWORK_SEARCH_PATHS in Pods-test-XCTest+OHHTTPStubSuiteCleanUp pod[https://stackoverflow.com/a/24651704](https://stackoverflow.com/a/24651704).

Hai bisogno del file LFSTestConfig.plist da Livefyre, che Livefyre fornisce su richiesta.

## Documentazione su Xcode {#section_arl_b3v_zz}

È possibile sfogliare la [documentazione](https://github.com/Livefyre/StreamHub-iOS-SDK) oppure creare la destinazione &quot;Documentazione&quot; nel codice Xcode (richiede l&#39;installazione di appledoc) sul sistema.

## Requisiti {#section_m5l_13v_zz}

Le versioni SDK di StreamHub iOS a partire dalla versione v0.2.0 richiedono iOS 6.0 o versioni successive.

## Appendice (supporto JSON) {#section_pcd_5hv_zz}

Per coloro che guardano gli internali dell’SDK StreamHub-iOS, tieni presente che utilizziamo una versione modificata di [JSONKit](https://github.com/escherba/JSONKit) come parser JSON predefinito (invece di NSJSONSerialization fornito da Apple). È stato necessario farlo perché il parser fornito da Apple non supporta la decodifica di file JSON contenenti numeri interi o a virgola mobile maggiori di quelli che possono essere rappresentati dal sistema. La nostra versione modificata di JSONKit tronca numeri molto grandi al corrispondente massimo del sistema, invece di generare un&#39;eccezione.
