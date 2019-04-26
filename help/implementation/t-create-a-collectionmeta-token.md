---
description: Create una nuova raccolta creando un token collectionmeta passato a Livefyre.
seo-description: Create una nuova raccolta creando un token collectionmeta passato
  a Livefyre.
seo-title: Creare una raccolta utilizzando il token collectionmeta
solution: Experience Manager
title: Creare una raccolta utilizzando il token collectionmeta
uuid: 5 a 3 e 18 e 8-8568-45 bb -9070-d 0 fa 43 dd 819 b
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e

---


# Creare una raccolta utilizzando il token collectionmeta{#create-a-collection-using-the-collectionmeta-token}

Create una nuova raccolta creando un token collectionmeta passato a Livefyre.

1. Create il token collectionmeta.
1. Creare il checksum.

   Il checksum è richiesto se desiderate inviare a Livefyre qualsiasi modifica apportata alla vostra raccolta. Livefyre aggiorna la raccolta solo se il checksum fornito è diverso da quello inviato in precedenza. La creazione di un checksum è esattamente come creare `collectionMeta` un token, ma invece di `buildCollectionMetaToken` chiamarvi `buildChecksum`.

Creare token utente per l'autenticazione in Livefyre.