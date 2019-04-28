---
description: Potete utilizzare Livefyre Identity con linkedin per consentire agli utenti di utilizzare i propri accessi linkedin per interagire con le app sul sito.
seo-description: Potete utilizzare Livefyre Identity con linkedin per consentire agli utenti di utilizzare i propri accessi linkedin per interagire con le app sul sito.
seo-title: Creare un'app linkedin da utilizzare con Livefyre Identity
solution: Experience Manager
title: Creare un'app linkedin da utilizzare con Livefyre Identity
uuid: c 5112 f 24-a 4 e 0-4526-afe 8-b 8 f 27 a 3 b 2854
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Creare un&#39;app linkedin da utilizzare con Livefyre Identity{#create-a-linkedin-app-for-use-with-livefyre-identity}

Potete utilizzare Livefyre Identity con linkedin per consentire agli utenti di utilizzare i propri accessi linkedin per interagire con le app sul sito.

Per abilitare l&#39;accesso di linkedin, Livefyre richiede le informazioni di app linkedin seguenti:

* Chiave consumer (chiave API)
* Segreto consumatore (Segreto API)

Per creare un&#39;app linkedin da utilizzare con Livefyre Identity:

1. Andate a https://www.linkedin.com/secure/developer e accedete all&#39;account linkedin per creare una nuova app o selezionate un&#39;app esistente da utilizzare con Livefyre Identity.
1. Fate clic **[!UICONTROL Create Application]** su.
1. Compilare il modulo per creare l&#39;applicazione.
1. In **[!UICONTROL Default Application Permissions]**, abilitate le autorizzazioni **[!UICONTROL r_basicprofile]** e **[!UICONTROL r_emailaddress]** le autorizzazioni.
1. Immettete il **[!UICONTROL OAuth 2.0 Authorized Redirect URL]** nome `https://identity.livefyre.com/{network-name}.fyre.co/api/v1.0/public/profile/social/complete/linkedin_fyre`.
1. Salvate l&#39;app.
1. In **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > LinkedIn]**, attivate l&#39; **[!UICONTROL Enable LinkedIn Login]****[!UICONTROL On]** interruttore.
1. Immettete l&#39;ID client linkedin e il segreto cliente linkedin.
1. Fate clic **[!UICONTROL Save Settings]** su.

Una volta completata, la pagina dei dettagli dell&#39;app di linkedin presenta la chiave API (Key Key) e il Segreto API (Segreto consumatore) dell&#39;app da utilizzare nella pagina Impostazioni integrazione di Studio.
