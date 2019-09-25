---
description: Automatizzare il processo utilizzando le API delle funzioni
seo-description: Automatizzare il processo utilizzando le API delle funzioni
seo-title: API delle funzionalità
title: API delle funzionalità
uuid: eac3a156-0b60-4ffa-8b6f-e451eb03da77
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# API delle funzionalità{#feature-apis}

Automatizzare il processo utilizzando le API delle funzioni

Utilizzate le API delle funzioni per automatizzare il processo con cui viene presentato il contenuto. Ad esempio, quando crei un'app Live Blog o Comment, puoi usare tutte le funzioni di un moderatore selezionato per indirizzare la conversazione e stabilire coerenza all'interno del flusso.

Livefyre offre API Feature e Unfeature.

## Funzione {#section_jpw_nqw_xz}

**Risorsa**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/feature/<commentId>/?lftoken=<base64userToken>
```

&#x200B; Immettere il token utente per il moderatore selezionato.

**Post Data**

```
{value: <number>} 
```

Il valore viene utilizzato per ordinare i contenuti contenuti in primo piano, dal più grande al più piccolo (10 verrà visualizzato prima di 1 nell'elenco dei contenuti in primo piano). Questo valore predefinito **ora** vieneimpostato in epoch time, pertanto i commenti contenuti vengono in genere ordinati dal più recente al meno recente.

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

