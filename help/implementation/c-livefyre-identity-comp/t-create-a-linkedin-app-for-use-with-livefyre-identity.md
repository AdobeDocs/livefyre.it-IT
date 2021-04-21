---
description: Puoi utilizzare Livefyre Identity con LinkedIn per consentire agli utenti di utilizzare i loro accessi LinkedIn per interagire con le app sul tuo sito.
title: Creare un’app LinkedIn da utilizzare con Livefyre Identity
exl-id: e77eca6a-1698-414e-994e-1189f780ada1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---

# Creare un&#39;app LinkedIn da utilizzare con Livefyre Identity{#create-a-linkedin-app-for-use-with-livefyre-identity}

Puoi utilizzare Livefyre Identity con LinkedIn per consentire agli utenti di utilizzare i loro accessi LinkedIn per interagire con le app sul tuo sito.

Per abilitare l&#39;accesso a LinkedIn, Livefyre richiede le seguenti informazioni sull&#39;app LinkedIn:

* Chiave consumatore (chiave API)
* Segreto consumatore (segreto API)

Per creare un’app LinkedIn da utilizzare con Livefyre Identity:

1. Vai su https://www.linkedin.com/secure/developer e accedi al tuo account LinkedIn per creare una nuova app o selezionane una esistente da utilizzare con Livefyre Identity.
1. Clic **[!UICONTROL Create Application]**.
1. Compilare il modulo per creare l&#39;Applicazione.
1. In **[!UICONTROL Default Application Permissions]**, abilita le autorizzazioni dell&#39;app **[!UICONTROL r_basicprofile]** e **[!UICONTROL r_emailaddress]** .
1. Inserisci **[!UICONTROL OAuth 2.0 Authorized Redirect URL]** come `https://identity.livefyre.com/{network-name}.fyre.co/api/v1.0/public/profile/social/complete/linkedin_fyre`.
1. Salva l’app.
1. In **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > LinkedIn]**, imposta l&#39;opzione **[!UICONTROL Enable LinkedIn Login]** su **[!UICONTROL On]**.
1. Immetti l’ID client LinkedIn e il segreto client LinkedIn.
1. Clic **[!UICONTROL Save Settings]**.

Una volta completata, la pagina dei dettagli dell’app di LinkedIn elenca la chiave API dell’app (Chiave consumatore) e il segreto API (Segreto consumatore) da utilizzare nella pagina delle impostazioni di integrazione di Studio.
