---
description: Puoi usare Livefyre Identity con Yahoo! per consentire agli utenti di utilizzare il loro Yahoo! accessi per interagire con le app sul sito.
title: Crea un Yahoo! App per l’utilizzo con Livefyre Identity
exl-id: 6b4c6ea9-1cb0-4496-aabe-70811f464a3d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# Crea un Yahoo! App da utilizzare con Livefyre Identity{#create-a-yahoo-app-for-use-with-livefyre-identity}

Puoi usare Livefyre Identity con Yahoo! per consentire agli utenti di utilizzare il loro Yahoo! accessi per interagire con le app sul sito.

Per consentire ai tuoi utenti di accedere con le loro credenziali Yahoo, Livefyre richiede le seguenti informazioni dell&#39;app Yahoo:

* ID client (chiave consumer)
* Segreto client (segreto consumatore)

Per creare un Yahoo! app da utilizzare con Livefyre Identity:

1. Vai a [https://developer.yahoo.com/apps/](https://developer.yahoo.com/apps/) e accedi al tuo Yahoo! per creare una nuova app o selezionarne una esistente da utilizzare con Livefyre Identity.
1. Seleziona **[!UICONTROL Application Type: Web Application]**.
1. Inserisci **[!UICONTROL Callback Domain:]** `https://identity.livefyre.com`
1. Selezionare **[!UICONTROL API Permissions: Profiles (Social Directory)]** e **[!UICONTROL Read Public]**.

   Al termine, la pagina dei dettagli dell’app di Yahoo elenca l’ID client (chiave di consumo) e il segreto client (segreto di consumo) dell’app da utilizzare nella pagina Impostazioni integrazione di Studio.

   >[!NOTE]
   >
   >Se si abilita Yahoo! accedi senza creare un Yahoo! app e se lasci vuoti i campi ID client e Segreto client in Studio, Livefyre utilizzerà OpenID per registrare questi utenti nelle tue app Livefyre. OAuth e il branding personalizzato non saranno disponibili in questo caso.
