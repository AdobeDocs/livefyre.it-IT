---
description: Consente agli utenti di personalizzare l’immagine visualizzata con il relativo contenuto.
seo-description: Consente agli utenti di personalizzare l’immagine visualizzata con il relativo contenuto.
seo-title: Avatar
title: Avatar
uuid: bf20f3bc-3dcc-4e16-a629-3380d1a7a3f2
translation-type: tm+mt
source-git-commit: 7dc3ac6725a27460cecfa6051549da85370ca053

---


# Avatar{#avatars}

Consente agli utenti di personalizzare l’immagine visualizzata con il relativo contenuto.

Gli avatar degli utenti vengono visualizzati (per impostazione predefinita) accanto al contenuto in tutte le app e vengono estratti dal sistema del profilo di identità utilizzato nell'implementazione. Questi avatar hanno dimensioni diverse, a seconda dell'app in cui sono visualizzati.

(Livefyre consente di disattivare gli Avatar se non si desidera visualizzarli nelle app.)

>[!NOTE]
>
>Gli avatar sono visualizzati a 25p x 25p per Chat e 50p x 50p nella maggior parte delle altre app.

## Archiviazione Avatar {#section_zbh_x1f_wy}

Gli avatar vengono caricati in modo asincrono in Livefyre. Quando un utente accede per la prima volta all'app o modifica il file immagine avatar associato, l'immagine del profilo viene aggiunta a una coda di attività. (Un avatar predefinito viene visualizzato temporaneamente mentre quello dell’utente viene caricato nel percorso di memorizzazione dell’avatar di Livefyre).

## Gravatar {#section_mqh_p1f_wy}

Livefyre supporta l'uso dei Gravatars. Se un utente non dispone di un avatar personalizzato come parte del suo profilo utente, Livefyre verificherà la presenza di un Gravatar per tale utente. Se non esiste un Gravatar, verrà utilizzato l'avatar predefinito.


App che utilizzano questa funzione:

* [Carosello](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Commenti](/help/using/c-about-apps/c-comments/c-comments.md)
* [Scheda](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Mappa](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Muro di supporto](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaico](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Recensioni](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)

