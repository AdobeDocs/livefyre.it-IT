---
description: Conta il numero di elementi social curati.
title: Contatore social
exl-id: def7fba4-1c2e-4c7b-84f7-f9ede592d675
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 5%

---

# Contatore social{#social-counter}

Conta il numero di elementi social curati. Per un elenco completo degli endpoint disponibili, consulta la sezione Livefyre [Riferimento API](https://api.livefyre.com/docs) .

L&#39;API del contatore social restituisce i conteggi per le regole di cura corrispondenti in una determinata raccolta per gli intervalli di un periodo di tempo.

>[!NOTE]
>
>Questa API è disponibile solo per gli hashtag Twitter.

API contatore social:

* Risorsa
* Tipi di regole
* Risposta

## Risorsa {#section_p2s_2hc_11b}

```
GET https://{networkName}.bootstrap.fyre.co/api/v3.0/stats.collections.curate/{query}.json
```

* **networkName:** il nome di rete fornito da Livefyre. Ad esempio: *laboratori* in `labs.fyre.co`.
* **query:** hash codificato url-safe base64 di tutto il sito, ID articolo, coppie di tipo regola per le quali è necessario recuperare le informazioni sul conteggio (pre-codificato)

   ```
   {site ID}:{article ID};{rule-type},  {article ID};{rule-type}|{site ID}:{article ID};{rule-type}
   ```

   >[!NOTE]
   >La query è limitata a 10 siti, ID articolo, coppie di tipo regola. (L&#39;esempio precedente conterrebbe 3 tule).

* **** `(optional)` specifica il periodo di tempo relativo o assoluto da rappresentare nel grafico; da specifica l’inizio e il valore predefinito è 24 ore fa, se omesso.
* **** `(optional)` non specifica il periodo di tempo relativo o assoluto da rappresentare nel grafico; fino specifica l’inizio e, se omesso, imposta l’ora corrente (ora).

### Tempo relativo

| Abbreviazione | Unità |
|---|---|
| s | Seconds |
| min | Minutes |
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

FORMATO: HH:MM_YYYYMMDD

| Abbreviazione | Significato |
|---|---|
| HH | Ore (in formato 24 ore) |
| MM | Minutes |
| YYYY | Anno a 4 cifre |
| MM | Mese |
| DD | Giorno |

Esempio:

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=04:00_20130709 
```

## Tipi di regole {#section_v53_xqb_11b}

| Valore | Type (Tipo) |
|---|---|
| 2 | Twitter |

Esempio:

Per ottenere i conteggi nell’ultimo minuto per il sito `123456` e l’ID articolo `some-article-id` e il tipo di regola `2`, ad esempio: `123456:some-article-id;2:`

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
