---
description: Cosa aspettarsi dall'implementazione di Livefyre Studio.
seo-description: Cosa aspettarsi dall'implementazione di Livefyre Studio.
seo-title: Processo di implementazione
solution: Experience Manager
title: Processo di implementazione
uuid: 9a0f394e-3467-47d1-9816-45e2130db440
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 1%

---


# Processo di implementazione{#implementation-process}

Il tempo necessario per implementare Livefyre dipende dall&#39;implementazione e dalla portata del lavoro.

## Panoramica dell&#39;architettura di rete Livefyre {#section_dgj_l32_rbb}

Livefyre utilizza i seguenti termini per discutere dell&#39;architettura di rete:

* Rete. Il dominio di primo livello sul quale intendete utilizzare Livefyre.
* Siti. Un sottodominio o una sezione del sito che fa parte della rete.
* iOS. Rendering dei contenuti sul sito. Il contenuto viene visualizzato visivamente nelle app utilizzando le app di visualizzazione (Mosaico, Carosello, Scheda funzioni, ecc.) o in formato testo, utilizzando le app per conversazioni (commenti, revisioni, chat ecc.). Puoi inserire una o più app nei tuoi siti.
* Streams. I flussi sono filtri che consentono di eseguire ricerche nei social media e in altri siti per raccogliere automaticamente contenuti per la moderazione o la pubblicazione diretta in un&#39;app.
* Contenuto (ad esempio, UGC, commenti). Cosa viene visualizzato nelle app. I contenuti possono essere visivi (ad esempio, foto o video), solo audio o testo.

Il diagramma seguente mostra la relazione tra Rete, Siti, App e Contenuto.

![](assets/network_site_architecture.png)

La vostra istanza Livefyre è la dashboard centrale per moderare i contenuti, gestire gli utenti e molto altro. Contattate il CSM per accedere all’istanza Livefyre.

## Passaggi per l’integrazione {#section_s2j_d2x_tz}

Esistono tre passaggi principali per integrare Livefyre:

* Integrazione app

   Quando implementate Livefyre, lo stile di implementazione dipende dal caso di utilizzo. Per [ulteriori informazioni su ciascun tipo di implementazione](/help/implementation/c-getting-started/c-implementation-process/c-app-integration-types.md#c_app_integration_types).

* Integrazione dell&#39;autenticazione

   Devi integrare il sistema di gestione utenti esistente con Livefyre per le app di conversazione e con qualsiasi altra app che richieda l&#39;autenticazione dell&#39;utente finale sul tuo sito. Se al momento non utilizzate uno strumento di gestione utenti, potete utilizzare Identità Livefyre. Per [ulteriori informazioni sull&#39;identità Livefyre, il relativo contenuto e come configurarlo](/help/implementation/c-livefyre-identity-comp/c-livefyre-identity-comp.md#c_livefyre_identity).

* Personalizzazione

   La personalizzazione è facoltativa, ma la maggior parte dei clienti personalizzano le app in base al proprio marchio.

