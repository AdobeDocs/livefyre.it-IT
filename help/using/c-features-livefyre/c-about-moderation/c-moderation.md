---
description: Livefyre Spam e Abuse Filtering Engine (SAFE), un processo in background
  che analizza tutto il contenuto in arrivo ed è abilitato per tutti i clienti Livefyre.
seo-description: Livefyre Spam e Abuse Filtering Engine (SAFE), un processo in background
  che analizza tutto il contenuto in arrivo ed è abilitato per tutti i clienti Livefyre.
seo-title: Regole SAFE
title: Regole SAFE
uuid: 2 f 91 d 0 d 4-dffe -4651-88 af -79 bbb 96 c 1 b 5 c
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Regole SAFE{#safe-rules}

Livefyre Spam e Abuse Filtering Engine (SAFE), un processo in background che analizza tutto il contenuto in arrivo ed è abilitato per tutti i clienti Livefyre.



SAFE usa regole di pattern e modelli statistici per rilevare post di spam, abusi, blasfemie e in massa (ripetitive). Di tanto in tanto gli potrete fare riferimento in altri prodotti Livefyre, in particolare gli strumenti di moderazione dei contenuti e modq.

>[!NOTE]
>
>SAFE è solo in inglese, fatta eccezione per la classificazione di mailing list. Se necessitate di supporto per altre lingue, contattate il vostro responsabile commerciale strategico.

## Componenti Studio con SAFE {#section_k34_4tx_vy}

I flag applicati da SAFE possono essere utilizzati con i seguenti componenti Studio:

* Regole

   Puoi definire regole SAFE per segnalare automaticamente i contenuti e definire il modo **[!UICONTROL Network Settings]**in cui il contenuto contrassegnato deve essere gestito.

   Ad esempio, un sito potrebbe impostare una tolleranza molto bassa per Profanity e definire regole SAFE che impostano tutti i contenuti contrassegnati come Profane come bozò d. Altri siti possono definire regole che impostano il contenuto Profane affinché venga premoderato prima di entrare nel flusso.

* Modq

   Puoi moderare i contenuti segnalati dalle regole SAFE e altre regole di premoderazione (ad esempio, SPAM, blasfemia ecc.), in modq.

* Contenuto dell'app nella libreria

   Il contenuto contrassegnato da SAFE è elencato nel contenuto app della **[!UICONTROL Library]** scheda. Potete filtrare il contenuto per flag per moderare il contenuto.

## Opzioni filtro sicuro {#section_pg5_ttx_vy}

SAFE applica i seguenti flag al contenuto filtrato e può essere utilizzato per creare regole e moderare contenuto da Livefyre Studio.

* **[!UICONTROL Profanity List]**: Contenuto profano, come definito da un elenco di parole chiave inglese, in base all'uso comune.

   Il filtro Profanity cerca la lingua profana in base a un elenco di parole testate. Se rilevato, il contenuto è segnalato Profano.

   >[!NOTE]
   >
   >Livefyre fornisce anche un secondo filtro Elenco profetico, che potete personalizzare a livello di sito e di rete. Le regole create con l'Elenco profanity hanno la precedenza sulle regole automatizzate derivate dal filtro SAFE Profanity. Per ulteriori informazioni, consulta la sezione Elenco profetico nella documentazione Impostazioni.

* **[!UICONTROL Mild Profanity]**: Parole e frasi generalmente non accettabili nelle conversazioni educative, ma in genere sono accettabili nelle conversazioni occasionali. In genere, le parole e le frasi sono consentite in rete di rete.
* **[!UICONTROL Strong Profanity]**: Un linguaggio molto forte, ad esempio esplicazioni e frasi non consentite in rete di rete e utilizzati con cautela nei filmati con valutazione R e nelle trasmissioni TV via cavo. In genere queste parole non vengono utilizzate in conversazione cordiale o informale e sono pronunciate in una conversazione imitabile, con l'intento di danneggiare il listener.
* **[!UICONTROL SPAM]**: Contenuto non richiesto, generalmente contenuto commerciale. Utilizza un modello statistico che si basa su diverse funzioni (inclusi contenuti e URL dei commenti) per contrassegnare una parte del contenuto come SPAM. È possibile regolare le soglie di spam per personalizzare le percentuali di tag SPAM per la rete o il sito, tramite richiesta.
* **[!UICONTROL Mild Insult]**: Contenuto inoffensivo, come definito da un elenco di parole chiave e pattern di frase.
* **[!UICONTROL Strong Insult]**: Contenuto inoffensivo, come definito da un elenco di parole chiave e pattern di frase.
* **[!UICONTROL Hate Speech]**: Un abuso basato su etnia o religione, in particolare se l'appartenenza ai gruppi di destinazione è in minoranza o protetta.
* **[!UICONTROL ALL CAPS]**: Testo visualizzato in tutte le lettere maiuscole (leggi come yelling).
* **[!UICONTROL Mild Threat]**: Una minaccia o un insulto che in genere include un'abilità leggera indirizzata a un'altra persona. This option flags possible threats more often, but also has a higher false-positive rate than **[!UICONTROL Strong Threat]**.

* **[!UICONTROL Strong Threat]**: Una grave minaccia o un insulto che cita danni ricorrenti a una o più persone, spesso con forte ostilità. This option flags possible threats less often, but also has a lower false-positive rate than **[!UICONTROL Mild Threat]**.

* **[!UICONTROL Probable Nudity]**: Un'immagine che potrebbe presentare delle nuvole. This option flags nudity less often, but also has a lower false-positive rate than **[!UICONTROL Possible Nudity]**.

* **[!UICONTROL Possible Nudity]**: Un'immagine che potrebbe presentare delle nuvole. This option flags nudity more often, but also has a higher false-positive rate than **[!UICONTROL Probable Nudity]**.

* **[!UICONTROL PII]** (Informazioni personali): Informazioni che possono identificare l'utente. Questo può includere indirizzo e-mail, indirizzo fisico, numero di previdenza sociale (per clienti US), numero di carta di credito, password o qualcosa che può essere utilizzato nelle frodi o per ottenere l'identità di qualcun utente.
* **[!UICONTROL Livefyre Recommends Trash]**. Impostate l'azione eseguita dal sistema quando la raccomandazione di moderazione automatica identifica il contenuto per il rifiuto. ![](assets/mod_reco1.png)

   >[!NOTE]
   >
   >Per attivare Recommendations Recommendations, contattate il vostro tecnico di supporto Adobe Livefyre.

## Gestione contenuto non rilevata da SAFE {#section_pjy_5tx_vy}

Esistono diversi mezzi disponibili per gestire efficacemente i contenuti non rilevati da questo filtro. Le opzioni riportate di seguito sono elencate nell'ordine di processo consigliato.

1. Come moderatore, rimuovete il contenuto dallo streaming.
1. Create una Regola di segnalazione che indichi se un pezzo di contenuto è contrassegnato come Spam o Offensivo da cinque utenti, impostandolo su Bozo.
1. Proibite l'utente che pubblica contenuto non desiderato, in modo che tutto il suo contenuto passerà direttamente allo stato Bozo.
1. Aggiungi parole specifiche da filtrare sempre nel tuo elenco.

>[!NOTE]
>
>Se un moderatore posiziona il contenuto che viene rilevato dal filtro Spam, viene comunque segnalato come Spam, ma viene approvato automaticamente e non sarà impostato su Bozo.

Se notate tendenze o pattern di contenuto non rilevati da SAFE, inviate i vostri CSMS con gli ID commento e il testo.



App che utilizzano questa funzione:

* [Carosello](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Commenti](/help/using/c-about-apps/c-comments/c-comments.md)
* [Scheda Funzioni](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Mappa](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Media Wall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaic](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Recensioni](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Pulsante Carica](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

