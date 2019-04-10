---
description: Aggiungete Livefyre alla vostra app iOS nativa.
seo-description: Aggiungete Livefyre alla vostra app iOS nativa.
seo-title: Livefyre iOS SDK
solution: Experience Manager
title: Livefyre iOS SDK
uuid: bfdef 31 a -49 fc -4 b 25-b 0 c 5-300 f 27067302
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Livefyre iOS SDK{#livefyre-ios-sdk}

Aggiungete Livefyre alla vostra app iOS nativa.

Utilizzate questa libreria open-source per integrare i servizi Livefyre nell'app iOS nativa. Livefyre streamhub iOS SDK fornisce un livello sottile intorno ai nostri meccanismi API comuni, basati sulla libreria afnetworking eccellente.

Livefyre fornisce anche due app di esempio iOS basate su questo SDK: un flusso commenti e un'app di esempio di revisione.

## Integrazione dell'SDK nel progetto come contenitore Cocoa (consigliato) {#section_qc5_h3v_zz}

Il modo più pratico per aggiungere l'SDK streamhub-iOS al progetto è utilizzare cocoapods. Se non disponete di cocoapods, eseguite gem install cocoapods e configurazione del contenitore. Esempio di Podfile:

```
source 'https://github.com/Livefyre/cocoapods.git' 
source 'https://github.com/CocoaPods/Specs.git' 
  
platform :ios, :deployment_target => '6.0' 
  
pod 'StreamHub-iOS-SDK', '~> 0.3.0'
```

Dovrai anche aggiungere un archivio Specifiche all'installazione cocoapod (questa opzione verrà duplicata nella `~/.cocoapods/repos` directory):

```
pod repo add livefyre https://github.com/Livefyre/cocoapods.git
```

Una volta creato il contenitore nella directory principale del progetto app e nell'archivio sopra aggiunto, eseguite:

```
pod install
```

Questo scarica tutte le dipendenze e crea un file myapp. xcworkspace, da utilizzare da ora in poi per aprire il progetto dell'app in Xcode.

## Come sottoprogetto Xcode {#section_jcm_g3v_zz}

In alternativa, clonare l'archivio:

```
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
```

Quindi, aggiungete il progetto Xcode (lfsclient. xcodeproj) all'app come sottoprogetto (ad esempio, trascinate semplicemente il file lfsclient. xcodeproj nel riquadro Navigatore progetti in Xcode).

Dovrai anche effettuare le stesse operazioni con qualsiasi dipendenza ([afnetworking](https://github.com/AFNetworking/AFNetworking), [jsonkit](https://github.com/escherba/JSONKit)).

## Download di tutti gli elementi alla volta (non consigliato) {#section_rpb_f3v_zz}

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
>Per eseguire test in Xcode 6, dovete aggiungere $ (PLATFORM_ DIR)/Developer/Library/Frameworks a FRAMEWORK_ SEARCH_ PATHS in Pods-test-xctest + ohhttpstubsuitecleanup podhttps://stackoverflow.com/a/24651704[](https://stackoverflow.com/a/24651704).

È necessario il file lfstestconfig. plist da Livefyre, fornito su richiesta da Livefyre.

## Documentazione Xcode {#section_arl_b3v_zz}

Puoi sfogliare [la documentazione](https://livefyre.github.com/StreamHub-iOS-SDK/) o creare la destinazione «Documentazione» nel codice Xcode (richiede che nel sistema sia installato appledoc).

## Requisiti {#section_m5l_13v_zz}

Streamhub iOS SDK versione 0.2.0 richiede iOS 6.0 o versione successiva.

## Appendice (supporto JSON) {#section_pcd_5hv_zz}

Per gli utenti che guardano gli interattivi streamhub-iOS SDK, notare che è disponibile una versione modificata di [jsonkit](https://github.com/escherba/JSONKit) come analisi JSON predefinita (anziché nsjsonserializzazione). Ciò è dovuto al fatto che il parser fornito da Apple non supporta la decodifica di file JSON contenenti numeri interi o numeri a virgola mobile maggiori di quelli che possono essere rappresentati dal sistema. La versione modificata di jsonkit tronca numeri molto grandi al massimo del sistema corrispondente, anziché generare un'eccezione.
