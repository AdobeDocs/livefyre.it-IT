---
description: Utilizza embed.ly per visualizzare più formati multimediali direttamente
  nell'app.
seo-description: Utilizza embed.ly per visualizzare più formati multimediali direttamente
  nell'app.
seo-title: Integrazione Embedly
solution: Experience Manager
title: Integrazione Embedly
uuid: 1 f 27 e 32 c-c 2 c 3-4 f 7 c -93 de-c 9 c 7 bf 783 d 6 a
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Integrazione Embedly{#embedly-integration}

Utilizzate `embed.ly` per visualizzare più formati multimediali direttamente nell'app.

Per abilitare meglio il contenuto multimediale incorporato da una varietà di fonti, inclusi Google Maps, YouTube, Flickr, Facebook, Instagram, Spotify e Tumblr, Livefyre Apps utilizza Embedly come fornitore di terze parti per l'espansione URL. Se un utente o un moderatore include un collegamento supportato in un post, il supporto incluso nel collegamento si espande quando viene inviato alla raccolta.

In questo modo Livefyre Apps consente di accedere alle più di 250 diverse opzioni multimediali incorporate supportate da Incorporare.

>[!NOTE]
>
>Livefyre espande solo un sottoinsieme dell'elenco completo dei fornitori. Le immagini incorporate si espandono su pagine HTTPS solo se il fornitore è Twitter, YouTube, Imgur, Vine, Wikipedia o soundcloud. Per ulteriori domande sull'espansione o le origini dei collegamenti, contattate il vostro Account Manager tecnico.

In questa pagina sono riportati alcuni esempi di tipi di supporti incorporati più diffusi e i pattern URL accettabili. `Embed.ly` sta aggiungendo continuamente nuove sorgenti. Per un elenco completo dei fornitori `https://embed.ly/embed/features/providers`, visitate.

>[!NOTE]
>
>La formattazione incorporata richiede un'inchiostro completa. I collegamenti abbreviati non funzioneranno.

È possibile incorporare solo contenuti visualizzabili pubblicamente. Se tentate di incorporare un contenuto non pubblico, il collegamento al contenuto verrà visualizzato nel post di blog e un'icona segnaposto lo accompagnerà. Quando un utente fa clic su di esso, il collegamento porta il lettore a un messaggio di errore dal servizio in cui è ospitato il contenuto, ad esempio un messaggio Facebook per una foto solo per gli amici. Contattate l'Account Manager se notate che i supporti non sono espansi come previsto.

## URL con incorporazione di esempio

| Tipo | Fornitore | URL |
|--- |--- |--- |
| Mappe | Google Maps | <ul><li>`https://maps.google.com/maps?*`</li><li>`https://maps.google.com/?*`</li><li>`https://maps.google.com/maps/ms?*`</li></ul><br>**Nota**: L'URL deve iniziare con `http` e non `https.` |
| Social network | Google Plus | <ul><li>`https://plus.google.com/*`</li><li>`https://www.google.com/profiles/*`</li><li> `https://plus.google.com/*`</li><li>`https://google.com/profiles/*`</li></ul> |
| Video | YouTube | <ul><li>`https://*youtube.com/watch*`</li><li> `https://*.youtube.com/v/*`</li><li>`https://*youtube.com/watch*` </li><li>`https://*.youtube.com/v/*`</li><li>`https://youtu.be/*`</li><li>`https://*.youtube.com/user/*` </li><li>`https://*.youtube.com/*#*/*`</li><li>`https://m.youtube.com/watch*`</li><li>`https://m.youtube.com/index*`</li><li>`https://*.youtube.com/profile*`</li><li>`https://*.youtube.com/view_play_list*`</li><li>`https://*.youtube.com/playlist*`</li></ul> |
| Foto | Flickr | `https://www.flickr.com/photos/*`<br>`https://flic.kr/*` |
|  | Instagram | `https://instagr.am/p/*`<br>`https://instagram.com/p/*` |
|  | Twitpic | <ul><li>`https://twitpic.com/*`</li><li>`https://www.twitpic.com/*`</li><li>`https://twitpic.com/photos/*`</li><li>`https://www.twitpic.com/photos/*`</li></ul> |
|  | Facebook | `https://www.facebook.com/photo.php*` |
|  | `Ow.ly` (Servizio caricamento contenuto di Hootsuite) | `https://ow.ly/i/*` |
| Sondaggi | Gopollgo | `https://gopollgo.com/*`<br>`https://www.gopollgo.com/*` |
|  | Droplr | `https://d.pr/i/*` |
| Audio | Soundcloud | <ul><li>`https://soundcloud.com/*`</li><li>`https://soundcloud.com/*/*` </li><li>`https://soundcloud.com/*/sets/*` </li><li>`https://soundcloud.com/groups/*` </li><li>`https://snd.sc/*`</li></ul> |
|  | Spotify | `https://open.spotify.com/*` |
| Blog | Tumblr | `https://tumblr.com/*`<br>`https://*.tumblr.com/post/*` |

App che utilizzano questa funzione:

* [Carosello](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Commenti](/help/using/c-about-apps/c-comments/c-comments.md)
* [Scheda Funzioni](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Mappa](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Media Wall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaic](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Sondaggi](/help/using/c-about-apps/c-polls-app/c-polls-app.md#c_polls_app)
* [Recensioni](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Tendenza](/help/using/c-about-apps/c-trending-app/c-trending-app.md#c_trending_app)
* [Pulsante Carica](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)
