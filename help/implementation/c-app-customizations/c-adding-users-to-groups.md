---
description: Aggiungete un tag utente a un account per aggiungere un utente a un gruppo.
seo-description: Aggiungete un tag utente a un account per aggiungere un utente a un gruppo.
seo-title: Aggiunta di utenti a gruppi
solution: Experience Manager
title: Aggiunta di utenti a gruppi
uuid: 3633 f 2 df -8 d 60-4 cdd-b 9 a 2-3807218 c 74 a 0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Aggiunta di utenti a gruppi{#adding-users-to-groups}

Aggiungete un tag utente a un account per aggiungere un utente a un gruppo.

I tag utente possono essere implementati sia per i sistemi di profilo proprietari che per quelli enterprise e possono essere aggiunti agli account in vari modi:

* La creazione di proprietari e moderatori tramite Studio assegna all&#39;account il tag utente «Moderatore».
* La creazione di gruppi di utenti e l&#39;aggiunta di utenti tramite Studio applicano automaticamente i tag utente con il nome del gruppo agli utenti selezionati.
* I tag utente possono essere applicati direttamente agli account utilizzando la [chiamata Aggiungi tag](https://api.livefyre.com/docs#add-user-tag) utente utente o Ping per Pull.

>[!NOTE]
>
>Entrambi i metodi API, la chiamata HTTP Aggiungi tag e il metodo Ping for Pull, sovrascriveranno i tag precedentemente assegnati all&#39;account tramite altri mezzi. Pertanto, selezionate un metodo e utilizzatelo in modo coerente durante il processo.

## Aggiungere un utente a un gruppo dalla pagina Utenti in Studio {#section_qgq_nbw_xz}

* Fate clic **[!UICONTROL Add Group]** sull&#39;etichetta del gruppo sotto qualsiasi nome utente per aprire il menu dei gruppi.
* Scorrete l&#39;elenco e individuate il gruppo al quale desiderate aggiungere l&#39;utente. Potete inserire un nome di gruppo nella **[!UICONTROL Search]** casella nella parte superiore del menu a discesa.
* Fai clic sulla casella di controllo accanto ai gruppi ai quali l&#39;utente deve aggiungere l&#39;utente e premi Invio.

Il profilo dell&#39;utente visualizza il nome del gruppo (se l&#39;utente è solo in un gruppo) o il numero di gruppi a cui appartiene l&#39;utente.

## Aggiungere un utente a un gruppo utilizzando la chiamata Aggiungi tag utente {#section_kn3_gbw_xz}

Passate il token lftoken dell&#39;utente e il nome del tag selezionato con la richiesta POST

Ad esempio:

```
curl -XPOST -d 'tag_name=tag&lftoken=eyJhbGciOiAiA_TOKENcGlyZXMiOiAxMzU3OTY3NTAxLjIzn0.KoyXUVCavt-rdvkVXm2qzQTyMAOSp-crQA1uL1ht9WU' 'https://labs.quill.fyre.co/api/v3.0/author/system@`labs.fyre.co`/tag/'
```


Per ulteriori informazioni, consultate Riferimento API &gt; [Aggiungi tag utente](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:author:tags:method=post).

## Aggiungere un utente a un gruppo utilizzando Ping per Pull {#section_kyj_11w_xz}

Utilizzate l&#39;array tag per assegnare utenti a gruppi di utenti. (I tag possono includere caratteri alfanumerici e caratteri di sottolineatura 1-63).

Ad esempio:

```
"tags": ["moderator", "brand_advocate"],
```

## Aggiungere un utente a un gruppo utilizzando Profili remoti {#section_uyn_scv_xz}

Aggiungi tag utente al profilo remoto, utilizzati per sincronizzare i dati utente tra il sistema di profilo personalizzato e Livefyre, per gli utenti specifici.
