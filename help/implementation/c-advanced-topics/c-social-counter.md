---
description: Conta il numero di elementi social curati.
seo-description: Conta il numero di elementi social curati.
seo-title: Contatore social
solution: Experience Manager
title: Contatore social
uuid: fa 9 aa 1 a 8-6 a 04-4 bc 1-9 bfe-e 42 c 1250 fd 48
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Contatore social{#social-counter}

Conta il numero di elementi social curati. Per un elenco completo degli endpoint disponibili, consultate la sezione [Riferimento](https://api.livefyre.com/docs) API di Livefyre.

Il conteggio API Social restituisce i conteggi delle regole di cura corrispondenti in una determinata raccolta a intervalli di tempo.

>[!NOTE]
>
>Questa API è disponibile solo per gli hashtag Twitter.

API del contatore social:

* Risorsa
* Tipi di regole
* Risposta

## Risorsa {#section_p2s_2hc_11b}

```
GET https://{networkName}.bootstrap.fyre.co/api/v3.0/stats.collections.curate/{query}.json
```

* **Networkname:** Il nome di rete fornito da Livefyre. Ad esempio: *in*`labs.fyre.co`.
* **query:** Hash codificato basato su URL 64 di tutto il sito, ID articolo, croples di tipo regola per i quali le informazioni sul conteggio devono essere recuperate (precodificate)

   ```
   {site ID}:{article ID};{rule-type},  {article ID};{rule-type}|{site ID}:{article ID};{rule-type}
   ```

   >[!NOTE]
   >La query è limitata a 10 sito, ID articolo, tuples di tipo regola. (L'esempio precedente conterrà 3 pcm).

* **from** `(optional)` specifica il periodo di tempo relativo o assoluto al grafico; from specify the beginning and defaults to 24 hours prior, if omitted.
* **fino** `(optional)` a specificare il periodo di tempo relativo o assoluto al grafico; fino a specificare l'inizio e impostazioni predefinite per l'ora corrente (ora), se omessa.

### Tempo relativo

| Abbreviazione | Unità |
|---|---|
| s | Secondi |
| min | Minuti |
| h | Ore |
| d | Giorni |
| w | Settimane |
| mon | 30 giorni (mese) |
| y | 365 giorni (anno) |

Esempio:

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=-7d&until=-6d
```

## Tempo assoluto {#section_xqr_jgc_11b}

FORMATO: HH: MM_ YYYYMMDD

| Abbreviazione | Significato |
|---|---|
| HH | Ore (in formato orologio a 24 h) |
| MM | Minuti |
| YYYY | Anno di 4 cifre |
| MM | Mese |
| DD | Giorno |

Esempio:

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=04:00_20130709 
```

## Tipi di regole {#section_v53_xqb_11b}

| Valore | Tipo |
|---|---|
| 2 | Twitter |

Esempio:

Per ottenere conteggio sull'ultimo minuto per il sito `123456` e l'ID articolo `some-article-id` e per il tipo di regola `2`, ad esempio: `123456:some-article-id;2:`

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
