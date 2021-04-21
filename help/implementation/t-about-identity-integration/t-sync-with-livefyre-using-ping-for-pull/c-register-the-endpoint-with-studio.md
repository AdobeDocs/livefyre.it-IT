---
description: Registra l'endpoint URL in modo che Livefyre possa utilizzare l'URL per richiamare le informazioni di profilo aggiornate.
title: Registra l'endpoint con Studio
exl-id: 2910a13a-ae88-41d7-ba7c-88d7a1dbe445
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# Registra l&#39;endpoint con Studio{#register-the-endpoint-with-studio}

Registra l&#39;endpoint URL in modo che Livefyre possa utilizzare l&#39;URL per richiamare le informazioni di profilo aggiornate.

Registra il ping per l&#39;URL di pull una sola volta per rete. Una volta impostato, questo valore non deve cambiare a meno che l&#39;endpoint per il recupero dei dati del profilo utente dal sistema di gestione utenti non cambi.

1. Utilizza Studio per registrare questo endpoint URL con Livefyre.
1. Registra l&#39;URL da cui Livefyre recupererà le informazioni aggiornate sul profilo utente, vai a **[!UICONTROL Studio > Settings > Integration Settings > Remote Profiles]** e inseriscilo nel campo **[!UICONTROL Ping for Pull URL]** .

   Ad esempio, l’URL può avere un aspetto simile al seguente: `https://example.yoursite.com/some_path/?id={id}`
