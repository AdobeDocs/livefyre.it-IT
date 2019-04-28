---
description: Create l'endpoint di pull per ricevere e rispondere alle richieste di accesso al sistema di identità dell'utente.
seo-description: Create l'endpoint di pull per ricevere e rispondere alle richieste di accesso al sistema di identità dell'utente.
seo-title: Creare l'endpoint pull
solution: Experience Manager
title: Creare l'endpoint pull
uuid: 1703152 f-aaa 7-4 a 88-aa 33-d 9 f 8957 ad 42 b
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Creare l&#39;endpoint pull{#build-the-pull-endpoint}

Create l&#39;endpoint di pull per ricevere e rispondere alle richieste di accesso al sistema di identità dell&#39;utente.

1. Crea un endpoint HTTPS che riceve le richieste di Livefyre e risponde con un oggetto JSON che contiene i dati utente più recenti.

   >[!NOTE]
   >
   >Questo endpoint deve essere accessibile. È inoltre vivamente consigliabile inviare sia le richieste che le risposte al protocollo HTTPS.

1. Registra l&#39;endpoint con Studio.
