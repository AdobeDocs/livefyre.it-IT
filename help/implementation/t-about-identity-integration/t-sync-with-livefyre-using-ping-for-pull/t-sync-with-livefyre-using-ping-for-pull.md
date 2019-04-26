---
description: Utilizzate Ping per Pull per mantenere Livefyre sincronizzato con il
  sistema di gestione degli utenti.
seo-description: Utilizzate Ping per Pull per mantenere Livefyre sincronizzato con
  il sistema di gestione degli utenti.
seo-title: Sincronizzazione con Livefyre utilizzando Ping per Pull
solution: Experience Manager
title: Sincronizzazione con Livefyre utilizzando Ping per Pull
uuid: 7 b 059064-1 cca -46 d 7-8055-dfe 59 f 493 ac 1
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Sincronizzazione con Livefyre utilizzando Ping per Pull{#sync-with-livefyre-using-ping-for-pull}

Utilizzate Ping per Pull per mantenere Livefyre sincronizzato con il sistema di gestione degli utenti.

In generale ***, esegui Ping*** Livefyre ogni volta che un utente del sito Web o dell'app aggiorna il profilo (nome visualizzato, avatar ecc.) e Livefyre ***estrae*** il profilo aggiornato dell'utente.

![](assets/Ping-for-Pull.png)

Ping per la sequenza di pull:

1. Il cliente invia la richiesta ping a Livefyre (incluso l'utente da aggiornare).
1. Livefyre conferma la ricezione di Ping con HTTP 200/Success.
1. Livefyre elabora la richiesta di pull.
1. Livefyre mette in coda la richiesta di pull.
1. Livefyre esegue la richiesta pull all'endpoint per acquisire informazioni aggiornate sull'utente.
1. Il cliente riceve la risposta di Pull e convalida.
1. Livefyre aggiorna Profili remoti con le informazioni del profilo esterno incluse nell'endpoint Pull.

Ping Livefyre ogni volta che un utente aggiorna le informazioni sul profilo. Mentre il tempo di completamento dell'pull può variare a seconda del carico di rete, aggiorna le informazioni dell'utente entro tra 1 e 10 minuti. Le modifiche di profilo aggiornate verranno visualizzate prima in Livefyre Studio > Utenti.

Le informazioni sul profilo verranno visualizzate nella vostra app Livefyre dopo due eventi:

* Un utente viene disconnesso e quindi ritorna nell'app. I valori del nome visualizzato in userauthtoken hanno la precedenza rispetto a Ping per gli aggiornamenti Pull. La funzione di login o login utente aggiorna il token per aggiornare la sessione.

   Per generare nuovi userauthtokens quando vengono aggiornate le informazioni sul profilo, utilizzate SSO authdelegate per uscire nuovamente dal vostro utente in background.

* Un aggiornamento di avvio automatico della raccolta porterà le informazioni aggiornate (al massimo ogni 5-10 minuti).

Per implementare Ping for Pull per il sistema di profilo utente:

1. [Create l'endpoint Pull](#t_build_the_pull_endpoint).

   >[!NOTE]
   >
   >La libreria Livefyre include un metodo syncuser per tenere aggiornato i profili utente. Ignorate i due passaggi successivi se utilizzate la libreria Livefyre.

1. [Registra l'endpoint Pull in Studio](#register_the_endpoint_with_studio).
1. [Create il Ping](#t_build_the_ping).
1. [Create il Ping for Pull Response].(# reference_ n 3 x_ pzb_ mz)
