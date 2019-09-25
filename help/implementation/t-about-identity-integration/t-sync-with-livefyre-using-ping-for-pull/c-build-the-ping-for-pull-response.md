---
description: Create la risposta Ping for Pull per trasmettere informazioni aggiornate degli utenti a Livefyre.
seo-description: Create la risposta Ping for Pull per trasmettere informazioni aggiornate degli utenti a Livefyre.
seo-title: Creare il ping per la risposta pull
solution: Experience Manager
title: Creare il ping per la risposta pull
uuid: f90871d5-601f-40dc-b3d2-ab78635e4a88
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Creare il ping per la risposta pull{#build-the-ping-for-pull-response}

Create la risposta Ping for Pull per trasmettere informazioni aggiornate degli utenti a Livefyre.

| Type (Tipo) | Proprietà | Descrizione |
|--- |--- |--- |
| Stringa *richiesta* | id | L’ID utente dell’utente nel sistema del profilo. Deve essere univoco per tutti gli utenti della rete e non deve mai essere modificato. |
| Stringa *richiesta* | display_name | Nome visualizzato dell'utente. Questo verrà rappresentato con il contenuto Livefyre pubblicato dall'utente. |
| Oggetto *facoltativo, ma consigliato* | name | Stringhe per definire il nome formattato, il nome, il centro e il cognome dell'utente. |
| Stringa *facoltativa, ma consigliata* | e-mail | Indirizzo e-mail dell’utente. Utilizzato per inviare le notifiche e-mail. |
| Stringa *facoltativa, ma consigliata* | image_url | URL di un avatar da visualizzare per l’utente. Livefyre ridimensiona le immagini caricate a 100×100, 75×75 o 50×50 pixel, a seconda dei casi. Per risultati ottimali, gli utenti devono caricare un’immagine quadrata a 100×100 pixel. Per fare in modo che l'immagine avatar venga aggiornata in Livefyre, modificate image_url per ogni aggiornamento immagine in modo che Ping for Pull rilevi che l'immagine è stata modificata. Ad esempio, allegare una marca temporale al nome del file o incrementare le modifiche apportate alle immagini. Nota:  Tutti gli URL devono essere completi e accessibili. |
| Stringa *facoltativa, ma consigliata* | profile_url | URL della pagina del profilo utente sul sito. |
| Stringa *facoltativa, ma consigliata* | settings_url | URL a una pagina in cui gli utenti possono configurare le impostazioni del profilo dell’utente per il sito. |
| Array *facoltativo, ma consigliato* | tags | Utilizzato per assegnare utenti a gruppi di utenti. I tag possono includere da 1 a 63 caratteri alfanumerici e caratteri di sottolineatura. |
| Booleano *facoltativo, ma consigliato* | autofollow_conversations | Definisce se un utente desidera seguire automaticamente una raccolta dopo averla pubblicata. Quando si segue una raccolta, gli utenti ricevono notifiche e-mail quando altri utenti partecipano. Può essere vero o falso. Il valore predefinito è true. |
| Oggetto *facoltativo, ma consigliato* | email_notifications | Definisce la frequenza delle notifiche e-mail Livefyre disponibili. Per ogni tipo di notifica possono essere impostate frequenze diverse. Per impostazione predefinita, non vengono inviate notifiche. <br><ul><li> invia immediatamente le notifiche immediatamente dopo l’evento elencato. </li><li>invia spesso notifiche in batch. </li><li> mai non invierà notifiche e-mail per l'attività. </li><li>*commenti*: Definisce quando le notifiche vengono inviate quando altri utenti inseriscono contenuto nelle raccolte che l'utente segue. </li><li>*risposte*: Definisce quando le notifiche vengono inviate quando un altro utente risponde al contenuto di questo utente.</li><li>*Mi piace*: Definisce quando le notifiche vengono inviate quando un altro utente ama il contenuto di questo utente.</li><li>*moderator_comments*: Definisce quando le notifiche vengono inviate ai moderatori quando gli utenti inviano contenuto a qualsiasi raccolta nella rete.</li><li>*moderator_flags*: Definisce quando le notifiche vengono inviate ai moderatori quando altri utenti contrassegnano il contenuto in qualsiasi raccolta della rete.</li></ul> |
| Stringa *facoltativa* | la posizione | Un percorso inviato dall’utente. |
| Stringa *facoltativa* | bio | Autobiografia inviata dall’utente. |
| Array *facoltativo* | siti Web | Un array di siti inviati dall’utente. Max = 2. |
| Oggetto *facoltativo* | display_rules | Definisce le proprietà del profilo visibili pubblicamente agli altri utenti. Ogni parametro disponibile accetta l'input booleano true o false. Parametri disponibili:  <br><ul><li>bio </li><li> la posizione</li><li>  genere </li><li>nameimage </li><li> remote_profile_url</li></ul> |
| Booleano *facoltativo* | moderatore | Definisce se l'utente dispone di privilegi di moderatore nella rete. |
| Booleano *facoltativo* | gravatar_disabled | Definisce se disabilitare l'utilizzo di un gravatar da parte di Livefyre in assenza di image_url. |

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
