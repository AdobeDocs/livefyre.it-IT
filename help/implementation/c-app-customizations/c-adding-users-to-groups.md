---
description: Aggiungi un tag utente a un account per aggiungere un utente a un gruppo.
title: Aggiunta di utenti ai gruppi
exl-id: 6e799c77-e815-40c2-ae06-bbd076df9fe7
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 1%

---

# Aggiunta di utenti ai gruppi{#adding-users-to-groups}

Aggiungi un tag utente a un account per aggiungere un utente a un gruppo.

I tag utente possono essere implementati sia per i sistemi di profilo proprietari che per quelli aziendali e possono essere aggiunti agli account in diversi modi:

* La creazione di proprietari e moderatori tramite Studio assegna il tag utente &quot;Moderatore&quot; all’account.
* La creazione di gruppi di utenti e l’aggiunta di utenti tramite Studio applica automaticamente agli utenti selezionati i tag utente con il nome del gruppo.
* I tag utente possono anche essere applicati direttamente agli account utilizzando la chiamata [Aggiungi tag utente HTTP](https://api.livefyre.com/docs#add-user-tag) o Ping for Pull.

>[!NOTE]
>
>Entrambi i metodi API, la chiamata HTTP Add User Tag e il metodo Ping for Pull, sovrascriveranno tutti i tag precedentemente assegnati all’account tramite altri metodi. Pertanto, seleziona un metodo e utilizzalo in modo coerente durante l&#39;intero processo.

## Aggiungere un utente a un gruppo dalla pagina Utenti in Studio {#section_qgq_nbw_xz}

* Fai clic su **[!UICONTROL Add Group]** o sull&#39;etichetta del gruppo sotto qualsiasi nome utente per aprire il menu dei gruppi.
* Scorri l’elenco e trova il gruppo a cui desideri aggiungere l’utente. È possibile immettere un nome di gruppo nella casella **[!UICONTROL Search]** nella parte superiore del menu a discesa.
* Fai clic sulla casella di controllo accanto al gruppo o ai gruppi a cui deve essere aggiunto l’utente e premi Invio.

Il profilo dell’utente visualizza il nome del gruppo (se l’utente si trova in un solo gruppo) o il numero di gruppi a cui appartiene l’utente.

## Aggiungi un utente a un gruppo utilizzando la chiamata Aggiungi tag utente {#section_kn3_gbw_xz}

Passa il collegamento LFToken dell’utente e il nome del tag selezionato in con la richiesta POST

Ad esempio:

```
curl -XPOST -d 'tag_name=tag&lftoken=eyJhbGciOiAiA_TOKENcGlyZXMiOiAxMzU3OTY3NTAxLjIzn0.KoyXUVCavt-rdvkVXm2qzQTyMAOSp-crQA1uL1ht9WU' 'https://labs.quill.fyre.co/api/v3.0/author/system@`labs.fyre.co`/tag/'
```


Per ulteriori informazioni, consulta Riferimento API > [Aggiungi tag utente](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:author:tags:method=post).

## Aggiungi un utente a un gruppo utilizzando Ping per Pull {#section_kyj_11w_xz}

Utilizzare l&#39;array tags per assegnare gli utenti ai gruppi di utenti. I tag possono contenere da 1 a 63 caratteri alfanumerici e caratteri di sottolineatura.

Ad esempio:

```
"tags": ["moderator", "brand_advocate"],
```

## Aggiungi un utente a un gruppo utilizzando i profili remoti {#section_uyn_scv_xz}

Aggiungi i tag utente al profilo remoto, utilizzato per sincronizzare i dati utente tra il tuo sistema di profilo personalizzato e Livefyre, per gli utenti specifici.
