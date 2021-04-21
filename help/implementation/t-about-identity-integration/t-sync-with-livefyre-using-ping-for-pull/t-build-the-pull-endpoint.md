---
description: Crea l’endpoint pull per ricevere e rispondere alle richieste di accesso al sistema di identità utente.
title: Creare l’endpoint di pull
exl-id: cc66365b-0d5f-4a0b-954f-ee014e75d4a2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---

# Creare l&#39;endpoint di pull{#build-the-pull-endpoint}

Crea l’endpoint pull per ricevere e rispondere alle richieste di accesso al sistema di identità utente.

1. Crea un endpoint HTTPS che riceve le richieste Livefyre e risponde con un oggetto JSON che contiene i dati utente più recenti.

   >[!NOTE]
   >
   >Questo endpoint deve essere accessibile. Si consiglia inoltre vivamente di inviare entrambe le richieste e le risposte tramite il protocollo HTTPS.

1. Registra l&#39;endpoint con Studio.
