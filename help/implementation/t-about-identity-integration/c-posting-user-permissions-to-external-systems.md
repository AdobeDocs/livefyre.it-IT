---
description: Livefyre utilizza un'interfaccia PUSH per inviare a un sistema esterno informazioni sulle modifiche apportate alle autorizzazioni degli utenti.
seo-description: Livefyre utilizza un'interfaccia PUSH per inviare a un sistema esterno informazioni sulle modifiche apportate alle autorizzazioni degli utenti.
seo-title: Registrazione delle autorizzazioni utente a sistemi esterni (facoltativo)
solution: Experience Manager
title: Registrazione delle autorizzazioni utente a sistemi esterni (facoltativo)
uuid: 9c18b20d-3b93-4666-b7de-1ec60318cf88
translation-type: tm+mt
source-git-commit: 52f59cd15f315aa93be198f6eb586f008c18a384
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 3%

---


# Registrazione delle autorizzazioni utente a sistemi esterni (facoltativo){#posting-user-permissions-to-external-systems-optional}

Livefyre utilizza un&#39;interfaccia PUSH per inviare a un sistema esterno informazioni sulle modifiche apportate alle autorizzazioni degli utenti.

## Tipi di utenti in Livefyre Studio

| Tipo utente | Descrizione |
|--- |--- |
| proprietario | Questo utente è proprietario e può moderare i contenuti e assegnare nuovi moderatori. |
| admin | Questo utente è un moderatore e può moderare il contenuto. |
| membro | Questo utente è incluso nell&#39;elenco dei permessi. Il contenuto registrato non passa attraverso filtri di spam o di profanità e non richiede l&#39;approvazione nei flussi pre-moderati. |
| none | Questo utente è un utente standard e non dispone di autorizzazioni speciali. |
| emarginato | A questo utente è stato vietato di partecipare a qualsiasi conversazione. |

Per pubblicare le autorizzazioni degli utenti nei sistemi esterni, dovete registrare un URL che riceve i dati delle autorizzazioni come richieste POST.

Ad esempio:

```
POST https://{networkName}.quill.fyre.co/?actor_token={token}&push_affiliation_url={url}
```

| Parametro | Descrizione |
|--- |--- |
| networkName | Il nome di rete fornito da Livefyre. |
| token | Token di sistema valido. |
| url | URL per la registrazione. |

L’URL registrato deve accettare i POST con i seguenti dati come tipo di contenuto: application/x-www-form-urlencoded.

| Parametro | Descrizione |
|--- |--- |
| jid | JID dell&#39;utente la cui affiliazione viene modificata. Un JID è una stringa del modulo `user_id@network`. |
| affiliazione | Nome delle autorizzazioni assegnate, che deve essere una delle seguenti:  `{admin | member | none | outcast | owner}` |

Per ulteriori informazioni sull’aggiornamento delle impostazioni di affiliazione degli utenti, consultate [Aggiungi riferimento](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:affiliation:add:method=post)API di affiliazione utenti.
