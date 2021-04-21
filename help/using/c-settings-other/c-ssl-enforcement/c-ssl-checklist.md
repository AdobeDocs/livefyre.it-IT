---
description: Segui i passaggi descritti nella checklist per assicurarti di convertire correttamente da HTTP a HTTPS.
title: Elenco di controllo SSL
exl-id: 20161aa5-57c9-417b-af0e-c9e1e771f861
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---

# Lista di controllo SSL{#ssl-checklist}

Segui i passaggi descritti nella checklist per assicurarti di convertire correttamente da HTTP a HTTPS.

La conversione da HTTP a HTTPS verrà eseguita correttamente se sono stati completati i seguenti elementi:

* Tutte le mie integrazioni server-to-server utilizzano HTTPS.
* Tutte le mie integrazioni server-to-server supportano i crittografia TLS 1.2.
* Tutte le mie app mobili utilizzano HTTPS.
* Tutte le mie app mobili supportano i crittografia TLS 1.2.
* Tutte le mie integrazioni JavaScript personalizzate (StreamhubSDK o utilizzo API diretto) utilizzano HTTPS.
* Se distribuisco Livefyre JavaScript, utilizziamo le versioni più recenti.
* Ho notificato un servizio di terze parti (ad esempio analisi dei contenuti, moderazione, ecc.) che utilizza le API Livefyre per conto mio di queste modifiche.
