---
description: Quando implementi le app Livefyre, lo stile di implementazione dipende dal tuo caso d’uso. Questa pagina illustra le funzioni per i tre modi in cui puoi creare un’app.
title: Integrazioni di app CMS
exl-id: 7590e247-87cc-470e-bab6-e61a19221dbd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 1%

---

# Integrazioni di app CMS{#cms-app-integrations}

Quando implementi le app Livefyre, lo stile di implementazione dipende dal tuo caso d’uso. Questa pagina illustra le funzioni per i tre modi in cui puoi creare un’app.

L’integrazione di Livefyre è agnostica per qualsiasi piattaforma CMS e User Profile e Auth. Implementa Livefyre in uno o più modi, a seconda del tuo caso d’uso e dei tuoi requisiti.

Puoi utilizzare l’integrazione tradizionale per creare componenti AEM personalizzati.

## Panoramica sull’integrazione dei tipi di app CMS

| Type (Tipo) | Requisiti di sviluppo | Funzioni | Pro | Limitazioni |
|--- |--- |--- |--- |--- |
| Progettazione app | Molto basso | Crea incorporamenti JS in Studio da aggiungere alle pagine senza uno sviluppatore <br>Stile limitato e configurazioni disponibili </br>Caso di utilizzo: Pagine a uso singolo (copertura eventi, campagne, hub) | In grado di avviare un&#39;app e di eseguirla in un breve periodo di tempo. <br>Le configurazioni possono essere eseguite da un membro non tecnico. <br>Facile al volo cambia le configurazioni | È necessario creare un&#39;app prima con Livefyre Studio <br>Non automatizzata |
| Livefyre.js | Canale | Integra le app nel JavaScript delle tue pagine <br>Caso di utilizzo: Modelli riutilizzabili (contenuti editoriali, recensioni di prodotti) | Utilizza l&#39;intera suite di personalizzazioni e configurazioni dell&#39;app <br>Automatizza il processo per creare un&#39;istanza dinamica delle app dall&#39;interno del CMS sulle tue pagine | Ho bisogno di uno sviluppatore in anticipo. |
| API SDK | Advanced | Recupera i contenuti da Livefyre da utilizzare per le applicazioni personalizzate <br>Personalizza front-end oltre l’offerta supportata <br>Caso di utilizzo: Integrazioni di dati/Analytics e app front-end personalizzate | Potenza completa sull&#39;aspetto e sul funzionamento dell&#39;app | Richiede lo sviluppo in anticipo. <br>Maggiore impegno nello sviluppo per l&#39;implementazione. |
