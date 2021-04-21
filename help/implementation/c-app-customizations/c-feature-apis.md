---
description: Automatizzare il processo utilizzando le API delle funzioni
title: API delle funzionalità
exl-id: 765e47fe-a406-44e6-b4fb-b2e85fc83c01
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 2%

---

# API delle funzionalità{#feature-apis}

Automatizzare il processo utilizzando le API delle funzioni

Utilizza le API delle funzioni per automatizzare il processo in base al quale viene presentato il contenuto. Ad esempio, quando crei un blog o un&#39;app di commento in tempo reale, puoi usare tutte le funzioni del contenuto pubblicato da un moderatore selezionato per gestire la conversazione e stabilire la coerenza all&#39;interno del flusso.

Livefyre offre API sia Feature che Non feature.

## Funzione {#section_jpw_nqw_xz}

**Risorsa**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/feature/<commentId>/?lftoken=<base64userToken>
```

&#x200B; Immettere il token utente per il moderatore selezionato.

**Dati post**

```
{value: <number>} 
```

Il valore viene utilizzato per ordinare il contenuto in primo piano, dal più grande al più piccolo (10 verrà visualizzato prima di 1 nell’elenco dei contenuti in primo piano). Questo valore viene impostato automaticamente su **now** in epoch time, pertanto i commenti in primo piano vengono in genere ordinati in ordine dal più recente al meno recente.

**Risposta di esempio**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>Il campo dati non è ancora in uso.

## Funzione {#section_knh_mqw_xz}

**Risorsa**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/unfeature/<commentId>/?lftoken=<base64userToken>
```

Immettere il token utente per il moderatore selezionato.

**Risposta di esempio**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>Il campo dati non è ancora in uso.
