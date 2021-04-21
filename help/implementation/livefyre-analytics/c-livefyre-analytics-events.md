---
title: Eventi di Livefyre Analytics
description: Eventi di Livefyre Analytics
exl-id: ec32414c-0580-44dc-ae5b-6df0b42c0ec3
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 2%

---

# Eventi di Livefyre Analytics

## Definizione dell&#39;oggetto evento {#section_dh1_yhn_pdb}

Il codice seguente definisce i campi nell&#39;oggetto evento che vengono ricevuti dal gestore di analisi su una pagina.

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

## Eventi ed eVar di Livefyre Analytics {#section_u3k_tft_mcb}

I seguenti eventi Livefyre da mappare a eventi personalizzati da utilizzare nei rapporti tramite Report Suite Manager. Per ulteriori informazioni sulle suite di rapporti in Adobe Analytics, consulta [Report Suite Manager](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html). Per ulteriori informazioni su come utilizzare gli eventi Livefyre con Report Suite Manager, consulta [](../livefyre-analytics/c-use-livefyre-with-adobe-analytics.md#section_iks_kgd_4cb).

## Eventi di Livefyre Analytics

| Evento | Descrizione |
|---|---|
| Init | Quando viene caricata una pagina che include almeno un’app Livefyre |
| Load | Ogni volta che un&#39;app è stata caricata su una pagina, indipendentemente dalla visualizzazione utente |
| Visualizzazione | Quando un&#39;app è entrata per la prima volta nel riquadro di visualizzazione. |
| Post | Ogni volta che un utente pubblica un commento o un contenuto, ad esempio: post di primo livello, risposte, recensioni, caricamenti di media wall |
| Pubblicato | Quando un post ha avuto successo. |
| Twitter_Reply | Ogni volta che un utente risponde su Twitter |
| Twitter_Like | Dove è stato condiviso il contenuto in: Retweet |
| Livefyre_Like | Ogni volta che la funzione &quot;livefyre like&quot; viene utilizzata in un’app |
| A differenza di Livefyre | Ogni volta che a un utente non piace un livefyre come |
| ShareOnPost | Ogni volta che un utente pubblica un contenuto e utilizza la funzione di condivisione on post |
| ShareButtonClick | Ogni volta che un utente fa clic sul pulsante di condivisione su un commento |
| ShareTwitter | Quando si fa clic su Condividi su Twitter |
| ShareFacebook | Quando si fa clic su Condividi su Facebook |
| ShareURL | Quando l’opzione Condividi su area di testo URL è selezionata/copiata. |
| Espandi risposte | Quando un utente fa clic sul collegamento + o Espandi per visualizzare tutte le risposte in un post di livello principale |
| ComprimiRisposte | Quando un utente fa clic sul collegamento - o Comprimi per visualizzare tutte le risposte in un post di primo livello |
| FlagClick | Ogni volta che un utente apre il modale contrassegno |
| FlagSpam | Quando un utente contrassegna il contenuto come spam |
| FlagNonConcordo | Quando un utente contrassegna i contenuti come non concordi |
| FlagOffensive | Quando un utente contrassegna i contenuti come offensivi |
| FlagOffTopic | Quando un utente contrassegna il contenuto come argomento esterno |
| FlagCancel | Ogni volta che un utente fa clic su X o &quot;annulla&quot; quando invia un flag |
| FollowCollection | Ogni volta che viene seguita una conversazione (&quot;Sono interessato&quot; alle Recensioni) |
| UnfollowCollection | Quando una conversazione non viene seguita |
| RequestMore | Ogni volta che un utente carica più contenuto in un&#39;app (deve essere anche ad alta velocità) |
| Visualizzazione modale | Ogni volta che un utente fa clic per visualizzare il contenuto in un modale |
| TwitterRetweetClick | Dove è stato condiviso il contenuto in: Retweet |
| PostButtonClick | Quando un utente clicca sul post (&quot;Cosa hai in mente?&quot;) pulsante |
| Login | Ogni volta che un utente ha effettuato l&#39;accesso |
| Logout | Ogni volta che un utente si disconnette |

Di seguito è riportato un elenco di variabili di conversione (eVar) fornite da Livefyre.

## Variabili di conversione - eVar

| Evento | Descrizione |
|--- |--- |
| ID di rete | ID/nome di rete in Livefyre |
| ID app | URN dell’app |
| ID contesto | ID contenuto in Livefyre |
| Tipo di app | Tipo di app Livefyre. Opzioni: <br><ul><li>Blog dal vivo  </li><li> Scheda tecnica</li><li>Carosello</li><li>Chat </li><li>Commenti</li><li>Filmstrip</li><li>Mappa</li><li>Mosaico</li><li>Parete multimediale</li><li>Tendenza</li><li>Pulsante Carica</li></ul> |
| Tipo di contenuto | Instagram, Twitter, Facebook, LiveFyre, YouTube, ecc. |

## Ulteriori informazioni {#section_b3d_4yl_pdb}

Per ulteriori informazioni sugli argomenti trattati in questa pagina, vedi:

* [Report Suite ](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html)[ManagerDTM](https://docs.adobe.com/content/help/en/livefyre/using/apps/filmstrip/c-filmstrip-app.html)

* [Regole](https://docs.adobe.com/content/help/en/dtm/using/resources/rules/create-rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)
