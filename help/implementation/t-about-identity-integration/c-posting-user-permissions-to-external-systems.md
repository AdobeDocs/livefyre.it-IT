---
description: Livefyre utilizza un'interfaccia PUSH per inviare a un sistema esterno informazioni sulle modifiche alle autorizzazioni utente.
title: Pubblicazione delle autorizzazioni utente su sistemi esterni (facoltativo)
exl-id: 335c9ff2-e392-4310-aad2-7890c8e82eba
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 4%

---

# Pubblicazione delle autorizzazioni utente su sistemi esterni (facoltativo){#posting-user-permissions-to-external-systems-optional}

Livefyre utilizza un&#39;interfaccia PUSH per inviare a un sistema esterno informazioni sulle modifiche alle autorizzazioni utente.

## Tipi di utenti in Livefyre Studio

| Tipo di utente | Descrizione |
|--- |--- |
| proprietario | Questo utente è proprietario e può sia moderare il contenuto che assegnare nuovi moderatori. |
| admin | Questo utente è un moderatore e può moderare il contenuto. |
| membro | Questo utente è inserito nell’elenco Consentiti. Il contenuto postato non passa attraverso filtri di spam o di profanità e non richiede l’approvazione in flussi pre-moderati. |
| nessuno | Questo utente è un utente standard e non dispone di autorizzazioni speciali. |
| emarginato | A questo utente è stato vietato di partecipare a qualsiasi conversazione. |

Per pubblicare le autorizzazioni degli utenti su sistemi esterni, è necessario registrare un URL che riceve i dati delle autorizzazioni come richieste di POST.

Ad esempio:

```
POST https://{networkName}.quill.fyre.co/?actor_token={token}&push_affiliation_url={url}
```

| Parametro | Descrizione |
|--- |--- |
| networkName | Il nome di rete fornito da Livefyre. |
| token | Token di sistema valido. |
| url | URL da registrare. |

L’URL registrato deve accettare i POST con i seguenti dati come tipo di contenuto: application/x-www-form-urlencoded.

| Parametro | Descrizione |
|--- |--- |
| jid | JID dell&#39;utente la cui affiliazione viene modificata. Un JID è una stringa del modulo `user_id@network`. |
| affiliazione | Nome delle autorizzazioni assegnate, che deve essere uno dei seguenti:  `{admin | member | none | outcast | owner}` |

Per ulteriori informazioni sull&#39;aggiornamento delle impostazioni di affiliazione degli utenti, consulta [Aggiungi riferimento API di affiliazione degli utenti](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:affiliation:add:method=post).
