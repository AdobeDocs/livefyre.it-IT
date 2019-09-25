---
description: Conta il numero di elementi social curati.
seo-description: Conta il numero di elementi social curati.
seo-title: Contatore social
solution: Experience Manager
title: Contatore social
uuid: fa9aa1a8-6a04-4bc1-9bfe-e42c1250fd48
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Contatore social{#social-counter}

Conta il numero di elementi social curati. Per un elenco completo degli endpoint disponibili, consultate la sezione Riferimento [](https://api.livefyre.com/docs) API Livefyre.

L'API Social Counter restituisce i conteggi per le regole di cura corrispondenti in una determinata raccolta per gli intervalli in un determinato periodo di tempo.

>[!NOTE]
>
>Questa API è disponibile solo per gli hashtag Twitter.

Social Counter API:

* Risorsa
* Tipi di regole
* Risposta

## Risorsa {#section_p2s_2hc_11b}

```
GET https://{networkName}.bootstrap.fyre.co/api/v3.0/stats.collections.curate/{query}.json
```

* **** networkName: Il nome di rete fornito da Livefyre. Ad esempio: *laboratori* in `labs.fyre.co`.
* **** query: L'hash codificato url-safe di base64 di tutto il sito, l'ID articolo, le coppie di tipo regola per le quali recuperare le informazioni sul conteggio (precodificato)

   ```
   {site ID}:{article ID};{rule-type},  {article ID};{rule-type}|{site ID}:{article ID};{rule-type}
   ```

   >[!NOTE]
   >La query è limitata a 10 siti, ID articolo, coppie di tipo regola. L’esempio precedente contiene 3 coppie.

* **da** `(optional)` specifica il periodo di tempo relativo o assoluto da rappresentare sul grafico; from specifica l'inizio e, se omesso, il valore predefinito è 24 ore fa.
* **fino** a specificare `(optional)` il periodo di tempo relativo o assoluto da rappresentare; fino specifica l'inizio e, se omesso, imposta l'ora corrente (ora) per impostazione predefinita.

### Tempo relativo

| Abbreviazione | Unità |
|---|---|
| s | Secondi |
| min | Minuti |
| h | Ore |
| d | Giorni |
| w | settimane |
| mon | 30 giorni (mese) |
| y | 365 giorni (anno) |

Esempio:

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=-7d&until=-6d
```

## Tempo assoluto {#section_xqr_jgc_11b}

FORMATO: HH:MM_YYYMMDD

| Abbreviazione | Significato |
|---|---|
| HH | Ore (in formato 24 ore) |
| MM | Minuti |
| YYYY | Anno a 4 cifre |
| MM | Mese |
| DD |  Day |

Esempio:

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=04:00_20130709 
```

## Tipi di regole {#section_v53_xqb_11b}

| Valore | Type (Tipo) |
|---|---|
| 2 | Twitter |

Esempio:

Per ottenere i conteggi nell’ultimo minuto per l’ID del sito `123456` e dell’articolo `some-article-id` e il tipo di regola, ad esempio `2`: `123456:some-article-id;2:`

```
curl -XGET "https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=-1min" 
```

Risposta di esempio:

```
{ 
    "status": "ok", 
    "code": 200, 
    "data": { 
        "123456": { 
            "some-article-id": { 
                "2": [ 
                    [ 
                        2, 
                        1374770460 
                    ], 
                    [ 
                        4, 
                        1374770470 
                    ], 
                    [ 
                        3, 
                        1374770480 
                    ], 
                    [ 
                        1, 
                        1374770490 
                    ], 
                    [ 
                        0, 
                        1374770500 
                    ], 
                    [ 
                        7, 
                        1374770510 
                    ] 
                ] 
            } 
        } 
    } 
}
```
