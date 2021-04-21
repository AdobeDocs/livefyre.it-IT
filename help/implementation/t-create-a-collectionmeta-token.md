---
description: Crea una nuova raccolta creando un token collectionMeta che viene passato a Livefyre.
title: Creare una raccolta utilizzando il token CollectionMeta
exl-id: d2dafc90-de21-4998-8e85-83f970524329
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# Creare una raccolta utilizzando il token CollectionMeta{#create-a-collection-using-the-collectionmeta-token}

Crea una nuova raccolta creando un token collectionMeta che viene passato a Livefyre.

1. Crea il token collectionMeta.
1. Crea il checksum.

   Il checksum è necessario se desideri notificare a Livefyre eventuali modifiche apportate alla tua Raccolta. Livefyre aggiornerà la raccolta solo se il checksum fornito è diverso dal checksum inviato in precedenza. La creazione di un checksum è simile alla creazione di un token `collectionMeta` ma invece di chiamare `buildCollectionMetaToken` chiama `buildChecksum`.

Crea token utente per l’autenticazione in Livefyre.
