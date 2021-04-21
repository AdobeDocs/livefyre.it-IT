---
description: Note sulla versione per la versione del 16 novembre 2017.
title: 16 novembre 2017
exl-id: 167b8c7d-f2fb-4735-9681-d349646ec3eb
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 7%

---

# 16 novembre 2017{#november}

Note sulla versione per la versione del 16 novembre 2017.

## Versione di produzione

| **Tipo di problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Bug | AEM, libreria | È stato corretto un bug a causa del quale non veniva restituito alcun risultato quando si utilizzava la ricerca Tag e Valutazione nella Libreria. |
| Bug | App | È stato risolto un problema che impediva la visualizzazione del tag della funzione in un&#39;app a schede singole. |
| Bug | Carosello | È stato risolto un problema a causa del quale il carosello non veniva visualizzato in Designer. |
| Bug | Commenti | Sono stati corretti conteggi di commenti imprecisi nelle app di commenti. |
| Miglioramento | Scheda tecnica | L’app a schede di funzioni dispone di tutte le funzionalità di e-commerce abilitate. |
| Miglioramento | Filmstrip | Sono state aggiunte opzioni di ridimensionamento per Filmstrip in modo che l’utente possa avere un maggiore controllo sull’aspetto delle immagini nell’app. |
| Bug | Thread caldi | Sono stati corretti i messaggi di errore da Hot Threads per renderli più sicuri. |
| Miglioramento | Libreria | I clienti possono eliminare i tag avanzati applicati dal nostro sistema AI. Una volta eliminati, questi tag non vengono visualizzati nei risultati della ricerca. |
| Bug | Libreria | È stato risolto un problema che impediva la corretta visualizzazione di un’immagine dopo l’aggiunta alla libreria da una ricerca social. |
| Bug | Libreria | È stato risolto un problema che rallentava la creazione delle cartelle. |
| Bug | Libreria | Gli utenti possono ora inviare file .mov alle raccolte. |
| Bug | Libreria | Le immagini con caratteri speciali nel titolo non venivano caricate nella libreria, ma questo problema è stato risolto. |
| Miglioramento | Libreria | Abbiamo aggiornato il nostro algoritmo di classificazione &quot;rilevanza&quot; quando un utente cerca gli smart tag, quindi quando un utente attiva l’ordinamento &quot;rilevanza&quot; nella ricerca nelle librerie, viene attivato il nuovo algoritmo di classificazione. Questo nuovo algoritmo di classificazione prende in considerazione, i punteggi di precisione degli smart tag, il numero di stelle assegnate dall’utente e l’età del documento. L’obiettivo è quello di rendere l’esperienza di ricerca dei tag più precisa per l’utente. |
| Miglioramento | Libreria | Quando un cliente salva una risorsa nella libreria, Livefyre utilizza la tecnologia di machine learning di Adobe Sensei per aggiungere tag che descrivono automaticamente l’immagine della risorsa. Questo consente all’utente di cercare tali tag nel sistema. |
| Miglioramento | Libreria | Quando un cliente salva una risorsa basata su immagini nella libreria, ora Livefyre la taggerà automaticamente utilizzando la tecnologia Adobe AI, estraendo dal sistema funzioni, categorie e proprietà estetiche. Questo consente all’utente di cercare nella libreria in base a ciò che si trova all’interno delle immagini, non solo al testo. |
| Bug | Identità Livefyre | Gli avatar non venivano caricati correttamente per l&#39;implementazione dell&#39;identità LF da parte di Microsoft. Questo problema è stato risolto. |
| Bug | ModQ | È stato risolto un problema a causa del quale la moderazione dei flussi e ModQ non visualizzavano tutti i contenuti correttamente. |
| Miglioramento | Impostazioni | Ora i clienti possono visitare la nostra informativa sulla privacy e i termini di servizio di Adobe in un piè di pagina in Impostazioni. |
| Miglioramento | Flussi | È stato corretto un bug per la pre-moderazione delle regole di flusso basate su e-mail. |
| Miglioramento | Flussi | È stata aggiunta la possibilità di filtrare il contenuto del flusso in base alla lingua. |
| Miglioramento | Utenti | Aggiunta la possibilità di utilizzare file .png per gli avatar utente. |

## Versione UAT

| **Tipo di problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Bug | App Manager | È stato risolto un problema relativo alla ricerca di tag app in App Manager. |
| Bug | Libreria | È stato risolto un problema che impediva l’aggiunta di stelle per più parti di contenuto alla volta nella Libreria risorse. |
| Bug | Studio | È stato risolto un problema che impediva ad alcuni utenti di accedere a Livefyre. |
