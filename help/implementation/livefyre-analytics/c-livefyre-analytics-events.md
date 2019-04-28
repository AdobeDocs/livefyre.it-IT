---
description: nulle
seo-description: nulle
seo-title: Eventi di Livefyre Analytics
solution: Experience Manager
title: Eventi di Livefyre Analytics
uuid: 4 eb 5 a 196-ca 33-40 f 8-a 96 d-ed 46469223 de
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Eventi di Livefyre Analytics {#livefyre-analytics-events}

## Definizione oggetto evento {#section_dh1_yhn_pdb}

Il codice seguente definisce i campi nell&#39;oggetto evento ricevuto dal gestore di analisi su una pagina.

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

## Eventi e evar di Livefyre Analytics {#section_u3k_tft_mcb}

I seguenti eventi Livefyre per mappare gli eventi personalizzati da utilizzare nei rapporti tramite la suite di rapporti. Per ulteriori informazioni sulle suite di rapporti in Adobe Analytics, consulta [Report Suite Manager](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)(Gestione suite di rapporti). Per ulteriori informazioni sull&#39;utilizzo di eventi Livefyre con Report Suite Manager, vedi [](../livefyre-analytics/c-use-livefyre-with-adobe-analytics.md#section_iks_kgd_4cb).

## Eventi di Livefyre Analytics

| Evento | Descrizione |
|---|---|
| Init | Quando viene caricata una pagina contenente almeno un&#39;app Livefyre |
| Carica | Ogni volta che un&#39;app è stata caricata su una pagina, indipendentemente dalla vista dell&#39;utente |
| Visualizza | Quando un&#39;app è entrato per la prima volta. |
| Post | Ogni volta che un utente inserisce un commento o un contenuto, ad esempio: post di livello principale, risposte, recensioni, caricamento di Wall Wall |
| Pubblicato | Quando un post è stato successionato. |
| Twitter_ Reply | Ogni volta che un utente ha risposto su Twitter |
| Twitter_ Like | Dove è stato condiviso il contenuto: Retweet |
| Livefyre_ Like | Ogni volta che la funzione livefyre like viene utilizzata in un&#39;app |
| Livefyre_ Unlike | Ogni volta che un utente ama un livefyre come |
| Shareonpost | Ogni volta che un utente pubblica contenuto e utilizza la condivisione su funzione post |
| Sharebuttonclick | Ogni volta che un utente fa clic sul pulsante Condividi su un commento |
| Sharetwitter | Quando si fa clic su Condividi su Twitter |
| Sharefacebook | Quando si fa clic su Condividi su Facebook |
| Shareurl | Quando l&#39;area di testo Condividi su URL è selezionata o copiata. |
| Expandreplies | Quando un utente fa clic sul collegamento + o Espandi per visualizzare tutte le risposte su un post di livello principale |
| Collapsereplies | Quando un utente fa clic sul collegamento - o Comprimi per visualizzare tutte le risposte su un post di livello principale |
| Flagclick | Ogni volta che un utente apre il flag Modale |
| Flagspam | Quando un utente contrassegna il contenuto come spam |
| Flagd | Quando un utente contrassegna il contenuto come non d&#39;accordo |
| Flagoffensive | Quando un utente contrassegna il contenuto come offensivo |
| Flagofftopic | Quando un utente attiva il contenuto come argomento off |
| Flagcancel | Ogni volta che un utente fa clic su X o su «annulla» durante l&#39;invio di un flag |
| Followcollection | Ogni volta che viene seguita una conversazione (&quot;Sono interessato&quot; in Recensioni) |
| Unfollowcollection | Quando una conversazione non è seguita |
| Requestmore | Ogni volta che un utente carica più contenuto in un&#39;app (richiede anche la massima velocità) |
| Modalview | Ogni volta che un utente fa clic per visualizzare il contenuto in una modale |
| Twitterretweetclick | Dove è stato condiviso il contenuto: Retweet |
| Postbuttonclick | Quando un utente fa clic sul post («Whats on your mind? &quot;) button |
| Login | Ogni volta che un utente accede |
| Disconnessione | Ogni volta che un utente si disconnette |

Di seguito è riportato un elenco delle variabili di conversione (evars) fornite da Livefyre.

## Variabili di conversione - evar

| Evento | Descrizione |
|--- |--- |
| ID rete | ID/nome di rete in Livefyre |
| ID app | L&#39;URN dell&#39;app |
| ID contesto | ID contenuto in Livefyre |
| Tipo app | Livefyre App Type. Opzioni: <br><ul><li>Blog live  </li><li> Scheda Funzioni</li><li>Carosello</li><li>Chat </li><li>Commenti</li><li>Filmstrip</li><li>Mappa</li><li>Mosaic</li><li>Media Wall</li><li>Tendenza</li><li>Pulsante Carica</li></ul> |
| Tipo di contenuto | Instagram, Twitter, Facebook, livefyre, YouTube, ecc. |

## Ulteriori informazioni {#section_b3d_4yl_pdb}

Per ulteriori informazioni sugli argomenti trattati in questa pagina, consulta:

* [Report Suite managerdtm](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)[](https://marketing.adobe.com/resources/help/en_US/livefyre/c_filmstrip_app.html)

* [Regole](https://marketing.adobe.com/resources/help/en_US/dtm/rules.html)
* [Livefyre. js](/help/implementation/c-livefyre.js.md)