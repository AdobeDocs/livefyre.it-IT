---
description: Aggiungete un tag utente a un account per aggiungere un utente a un gruppo.
seo-description: Aggiungete un tag utente a un account per aggiungere un utente a un gruppo.
seo-title: Aggiunta di utenti ai gruppi
solution: Experience Manager
title: Aggiunta di utenti ai gruppi
uuid: 3633f2df-8d60-4cdd-b9a2-3807218c74a0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 1%

---


# Aggiunta di utenti a gruppi{#adding-users-to-groups}

Aggiungete un tag utente a un account per aggiungere un utente a un gruppo.

I tag utente possono essere implementati sia per i sistemi di profilo proprietario che per quelli aziendali e possono essere aggiunti agli account in diversi modi:

* La creazione di proprietari e moderatori tramite Studio assegna il tag utente &quot;Moderatore&quot; all&#39;account.
* La creazione di gruppi di utenti e l’aggiunta di utenti tramite Studio applica automaticamente agli utenti selezionati i tag utente con il nome del gruppo.
* I tag utente possono essere applicati direttamente agli account utilizzando la chiamata [Aggiungi tag utente HTTP](https://api.livefyre.com/docs#add-user-tag) o Ping for Pull.

>[!NOTE]
>
>Entrambi i metodi API, la chiamata HTTP Add User Tag e il metodo Ping for Pull, sovrascriveranno tutti i tag precedentemente assegnati all&#39;account tramite altri metodi. Selezionare un metodo e utilizzarlo in modo coerente durante l&#39;intero processo.

## Aggiungere un utente a un gruppo dalla pagina Utenti in Studio {#section_qgq_nbw_xz}

* Fate clic su **[!UICONTROL Add Group]** o sull&#39;etichetta del gruppo sotto qualsiasi nome utente per aprire il menu dei gruppi.
* Scorrete l’elenco e individuate il gruppo al quale desiderate aggiungere l’utente. Potete immettere un nome di gruppo nella casella **[!UICONTROL Search]** nella parte superiore del menu a discesa.
* Fate clic sulla casella di controllo accanto al gruppo o ai gruppi a cui aggiungere l’utente e premete Invio.

Nel profilo dell’utente viene visualizzato il nome del gruppo (se l’utente si trova in un solo gruppo) o il numero di gruppi a cui appartiene l’utente.

## Aggiunta di un utente a un gruppo tramite la chiamata Aggiungi tag utente {#section_kn3_gbw_xz}

Passa il nome LFToken dell’utente e il nome del tag selezionato con la richiesta del POST

Ad esempio:

```
curl -XPOST -d 'tag_name=tag&lftoken=eyJhbGciOiAiA_TOKENcGlyZXMiOiAxMzU3OTY3NTAxLjIzn0.KoyXUVCavt-rdvkVXm2qzQTyMAOSp-crQA1uL1ht9WU' 'https://labs.quill.fyre.co/api/v3.0/author/system@`labs.fyre.co`/tag/'
```


Per ulteriori informazioni, consultate Riferimento API > [Aggiungi tag utente](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:author:tags:method=post).

## Aggiunta di un utente a un gruppo utilizzando Ping per pull {#section_kyj_11w_xz}

Utilizzate l&#39;array tags per assegnare gli utenti ai gruppi di utenti. I tag possono contenere da 1 a 63 caratteri alfanumerici e caratteri di sottolineatura.

Ad esempio:

```
"tags": ["moderator", "brand_advocate"],
```

## Aggiunta di un utente a un gruppo utilizzando i profili remoti {#section_uyn_scv_xz}

Aggiungete i tag utente al profilo remoto, utilizzato per sincronizzare i dati utente tra il sistema del profilo personalizzato e Livefyre, per gli utenti specifici.
