---
description: Livefyre usa un'interfaccia PUSH per inviare informazioni sul sistema
  esterno sulle modifiche alle autorizzazioni dell'utente.
seo-description: Livefyre usa un'interfaccia PUSH per inviare informazioni sul sistema
  esterno sulle modifiche alle autorizzazioni dell'utente.
seo-title: Invio di autorizzazioni utente a sistemi esterni (facoltativo)
solution: Experience Manager
title: Invio di autorizzazioni utente a sistemi esterni (facoltativo)
uuid: 9 c 18 b 20 d -3 b 93-4666-b 7 de -1 ec 60318 cf 88
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Invio di autorizzazioni utente a sistemi esterni (facoltativo){#posting-user-permissions-to-external-systems-optional}

Livefyre usa un'interfaccia PUSH per inviare informazioni sul sistema esterno sulle modifiche alle autorizzazioni dell'utente.

## Tipi di utenti in Livefyre Studio

| Tipo utente | Descrizione |
|--- |--- |
| owner | Questo utente è proprietario e può moderare i contenuti e assegnare nuovi moderatori. |
| admin | Questo utente è moderatore e può moderare il contenuto. |
| membro | Questo utente è inserito nella white list. Il contenuto pubblicato non passa attraverso filtri spam o profasity e non richiede l'approvazione nei flussi premoderati. |
| none | Questo utente è un utente standard e non dispone di autorizzazioni speciali. |
| outcast | A questo utente è stato vietato di partecipare a conversazioni. |

Per pubblicare autorizzazioni utente per sistemi esterni, dovete registrare un URL che riceva dati di autorizzazioni come richieste POST.

Ad esempio:

```
POST https://{networkName}.quill.fyre.co/?actor_token={token}&push_affiliation_url={url}
```

| Parametro | Descrizione |
|--- |--- |
| Networkname | Il nome di rete fornito da Livefyre. |
| token | Token di sistema valido. |
| url | URL per la registrazione. |

L'URL registrato deve accettare POST con i seguenti dati come tipo di contenuto: application/x-www-form-urlencoded.

| Parametro | Descrizione |
|--- |--- |
| jid | JID dell'utente la cui filiale viene modificata. Un JID è una stringa del modulo `user_id@network`. |
| affiliazione | Nome delle autorizzazioni assegnate, che devono essere una delle seguenti: `{admin | member | none | outcast | owner}` |

Per ulteriori informazioni sull'aggiornamento delle impostazioni di affiliazione degli utenti, consultate [Aggiunta di riferimento API di affiliazione utente](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:affiliation:add:method=post).
