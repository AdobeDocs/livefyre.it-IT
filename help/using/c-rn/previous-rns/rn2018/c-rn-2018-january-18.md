---
description: Note sulla versione per la versione del 18 gennaio 2018.
title: 18 gennaio 2018
exl-id: aaf49dc9-64eb-4354-8bcb-04039fa25f10
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 6%

---

# 18 gennaio 2018{#january}

Note sulla versione per la versione del 18 gennaio 2018.

## Versione di produzione

| **Tipo di problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Bug | App | È stato corretto un bug a causa del quale gli Avatar non venivano riprodotti correttamente in caso di utilizzo di un file jpeg. |
| Bug | ModQ | È stato corretto un bug che consentiva ai clienti S1 di filtrare per raccolte in ModQ. |
| Bug | Flussi | È stato corretto un bug a causa del quale una regola di flusso veniva interrotta quando il filtro della lingua era impostato come &quot;none&quot;. |
| Bug | Flussi | È stato corretto un bug che impediva il salvataggio delle regole di flusso di YouTube. |
| Bug | Flussi | È stato corretto un bug a causa del quale gli utenti potevano creare voci geografiche formattate in modo errato nelle regole di flusso e salvarle, il che avrebbe causato un errore del flusso. Ora gli utenti non possono più salvare i tag geografici in formato non corretto. |
| Bug | Studio | È stato risolto un problema che impediva ad alcuni utenti di accedere a Livefyre. |

## Versione UAT

| **Tipo di problema** | **Componente** | **Note sulla versione** |
|---|---|---|
| Bug | Libreria | Correzione bug di sicurezza. Tutte le chiamate di autenticazione ora vengono effettuate utilizzando il protocollo HTTPS invece che HTTP. |
| Miglioramento | Tag avanzati | Il contenuto inviato in streaming viene ora automaticamente contrassegnato da Adobe Sensei con tag avanzati, in quanto viene salvato in una cartella o pubblicato in un’app. |
| Bug | Flussi | È stato risolto un problema che impediva alle regole di flusso di Instagram di riconoscere i caratteri giapponesi. |
| Miglioramento | Flussi | Ora i clienti possono utilizzare gli operatori logici ( ANY, ALL, NOT) per creare filtri avanzati dettagliati nei flussi che curano contenuti molto più precisi. Ad esempio, se uso l&#39;hashtag #himalyas, posso scegliere di mostrare solo immagini che includono &quot;montagne nevose&quot;. |
| Bug | Studio | Correzione di un bug che mostrava caratteri speciali nei nomi come HTML. |
