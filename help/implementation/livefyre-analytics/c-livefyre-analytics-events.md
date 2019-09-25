---
description: nulle
seo-description: nulle
seo-title: Eventi di Livefyre Analytics
solution: Experience Manager
title: Eventi di Livefyre Analytics
uuid: 4eb5a196-ca33-40f8-a96d-ed46469223de
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Eventi di Livefyre Analytics {#livefyre-analytics-events}

## Definizione oggetto evento {#section_dh1_yhn_pdb}

Il codice seguente definisce i campi nell'oggetto evento che vengono ricevuti dal gestore di analisi su una pagina.

```
{
  evars: {
    appId : string : URN ID of the app
    appType : string : Type of the app
    contentType : string : Type of the content that this event pertains to
    contextId : string : URN ID of the contextual item that this event pertains to
    environment : string : Environment that this app is using
    networkId : string : Network that this app is using
    publishedDate : number : Epoch time when the app was published
    userLoggedIn : boolean : If a user is logged in
  },
  generator: {
    env : string: Environment that this app is using
    id : string: URN ID of the app
    name : string: Name of the app
    networkId : string: Network that this app is using
    source : string: URN of the collection
    version : string: Semver version of the app
  },
  startTime : number: Epoch time when event was created
  type : string: Event type (Table 1)
}
```

## Eventi e eVar di Livefyre Analytics {#section_u3k_tft_mcb}

I seguenti eventi Livefyre da mappare a eventi personalizzati da utilizzare nei rapporti tramite Report Suite Manager. Per ulteriori informazioni sulle suite di rapporti in Adobe Analytics, vedi [Report Suite Manager](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html). Per ulteriori informazioni sull'utilizzo degli eventi Livefyre con Report Suite Manager, consulta [](../livefyre-analytics/c-use-livefyre-with-adobe-analytics.md#section_iks_kgd_4cb).

## Eventi di Livefyre Analytics

| Evento | Descrizione |
|---|---|
| Init | Quando una pagina che include almeno un'app Livefyre viene caricata |
| Caricamento | Ogni volta che un'app veniva caricata su una pagina, a prescindere dalla visualizzazione utente |
| Visualizzazione | Quando un'app è entrata nella finestra per la prima volta. |
| Post | Ogni volta che un utente pubblica un commento o un contenuto, ad esempio: post di primo livello, risposte, recensioni, caricamenti di bacheche multimediali |
| Inserito | Quando un post ha avuto successo. |
| Twitter_Reply | Ogni volta che un utente risponde su Twitter |
| Twitter_Like | Dove è stato condiviso il contenuto: Retweet |
| Livefyre_Like | Ogni volta che la funzione "vivaio come" viene utilizzata in un'app |
| Livefyre_Contrariamente a | Ogni volta che un utente non gradisce un carattere attivo |
| ShareOnPost | Ogni volta che un utente pubblica dei contenuti e utilizza la funzione Condividi on post |
| ShareButtonClick | Ogni volta che un utente fa clic sul pulsante Condividi su un commento |
| ShareTwitter | Quando si fa clic su Condividi su Twitter |
| ShareFacebook | Quando si fa clic su Condividi su Facebook |
| ShareURL | Quando si seleziona o si copia l'area di testo Condividi su URL. |
| ExpandReplies | Quando un utente fa clic sul collegamento + o Espandi per visualizzare tutte le risposte su un post di livello principale |
| CollapseReplies | Quando un utente fa clic sul collegamento - o Comprimi per visualizzare tutte le risposte in un post di livello principale |
| FlagClick | Ogni volta che un utente apre il Modal contrassegno |
| FlagSpam | Quando un utente contrassegna il contenuto come spam |
| FlagDisagreement | Quando un utente contrassegna il contenuto come non d'accordo |
| FlagOffensive | Quando un utente contrassegna il contenuto come offensivo |
| FlagOffTopic | Quando un utente contrassegna il contenuto come argomento non noto |
| FlagCancel | Ogni volta che un utente fa clic su X o "annulla" durante l'invio di un flag |
| FollowCollection | Ogni volta che viene seguita una conversazione ("Sono interessato" alle recensioni) |
| UnfollowCollection | Quando una conversazione non viene seguita |
| RequestMore | Ogni volta che un utente carica più contenuto in un'app (deve essere anche per l'alta velocità) |
| ModalView | Ogni volta che un utente fa clic per visualizzare il contenuto in una modalità |
| TwitterRetweetClick | Dove è stato condiviso il contenuto: Retweet |
| PostButtonClick | Quando un utente fa clic sul post ("Cosa hai in mente?") button |
| Login | Ogni volta che un utente ha effettuato l’accesso |
| Logout | Ogni volta che un utente si disconnetteva |

Di seguito è riportato un elenco delle variabili di conversione (eVar) fornite da Livefyre.

## Variabili di conversione - eVar

| Evento | Descrizione |
|--- |--- |
| ID di rete | Nome/ID di rete in Livefyre |
| ID app | URL dell'app |
| ID contesto | ID contenuto in Livefyre |
| Tipo di app | Tipo di app Livefyre. Opzioni: <br><ul><li>Live Blog  </li><li> Scheda</li><li>Carosello</li><li>Chat </li><li>Commenti</li><li>Filmstrip</li><li>Mappa</li><li>Mosaico</li><li>Muro di supporto</li><li>Tendenza</li><li>Pulsante Carica</li></ul> |
| Tipo di contenuto | Instagram, Twitter, Facebook, LiveFyre, YouTube, ecc |

## More Info {#section_b3d_4yl_pdb}

Per ulteriori informazioni sugli argomenti trattati in questa pagina, vedi:

* [Report Suite](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)[ManagerDTM](https://marketing.adobe.com/resources/help/en_US/livefyre/c_filmstrip_app.html)

* [Regole](https://marketing.adobe.com/resources/help/en_US/dtm/rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)