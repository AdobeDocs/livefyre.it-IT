---
description: Automatizzare il processo utilizzando le API delle funzionalità
seo-description: Automatizzare il processo utilizzando le API delle funzionalità
seo-title: API funzionalità
title: API funzionalità
uuid: eac 3 a 156-0 b 60-4 ffa -8 b 6 f-e 451 eb 03 da 77
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# API funzionalità{#feature-apis}

Automatizzare il processo utilizzando le API delle funzionalità

Utilizzate le API delle funzionalità per automatizzare il processo in base al quale è contenuto il contenuto. Ad esempio, quando create un&#39;app di blog live o commento, funzione tutto il contenuto pubblicato da un moderatore selezionato per guidare la conversazione e stabilire coerenza nel flusso.

Livefyre offre entrambe le API Feature e Unfeature.

## Funzione {#section_jpw_nqw_xz}

**Risorsa**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/feature/<commentId>/?lftoken=<base64userToken>
```

Immettete il token utente per il moderatore selezionato.

**Post dati**

```
{value: <number>} 
```

Il valore verrà utilizzato per ordinare contenuti contenuti, più piccoli (10 appariranno prima del 1 nell&#39;elenco dei contenuti contenuti). Questo valore è predefinito **ora** in ora epoch, quindi i commenti contenuti verranno generalmente ordinati più in base alla meno recente.

**Risposta di esempio**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>Il campo dati non è ancora utilizzato.

## Funzionalità {#section_knh_mqw_xz}

**Risorsa**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/unfeature/<commentId>/?lftoken=<base64userToken>
```

Immettete il token utente per il moderatore selezionato.

**Risposta di esempio**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>Il campo dati non è ancora utilizzato.

