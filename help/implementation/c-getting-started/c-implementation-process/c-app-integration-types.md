---
description: Quando implementate le app Livefyre, lo stile di implementazione dipende dal caso di utilizzo. In questa pagina sono illustrate le funzionalità per i tre modi in cui puoi creare un'app.
seo-description: Quando implementate le app Livefyre, lo stile di implementazione dipende dal caso di utilizzo. In questa pagina sono illustrate le funzionalità per i tre modi in cui puoi creare un'app.
seo-title: Integrazioni app CMS
solution: Experience Manager
title: Integrazioni app CMS
uuid: 14fd7e36-0e50-4ae3-97f0-2de731c184f5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Integrazioni app CMS{#cms-app-integrations}

Quando implementate le app Livefyre, lo stile di implementazione dipende dal caso di utilizzo. In questa pagina sono illustrate le funzionalità per i tre modi in cui puoi creare un'app.

L'integrazione di Livefyre non è compatibile con qualsiasi piattaforma CMS e User Profile e Auth. Implementa Livefyre in uno o più modi, a seconda del caso d’uso e dei requisiti.

Puoi usare l’integrazione tradizionale per creare componenti AEM personalizzati.

## Panoramica sull'integrazione dei tipi di app CMS

| Type (Tipo) | Requisito di sviluppo | Funzioni | Pro | Limitazioni |
|--- |--- |--- |--- |--- |
| App Designer | Molto bassa | Create incorporamenti JS in Studio per aggiungere alle pagine senza uno stile <br>limitato sviluppatore e configurazioni disponibili </br>Caso di utilizzo: Pagine per uso singolo (copertura evento, campagne, hub) | È possibile avviare un'app e avviarla in breve tempo. <br>Le configurazioni possono essere eseguite da un membro non tecnico. <br>Facile al volo modifiche alle configurazioni | Creare prima un'app utilizzando Livefyre Studio <br>Non automatizzato |
| Livefyre.js | Canale | Integrare le app nel JavaScript delle pagine, caso di <br>utilizzo: Modelli riutilizzabili (contenuti editoriali, recensioni di prodotti) | Utilizza l'intera suite di personalizzazioni e configurazioni delle app <br>Automatizza il processo per creare dinamicamente un'istanza delle app dall'interno del CMS sulle pagine | Hai bisogno di uno sviluppatore in primo piano. |
| API SDK | Advanced | Recuperate i contenuti da Livefyre per utilizzarli per le applicazioni personalizzate <br>Personalizzate front-end oltre al caso di <br>utilizzo supportato: Integrazioni dati/Analytics e app front-end personalizzate | Potenza completa sull'aspetto e il comportamento dell'app | Richiede uno sviluppo immediato. <br>Un livello più elevato di sforzi da attuare. |
