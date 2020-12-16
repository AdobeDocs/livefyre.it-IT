---
description: Quando implementate le app Livefyre, lo stile di implementazione dipende dal caso di utilizzo. In questa pagina sono illustrate le funzionalità per i tre modi in cui puoi creare un'app.
seo-description: Quando implementate le app Livefyre, lo stile di implementazione dipende dal caso di utilizzo. In questa pagina sono illustrate le funzionalità per i tre modi in cui puoi creare un'app.
seo-title: Integrazioni app CMS
solution: Experience Manager
title: Integrazioni app CMS
uuid: 14fd7e36-0e50-4ae3-97f0-2de731c184f5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 1%

---


# Integrazioni app CMS{#cms-app-integrations}

Quando implementate le app Livefyre, lo stile di implementazione dipende dal caso di utilizzo. In questa pagina sono illustrate le funzionalità per i tre modi in cui puoi creare un&#39;app.

L&#39;integrazione di Livefyre non è compatibile con qualsiasi piattaforma CMS e User Profile e Auth. Implementa Livefyre in uno o più modi, a seconda del caso d’uso e dei requisiti.

È possibile utilizzare l&#39;integrazione tradizionale per creare componenti AEM personalizzati.

## Panoramica sull&#39;integrazione dei tipi di app CMS

| Type (Tipo) | Requisito di sviluppo | Funzioni | Pros | Limitazioni |
|--- |--- |--- |--- |--- |
| App Designer | Molto bassa | Create JS embeds in Studio per aggiungere alle pagine senza uno sviluppatore <br>Limitato stile e configurazioni disponibili </br>Caso di utilizzo: Pagine per uso singolo (copertura evento, campagne, hub) | Possibilità di avviare un&#39;app e di eseguirla in poco tempo. <br>Le configurazioni possono essere eseguite da un membro non tecnico. <br>Facile al volo modifiche alle configurazioni | Creare un&#39;app utilizzando prima Livefyre Studio <br>Non automatizzato |
| Livefyre.js | Canale | Integrare le app nel JavaScript delle pagine <br>Caso di utilizzo: Modelli riutilizzabili (contenuti editoriali, recensioni di prodotti) | Utilizza l&#39;intera suite di personalizzazioni e configurazioni delle app <br>Automatizza il processo per creare dinamicamente un&#39;istanza delle app dall&#39;interno del CMS sulle tue pagine | Hai bisogno di uno sviluppatore in primo piano. |
| API SDK | Advanced | Recuperate i contenuti da Livefyre per le applicazioni personalizzate <br>Personalizzate front-end oltre l&#39;offerta supportata <br>Caso di utilizzo: Integrazioni dati/Analytics e app front-end personalizzate | Potenza completa sull&#39;aspetto e il comportamento dell&#39;app | Richiede uno sviluppo immediato. <br>Un livello più elevato di sforzi di sviluppo da attuare. |
