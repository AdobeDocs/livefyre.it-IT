---
description: Genera il Ping per la risposta Pull per trasmettere informazioni utente aggiornate a Livefyre.
title: Creare il ping per la risposta di pull
exl-id: 81c398fd-2acb-4e39-a2b3-c96921b1192b
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 1%

---

# Creare il ping per la risposta di pull{#build-the-ping-for-pull-response}

Genera il Ping per la risposta Pull per trasmettere informazioni utente aggiornate a Livefyre.

| Type (Tipo) | Proprietà | Descrizione |
|--- |--- |--- |
| Stringa *obbligatoria* | id | ID utente dell’utente nel sistema del profilo. Deve essere univoco per tutti gli utenti della rete e non deve mai essere modificato. |
| Stringa *obbligatoria* | nome_visualizzato | Nome visualizzato dell&#39;utente. Questo verrà riprodotto con il contenuto Livefyre pubblicato dall’utente. |
| Oggetto *facoltativo, ma consigliato* | name | Stringhe per definire i nomi formattati, i nomi, i nomi e i cognomi dell’utente. |
| Stringa *facoltativa, ma consigliata* | e-mail | Indirizzo e-mail dell’utente. Utilizzato per inviare notifiche e-mail. |
| Stringa *facoltativa, ma consigliata* | image_url | URL di un avatar da visualizzare per l’utente. Livefyre ridimensiona le immagini caricate a 100×100, 75×75 o 50×50 pixel, a seconda dei casi. Per risultati migliori, gli utenti devono caricare un&#39;immagine quadrata, a 100×100 pixel. Per assicurarsi che l&#39;immagine avatar sia aggiornata in Livefyre, modifica l&#39;image_url per ogni aggiornamento dell&#39;immagine in modo che Ping for Pull rilevi che l&#39;immagine è stata modificata. Ad esempio, allega una marca temporale al nome del file o incrementa le modifiche dell’immagine. Nota:  Tutti gli URL devono essere completi e accessibili. |
| Stringa *facoltativa, ma consigliata* | profile_url | URL della pagina del profilo dell’utente sul sito. |
| Stringa *facoltativa, ma consigliata* | settings_url | URL a una pagina in cui gli utenti possono configurare le impostazioni del profilo dell’utente per il sito. |
| Array *facoltativo, ma consigliato* | tag | Utilizzato per assegnare gli utenti a gruppi di utenti. I tag possono includere da 1 a 63 caratteri alfanumerici e caratteri di sottolineatura. |
| Booleano *facoltativo, ma consigliato* | autofollow_conversations | Definisce se un utente desidera seguire automaticamente una raccolta dopo la pubblicazione. Quando segue una raccolta, gli utenti ricevono notifiche e-mail quando altri utenti partecipano. Può essere vero o falso. Predefinito su true. |
| Oggetto *facoltativo, ma consigliato* | email_notifications | Definisce la frequenza delle notifiche e-mail Livefyre disponibili. Per ciascun tipo di notifica possono essere fissate frequenze diverse. Per impostazione predefinita, non vengono inviate notifiche. <br><ul><li> invia immediatamente le notifiche immediatamente dopo l’evento elencato. </li><li>invia spesso notifiche in batch. </li><li> non invierà mai notifiche e-mail per l’attività. </li><li>*commenti*: Definisce quando vengono inviate notifiche quando altri utenti inseriscono contenuto nelle raccolte che l’utente sta seguendo. </li><li>*risposte*: Definisce quando vengono inviate notifiche quando un altro utente risponde al contenuto di questo utente.</li><li>*Mi piace*: Definisce quando vengono inviate notifiche quando un altro utente ama il contenuto di questo utente.</li><li>*moderator_comments*: Definisce quando le notifiche vengono inviate ai moderatori quando gli utenti pubblicano contenuti a qualsiasi raccolta nella rete.</li><li>*moderatore_flag*: Definisce quando le notifiche vengono inviate ai moderatori quando altri utenti contrassegnano il contenuto in qualsiasi raccolta nella rete.</li></ul> |
| Stringa *opzionale* | la posizione | Una posizione inviata dall’utente. |
| Stringa *opzionale* | bio | Autobiografia inviata dall’utente. |
| Array *facoltativo* | siti web | Matrice di siti inviati dall’utente. Max = 2. |
| Oggetto *facoltativo* | display_rules | Definisce quali proprietà di profilo sono visibili pubblicamente ad altri utenti. Ogni parametro disponibile accetta l’input booleano true o false. Parametri disponibili:  <br><ul><li>bio </li><li> la posizione</li><li>  genere </li><li>nameimage </li><li> remote_profile_url</li></ul> |
| Booleano *facoltativo* | moderatore | Definisce se l&#39;utente dispone di privilegi di moderatore nella rete. |
| Booleano *facoltativo* | gravatar_disabled | Definisce se disabilitare l&#39;uso di un gravatar da parte di Livefyre se non viene fornito alcun image_url. |

## Risposta di esempio {#section_uxt_3dd_mz}

```
{
 "id": "1234567890",
 "display_name": "Bob Dole",
 "name": {
   "formatted": "Bob Joseph Dole",
   "first": "Bob",
   "middle": "Joseph",
   "last": "Dole"
 },
   "email": "bob@dole.com",
   "image_url": "https://dole.com/images/bob.jpg",
   "profile_url": "https://site.com/bobdole",
   "settings_url":"https://site.com/settings",
   "tags": ["bob", "dole"],
   "autofollow_conversations": "true",
   "email_notifications": {
      "comments": "never",
      "replies": "immediately",
      "likes": "often",
      "moderator_comments": "immediately",
      "moderator_flags": "immediately" 
 },
  "location": "Washington D.C., USA",
  "bio": "Bob Dole speaks in the third person",
  "websites": ["https://dole.com/blog/", "https://bobdolerocks.com"],
  "display_rules": {
      "bio": "false",
      "location": "false",
      "gender": "false",
      "name": "false",
      "image": "false",
      "remote_profile_url": "false"
  },
  "moderator": "true",
  "gravatar_disabled": "false"
}
```
