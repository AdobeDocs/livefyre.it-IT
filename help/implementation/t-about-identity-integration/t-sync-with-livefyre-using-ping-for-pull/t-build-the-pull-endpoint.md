---
description: Create l'endpoint pull per ricevere e rispondere alle richieste di accesso al sistema di identità dell'utente.
seo-description: Create l'endpoint pull per ricevere e rispondere alle richieste di accesso al sistema di identità dell'utente.
seo-title: Creazione dell'endpoint di pull
solution: Experience Manager
title: Creazione dell'endpoint di pull
uuid: 1703152f-aaa7-4a88-aa33-d9f8957ad42b
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Creazione dell'endpoint di pull{#build-the-pull-endpoint}

Create l'endpoint pull per ricevere e rispondere alle richieste di accesso al sistema di identità dell'utente.

1. Create un endpoint HTTPS che riceva richieste Livefyre e risponda con un oggetto JSON che contiene i dati utente più recenti.

   >[!NOTE]
   >
   >Questo endpoint deve essere accessibile. Si raccomanda inoltre vivamente l'invio di richieste e risposte attraverso il protocollo HTTPS.

1. Registra l'endpoint con Studio.
