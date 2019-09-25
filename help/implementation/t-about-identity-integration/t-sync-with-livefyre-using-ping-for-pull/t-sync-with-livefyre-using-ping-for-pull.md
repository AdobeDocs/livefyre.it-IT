---
description: Utilizzate Ping for Pull per mantenere Livefyre sincronizzato con il sistema di gestione degli utenti.
seo-description: Utilizzate Ping for Pull per mantenere Livefyre sincronizzato con il sistema di gestione degli utenti.
seo-title: Sincronizzazione con Livefyre tramite Ping per pull
solution: Experience Manager
title: Sincronizzazione con Livefyre tramite Ping per pull
uuid: 7b059064-1cca-46d7-8055-dfe59f493ac1
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Sincronizzazione con Livefyre tramite Ping per pull{#sync-with-livefyre-using-ping-for-pull}

Utilizzate Ping for Pull per mantenere Livefyre sincronizzato con il sistema di gestione degli utenti.

In generale, ***Ping*** Livefyre ogni volta che un utente del sito Web o dell’app aggiorna il proprio profilo (nome visualizzato, avatar, ecc.) e Livefyre ***Pulls*** il profilo aggiornato dell’utente.

![](assets/Ping-for-Pull.png)

Ping per sequenza pull:

1. Il cliente invia una richiesta di ping a Livefyre (incluso l’utente da aggiornare).
1. Livefyre conferma la ricezione del ping con HTTP 200/Success.
1. Livefyre elabora la richiesta pull.
1. Code Livefyre Richiesta pull.
1. Livefyre esegue la richiesta pull all’endpoint per acquisire le informazioni utente aggiornate.
1. Il cliente riceve la risposta pull e la convalida.
1. Livefyre aggiorna i profili remoti con le informazioni di profilo esterne incluse nell'endpoint pull.

Ping Livefyre ogni volta che un utente aggiorna le informazioni del proprio profilo. Mentre il tempo di completamento Ping for Pull può variare a seconda del carico di rete, aggiorna le informazioni utente tra 1 e 10 minuti. Le modifiche del profilo aggiornate verranno visualizzate prima in Livefyre Studio &gt; Utenti.

Le informazioni sul profilo aggiornate verranno visualizzate nelle app Livefyre dopo due eventi:

* Un utente si disconnette, quindi accede nuovamente all'app. I valori dei nomi visualizzati in userAuthToken hanno precedenza rispetto a Ping per gli aggiornamenti pull. Un logout/login utente aggiornerà il token per aggiornare la sessione.

   Per generare un nuovo userAuthToken quando vengono aggiornate le informazioni del profilo, utilizza SSO authDelegate per disconnettere l’utente e quindi di nuovo in background.

* Un aggiornamento di avvio alla raccolta includerà le informazioni aggiornate (al massimo ogni 5-10 minuti).

Per implementare Ping for Pull per il tuo sistema di profili utente:

1. [Create l'endpoint](#t_build_the_pull_endpoint)pull.

   >[!NOTE]
   >
   >La libreria Livefyre include un metodo syncUser per tenere aggiornati i profili utente. Se utilizzate la libreria Livefyre, saltate i due passaggi successivi.

1. [Registra l’endpoint pull in Studio](#register_the_endpoint_with_studio).
1. [Create il ping](#t_build_the_ping).
1. [Create il ping per la risposta]pull.(#reference_n3x_pzb_mz)
