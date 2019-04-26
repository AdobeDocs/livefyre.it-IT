---
description: Create la risposta Ping for Pull per trasmettere le informazioni utente
  aggiornate a Livefyre.
seo-description: Create la risposta Ping for Pull per trasmettere le informazioni
  utente aggiornate a Livefyre.
seo-title: Creare la risposta di ping per la risposta
solution: Experience Manager
title: Creare la risposta di ping per la risposta
uuid: f 90871 d 5-601 f -40 dc-b 3 d 2-ab 78635 e 4 a 88
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Creare la risposta di ping per la risposta{#build-the-ping-for-pull-response}

Create la risposta Ping for Pull per trasmettere le informazioni utente aggiornate a Livefyre.

| Tipo | Proprietà | Descrizione |
|--- |--- |--- |
| Stringa *richiesta* | id | L'ID utente dell'utente nel sistema di profilo. Questo deve essere univoco per tutti gli utenti della rete e non deve mai cambiare. |
| Stringa *richiesta* | display_ name | Nome visualizzato dell'utente. Verrà eseguito il rendering con il contenuto Livefyre pubblicato dall'utente. |
| Oggetto *facoltativo, ma consigliato* | name | Stringhe per definire i nomi formattati, first, middle e last dell'utente. |
| Stringa *opzionale, ma consigliato* | email | Indirizzo e-mail dell'utente. Utilizzato per inviare notifiche e-mail. |
| Stringa *opzionale, ma consigliato* | image_ url | URL a un avatar da visualizzare per l'utente. Livefyre ridimensiona le immagini caricate a 100 × 100, 75 × 75 o 50 × 50 pixel, a seconda delle necessità. Per risultati ottimali, gli utenti devono caricare un'immagine quadrata, a 100 × 100 pixel. Per verificare che l'immagine avatar venga aggiornata in Livefyre, modificate l'immagine_ url per ogni aggiornamento dell'immagine, quindi Ping for Pull rileva che l'immagine è stata modificata. Ad esempio, associare una marca temporale al nome del file o incrementare l'immagine. Nota: Tutti gli URL devono essere completi e accessibili. |
| Stringa *opzionale, ma consigliato* | profile_ url | URL della pagina del profilo dell'utente sul sito. |
| Stringa *opzionale, ma consigliato* | settings_ url | URL a una pagina in cui gli utenti possono configurare le impostazioni del profilo dell'utente per il sito. |
| Array *facoltativo, ma consigliato* | tag | Utilizzato per assegnare utenti a gruppi di utenti. I tag possono includere caratteri alfanumerici 1-63 e caratteri di sottolineatura. |
| Booleano *opzionale, ma consigliato* | auto autofollow_ conversations | Definisce se un utente desidera seguire automaticamente una raccolta dopo averlo inviato. Quando si segue una raccolta, gli utenti ricevono le notifiche e-mail quando altri utenti partecipano. Può essere true o false. Impostazione predefinita: true. |
| Oggetto *facoltativo, ma consigliato* | email_ notifications | Definisce la frequenza delle notifiche e-mail disponibili di Livefyre. Potete impostare diverse frequenze per ogni tipo di notifica. Per impostazione predefinita, non viene inviata alcuna notifica. <br><ul><li> immediatamente le notifiche vengono pubblicate immediatamente dopo l'evento elencato. </li><li>spesso si verificano notifiche in batch. </li><li> non invierà mai le notifiche e-mail per l'attività. </li><li>*commenti*: Definisce quando le notifiche vengono inviate quando altri utenti pubblicano contenuto nelle raccolte che questo utente segue. </li><li>*risposte*: Definisce quando le notifiche vengono inviate quando un altro utente risponde al contenuto dell'utente.</li><li>*mi*piace: Definisce quando le notifiche vengono inviate quando un altro utente ama il contenuto dell'utente.</li><li>*moderator_ comments*: Definisce quando le notifiche vengono inviate ai moderatori quando gli utenti pubblicano contenuto in qualsiasi raccolta della rete.</li><li>*moderator_ flags*: Definisce quando le notifiche vengono inviate ai moderatori quando altri utenti effettuano il flag del contenuto in qualsiasi raccolta della rete.</li></ul> |
| Stringa *opzionale* | location | Una posizione inviata dall'utente. |
| Stringa *opzionale* | biografia | Una autobiografia inviata dall'utente. |
| Array *facoltativo* | siti Web | Un array di siti inviati dall'utente. Max = 2. |
| Oggetto *facoltativo* | display_ rules | Definisce quali proprietà del profilo sono visibili pubblicamente ad altri utenti. Ogni parametro disponibile richiede il valore booleano true o false. Parametri disponibili: <br><ul><li>biografia </li><li> location</li><li>  genere </li><li>nameimage </li><li> remote_ profile_ url</li></ul> |
| *Booleano opzionale* | moderatore | Definisce se l'utente dispone dei privilegi di moderatore in rete. |
| *Booleano opzionale* | lapatar_ disabled | Definisce se disabilitare l'uso di Livefyre di un semitatar se non viene fornito alcun URL image_ url. |

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
