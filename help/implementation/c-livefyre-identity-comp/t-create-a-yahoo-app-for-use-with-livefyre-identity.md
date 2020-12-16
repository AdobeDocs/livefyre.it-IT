---
description: Puoi usare Livefyre Identity con Yahoo! per consentire agli utenti di utilizzare il proprio Yahoo! login per interagire con le app sul sito.
seo-description: Puoi usare Livefyre Identity con Yahoo! per consentire agli utenti di utilizzare il proprio Yahoo! login per interagire con le app sul sito.
seo-title: Crea uno Yahoo! App da utilizzare con identità Livefyre
solution: Experience Manager
title: Crea uno Yahoo! App da utilizzare con identità Livefyre
uuid: 6863cd2e-eb0d-465b-b706-88ecaccf41bc
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---


# Crea uno Yahoo! App da utilizzare con Livefyre Identity{#create-a-yahoo-app-for-use-with-livefyre-identity}

Puoi usare Livefyre Identity con Yahoo! per consentire agli utenti di utilizzare il proprio Yahoo! login per interagire con le app sul sito.

Per consentire ai vostri utenti di accedere con le loro credenziali Yahoo, Livefyre richiede le seguenti informazioni per l&#39;app Yahoo:

* ID client (chiave consumer)
* Segreto cliente (Segreto consumatore)

Per creare uno Yahoo! app per l&#39;uso con identità Livefyre:

1. Andate a [https://developer.yahoo.com/apps/](https://developer.yahoo.com/apps/) e accedete al vostro Yahoo! per creare una nuova app o selezionarne una esistente da utilizzare con Livefyre Identity.
1. Seleziona **[!UICONTROL Application Type: Web Application]**.
1. Invio **[!UICONTROL Callback Domain:]** `https://identity.livefyre.com`
1. Selezionare **[!UICONTROL API Permissions: Profiles (Social Directory)]** e **[!UICONTROL Read Public]**.

   Al termine, la pagina dei dettagli dell&#39;app di Yahoo elenca l&#39;ID client (Chiave di consumo) e il Segreto cliente (Segreto di consumo) dell&#39;app da utilizzare nella pagina Impostazioni integrazione di Studio.

   >[!NOTE]
   >
   >Se attivi Yahoo! login senza creare un Yahoo! e se lasciate vuoti i campi ID client e Segreto cliente in Studio, Livefyre utilizzerà OpenID per registrare questi utenti nelle app Livefyre. OAuth e il marchio personalizzato non saranno disponibili in questo caso.