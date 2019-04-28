---
description: Cosa aspettarsi nell'implementazione di Livefyre Studio.
seo-description: Cosa aspettarsi nell'implementazione di Livefyre Studio.
seo-title: Processo di implementazione
solution: Experience Manager
title: Processo di implementazione
uuid: 9 a 0 f 394 e -3467-47 d 1-9816-45 e 2130 db 440
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Processo di implementazione{#implementation-process}

Il tempo di implementazione di Livefyre dipende dalla vostra implementazione e ambito.

## Panoramica di Livefyre Network Architecture {#section_dgj_l32_rbb}

Livefyre utilizza i termini seguenti nella discussione sull&#39;architettura di rete:

* Rete. Il dominio di livello più alto su cui intendi utilizzare Livefyre.
* Siti. Un sottodominio o una sezione del sito che fa parte della rete.
* App. Un rendering dei contenuti sul sito. Il contenuto viene visualizzato in App visivamente, utilizzando le app visualizzazione (Mosaic, Carosello, Scheda Feature Card, ecc.) o in formato di testo, utilizzando le App di conversazione (Commenti, Recensioni, Chat, ecc.). Puoi inserire una o più app sui tuoi siti.
* Flussi. I flussi sono filtri che cercano social media e altri siti per raccogliere automaticamente i contenuti per moderazione o pubblicazione diretta in un&#39;app.
* Contenuto (ad esempio, UGC, commenti). Ciò che viene visualizzato nelle app. Il contenuto può essere visivo (ad esempio, una foto o un video), solo audio o testo.

Il diagramma seguente mostra il rapporto tra Rete, Siti, App e Contenuto.

![](assets/network_site_architecture.png)

Disponete della vostra istanza di Livefyre, il dashboard centrale per moderazione del contenuto, gestione degli utenti e altro ancora. Contatta il tuo CSM per accedere all&#39;istanza di Livefyre.

## Passaggi per l&#39;integrazione {#section_s2j_d2x_tz}

Per integrare Livefyre sono disponibili tre passaggi principali:

* Integrazione app

   Quando implementate Livefyre, lo stile dell&#39;implementazione dipende dal caso d&#39;uso. Per [ulteriori informazioni su ciascun tipo di implementazione](/help/implementation/c-getting-started/c-implementation-process/c-app-integration-types.md#c_app_integration_types).

* Integrazione autenticazione

   Dovete integrare il sistema di gestione utenti esistente con Livefyre per la conversazione delle app e di qualsiasi altra app che richieda l&#39;autenticazione per utenti finali sul sito. Se al momento non utilizzate alcuno strumento di gestione degli utenti, potete utilizzare Livefyre Identity. Per [ulteriori informazioni su Livefyre Identità, su cosa si tratta e come configurarla](/help/implementation/c-livefyre-identity-comp/c-livefyre-identity-comp.md#c_livefyre_identity).

* Personalizzazione

   La personalizzazione è facoltativa, ma la maggior parte dei clienti personalizza le app per adattarle al loro marchio.

