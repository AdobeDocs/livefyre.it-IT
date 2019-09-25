---
description: Utilizza embed.ly per visualizzare più formati multimediali direttamente nell'app.
seo-description: Utilizza embed.ly per visualizzare più formati multimediali direttamente nell'app.
seo-title: Integrazione Embedly
solution: Experience Manager
title: Integrazione Embedly
uuid: 1f27e32c-c2c3-4f7c-93de-c9c7bf783d6a
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Integrazione Embedly{#embedly-integration}

Use `embed.ly` to display multiple media formats, directly in the App.

Per abilitare meglio i contenuti multimediali incorporati da diverse fonti, tra cui Google Maps, YouTube, Flickr, Facebook, Instagram, Spotify e Tumblr, le app Livefyre utilizzano Incorporatamente come provider di terze parti per l’espansione degli URL. Se un utente o un moderatore include un collegamento supportato in un post, i contenuti multimediali inclusi nel collegamento si espandono quando vengono inviati alla raccolta.

In questo modo, le app Livefyre possono accedere alle oltre 250 diverse opzioni di supporti incorporati supportate da Embedded.

>[!NOTE]
>
>Livefyre espande solo un sottoinsieme dell'elenco completo dei fornitori di Embedded. Le immagini incorporate si espanderanno sulle pagine HTTPS solo se il provider è Twitter, YouTube, Imgur, Vine, Wikipedia o SoundCloud. Per ulteriori informazioni sull'espansione dei collegamenti o sulle origini, contattate l'Account Manager tecnico.

In questa pagina sono riportati alcuni esempi di tipi di supporti incorporati diffusi e i relativi pattern URL accettabili. `Embed.ly` aggiunge continuamente nuove fonti. Per un elenco completo dei fornitori, visitate `https://embed.ly/embed/features/providers`.

>[!NOTE]
>
>La formattazione Incorporata richiede un collegamento permalink completo. I collegamenti abbreviati non funzioneranno.

È possibile incorporare solo contenuti visualizzabili al pubblico. Se tentate di incorporare un contenuto che non è pubblico, il collegamento al contenuto verrà visualizzato nel post del blog e verrà accompagnato da un'icona segnaposto. Quando un utente fa clic sul collegamento, il lettore riceve un messaggio di errore dal servizio in cui è ospitato il contenuto, ad esempio un messaggio Facebook per una foto solo per gli amici. Contattate l'Account Manager se notate che i supporti non sono espansi come previsto.

## URL incorporati di esempio

| Type (Tipo) | Provider | URL |
|--- |--- |--- |
| Mappe | Google Maps | <ul><li>`https://maps.google.com/maps?*`</li><li>`https://maps.google.com/?*`</li><li>`https://maps.google.com/maps/ms?*`</li></ul><br>**Nota**: L'URL deve iniziare con `http` e non con `https.` |
| Social Networking | Google Plus | <ul><li>`https://plus.google.com/*`</li><li>`https://www.google.com/profiles/*`</li><li> `https://plus.google.com/*`</li><li>`https://google.com/profiles/*`</li></ul> |
| Video | YouTube | <ul><li>`https://*youtube.com/watch*`</li><li> `https://*.youtube.com/v/*`</li><li>`https://*youtube.com/watch*` </li><li>`https://*.youtube.com/v/*`</li><li>`https://youtu.be/*`</li><li>`https://*.youtube.com/user/*` </li><li>`https://*.youtube.com/*#*/*`</li><li>`https://m.youtube.com/watch*`</li><li>`https://m.youtube.com/index*`</li><li>`https://*.youtube.com/profile*`</li><li>`https://*.youtube.com/view_play_list*`</li><li>`https://*.youtube.com/playlist*`</li></ul> |
| Foto | Flickr | `https://www.flickr.com/photos/*`<br>`https://flic.kr/*` |
|  | Instagram | `https://instagr.am/p/*`<br>`https://instagram.com/p/*` |
|  | TwitPic | <ul><li>`https://twitpic.com/*`</li><li>`https://www.twitpic.com/*`</li><li>`https://twitpic.com/photos/*`</li><li>`https://www.twitpic.com/photos/*`</li></ul> |
|  | Facebook | `https://www.facebook.com/photo.php*` |
|  | `Ow.ly` (Servizio di caricamento dei contenuti di Hootsuite) | `https://ow.ly/i/*` |
| Sondaggi | GoPollGo | `https://gopollgo.com/*`<br>`https://www.gopollgo.com/*` |
|  | Dropler | `https://d.pr/i/*` |
| Audio | SoundCloud | <ul><li>`https://soundcloud.com/*`</li><li>`https://soundcloud.com/*/*` </li><li>`https://soundcloud.com/*/sets/*` </li><li>`https://soundcloud.com/groups/*` </li><li>`https://snd.sc/*`</li></ul> |
|  | Spotify | `https://open.spotify.com/*` |
| Blog | Tumblr | `https://tumblr.com/*`<br>`https://*.tumblr.com/post/*` |

App che utilizzano questa funzione:

* [Carosello](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Commenti](/help/using/c-about-apps/c-comments/c-comments.md)
* [Scheda](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Mappa](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Muro di supporto](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaico](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Sondaggi](/help/using/c-about-apps/c-polls-app/c-polls-app.md#c_polls_app)
* [Recensioni](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Tendenza](/help/using/c-about-apps/c-trending-app/c-trending-app.md#c_trending_app)
* [Pulsante Carica](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

