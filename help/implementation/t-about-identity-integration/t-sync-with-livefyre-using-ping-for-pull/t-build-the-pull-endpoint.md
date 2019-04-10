---
description: Create l'endpoint di pull per ricevere e rispondere alle richieste di
  accesso al sistema di identità dell'utente.
seo-description: Create l'endpoint di pull per ricevere e rispondere alle richieste
  di accesso al sistema di identità dell'utente.
seo-title: Creare l'endpoint pull
solution: Experience Manager
title: Creare l'endpoint pull
uuid: 1703152 f-aaa 7-4 a 88-aa 33-d 9 f 8957 ad 42 b
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Creare l'endpoint pull{#build-the-pull-endpoint}

Create l'endpoint di pull per ricevere e rispondere alle richieste di accesso al sistema di identità dell'utente.

1. Crea un endpoint HTTPS che riceve le richieste di Livefyre e risponde con un oggetto JSON che contiene i dati utente più recenti.

   >[!NOTE]
   >
   >Questo endpoint deve essere accessibile. È inoltre vivamente consigliabile inviare sia le richieste che le risposte al protocollo HTTPS.

1. Registra l'endpoint con Studio.
