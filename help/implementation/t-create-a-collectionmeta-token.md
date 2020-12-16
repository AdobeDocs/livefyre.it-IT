---
description: Create una nuova raccolta creando un token collectionMeta che viene passato a Livefyre.
seo-description: Create una nuova raccolta creando un token collectionMeta che viene passato a Livefyre.
seo-title: Creare una raccolta utilizzando CollectionMeta Token
solution: Experience Manager
title: Creare una raccolta utilizzando CollectionMeta Token
uuid: 5a3e18e8-8568-45bb-9070-d0fa43dd819b
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# Creare una raccolta utilizzando CollectionMeta Token{#create-a-collection-using-the-collectionmeta-token}

Create una nuova raccolta creando un token collectionMeta che viene passato a Livefyre.

1. Create il token collectionMeta.
1. Create il checksum.

   Il checksum è richiesto se desiderate notificare a Livefyre eventuali modifiche apportate alla raccolta. Livefyre aggiornerà la raccolta solo se il checksum fornito è diverso dal checksum inviato in precedenza. Creare un checksum è come creare un token `collectionMeta`, ma invece di chiamare `buildCollectionMetaToken` si chiama `buildChecksum`.

Create token utente per l&#39;autenticazione in Livefyre.