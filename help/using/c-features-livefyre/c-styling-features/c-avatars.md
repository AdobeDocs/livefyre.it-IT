---
description: Consente agli utenti di personalizzare l'immagine visualizzata con il relativo contenuto.
title: Avatar
exl-id: cff7f6be-3660-4d71-949b-6ac04379d68d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# Avatars{#avatars}

Consente agli utenti di personalizzare l&#39;immagine visualizzata con il relativo contenuto.

Gli avatar utente vengono visualizzati (per impostazione predefinita) accanto al contenuto in tutte le app e vengono estratti dal sistema di profili di identità utilizzato nell&#39;implementazione. Le dimensioni di questi avatar variano a seconda dell’app in cui vengono visualizzati.

(Livefyre ti consente di disattivare gli Avatar se non desideri visualizzarli nelle tue app.)

>[!NOTE]
>
>Gli avatar vengono visualizzati a 25p x 25p per Chat e 50p x 50p nella maggior parte delle altre app.

## Archiviazione avatar {#section_zbh_x1f_wy}

Gli avatar vengono caricati in modo asincrono in Livefyre. Quando un utente accede per la prima volta all’app o modifica il file immagine avatar associato, l’immagine del profilo viene aggiunta a una coda di attività. (Un avatar predefinito viene visualizzato temporaneamente mentre quello dell’utente viene caricato nella posizione di archiviazione dell’avatar Livefyre.)

## Gravati {#section_mqh_p1f_wy}

Livefyre supporta l&#39;uso di Gravatars. Se un utente non dispone di un avatar personalizzato come parte del suo profilo utente, Livefyre controllerà la presenza di un Gravatar per quell’utente. Se non esiste un Gravatar, verrà utilizzato l&#39;avatar predefinito.


App che utilizzano questa funzione:

* [Carosello](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Commenti](/help/using/c-about-apps/c-comments/c-comments.md)
* [Scheda tecnica](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Mappa](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Parete multimediale](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaico](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Recensioni](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Memorizza 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
