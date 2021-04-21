---
description: Utilizza Ping per Pull per mantenere Livefyre sincronizzato con il tuo sistema di gestione degli utenti.
title: Sincronizzazione con Livefyre utilizzando Ping per Pull
exl-id: 01b5851d-9dc0-44dc-9c0d-0c467502450d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Sincronizzazione con Livefyre utilizzando Ping per Pull{#sync-with-livefyre-using-ping-for-pull}

Utilizza Ping per Pull per mantenere Livefyre sincronizzato con il tuo sistema di gestione degli utenti.

In generale, ***Ping*** Livefyre ogni volta che un utente del tuo sito web/app aggiorna il suo profilo (nome visualizzato, avatar, ecc.) e Livefyre ***Pulls*** il profilo aggiornato dell&#39;utente.

![](assets/Ping-for-Pull.png)

Ping per sequenza di trazione:

1. Il cliente invia una richiesta Ping a Livefyre (incluso l’utente da aggiornare).
1. Livefyre conferma la ricezione di ping con HTTP 200/Success.
1. Livefyre elabora la richiesta Pull.
1. Richiesta di pull in coda di Livefyre.
1. Livefyre esegue la richiesta di pull all’endpoint per acquisire le informazioni utente aggiornate.
1. Il cliente riceve la risposta Pull e convalida.
1. Livefyre aggiorna i profili remoti con le informazioni di profilo esterne incluse nell’endpoint Pull.

Effettua il ping di Livefyre ogni volta che un utente aggiorna le sue informazioni sul profilo. Mentre Ping per il tempo di completamento del pull può variare a seconda del carico di rete, aggiorna le informazioni utente tra 1 e 10 minuti. Le modifiche del profilo aggiornate verranno visualizzate prima in Livefyre Studio > Utenti.

Le informazioni sul profilo aggiornato verranno visualizzate nelle app Livefyre dopo due eventi:

* Un utente si disconnette, quindi accede di nuovo all’app. I valori del nome visualizzato in userAuthToken hanno la precedenza su Ping per gli aggiornamenti di Pull. Un utente disconnesso/login aggiornerà il token per aggiornare la sessione.

   Per generare nuovi userAuthToken quando le informazioni sul profilo vengono aggiornate, utilizza l&#39;SSO authDelegate per disconnettersi e quindi accedere di nuovo in background.

* Un aggiornamento bootstrap della raccolta includerà le informazioni aggiornate (al massimo ogni 5-10 minuti).

Per implementare Ping for Pull per il tuo sistema di profilo utente:

1. [Creare l’endpoint](#t_build_the_pull_endpoint) Pull.

   >[!NOTE]
   >
   >La libreria Livefyre include un metodo syncUser per mantenere i profili utente aggiornati. Ignora i due passaggi successivi se utilizzi la libreria Livefyre .

1. [Registra l&#39;endpoint Pull in Studio](#register_the_endpoint_with_studio).
1. [Crea il ping](#t_build_the_ping).
1. [Genera il ping per la risposta] di pull.(#reference_n3x_pzb_mz)
