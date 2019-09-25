---
description: Il motore di filtraggio degli spam e degli abusi di Livefyre (SAFE) è un processo in background che analizza tutti i contenuti in arrivo ed è abilitato per tutti i clienti Livefyre.
seo-description: Il motore di filtraggio degli spam e degli abusi di Livefyre (SAFE) è un processo in background che analizza tutti i contenuti in arrivo ed è abilitato per tutti i clienti Livefyre.
seo-title: Regole di sicurezza
title: Regole di sicurezza
uuid: 2f91d0d4-dffe-4651-88af-79bbb96c1b5c
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Regole di sicurezza{#safe-rules}

Il motore di filtraggio degli spam e degli abusi di Livefyre (SAFE) è un processo in background che analizza tutti i contenuti in arrivo ed è abilitato per tutti i clienti Livefyre.



SAFE utilizza le regole dei pattern e i modelli statistici per rilevare spam, abusi, profanità e post in massa (ripetitivi). Di tanto in tanto verrà fatto riferimento ad altri prodotti Livefyre, in particolare agli strumenti di moderazione dei contenuti e a ModQ.

>[!NOTE]
>
>SAFE è solo inglese, tranne che per la classificazione di spedizione in massa. Se hai bisogno di supporto per altre lingue, contatta il tuo Strategic Account Manager.

## Componenti da studio mediante SAFE {#section_k34_4tx_vy}

I flag applicati da SAFE possono essere utilizzati con i seguenti componenti Studio:

* Regole

   Potete definire regole SAFE per contrassegnare automaticamente il contenuto e definire in che modo il contenuto contrassegnato deve essere gestito nel **[!UICONTROL Network Settings]**.

   Ad esempio, un sito può impostare una tolleranza molto bassa per Profanity e definire regole SICURE che impostano tutti i contenuti contrassegnati come Profane da Bozo’d. Altri siti possono definire regole che impostano il contenuto Profano in modo da essere pre-moderato prima di entrare nel flusso.

* ModQ

   Nel ModQ potete moderare il contenuto contrassegnato dalle regole SAFE e da altre regole di moderazione (ad esempio, SPAM, profanity, ecc.).

* Contenuto app nella libreria

   Il contenuto contrassegnato da SAFE è elencato in Contenuto app nella **[!UICONTROL Library]** scheda. Potete filtrare il contenuto in base ai flag per moderare il contenuto.

## Opzioni filtro SAFE {#section_pg5_ttx_vy}

SAFE applica i seguenti flag ai contenuti filtrati e può essere utilizzato per creare regole e contenuti moderati da Livefyre Studio.

* **[!UICONTROL Profanity List]**: Contenuto utile, come definito da un elenco di parole chiave inglesi, in base all'uso comune.

   Il filtro Profanity cerca una lingua profana, in base a un elenco di parole testato. Se rilevato, il contenuto viene contrassegnato come Profano.

   >[!NOTE]
   >
   >Livefyre fornisce anche un secondo filtro Elenco profitti, personalizzabile a livello di sito e di rete. Le regole create con l'Elenco profitti avranno la precedenza sulle regole automatizzate derivanti dal filtro Profanità SAFE. Per ulteriori informazioni, consulta la sezione Elenco profitti nella documentazione Settings.

* **[!UICONTROL Mild Profanity]**: Parole e frasi generalmente non accettabili nelle conversazioni educate, ma solitamente sono accettabili nelle conversazioni casuali. In genere, queste parole e frasi sono consentite dalla televisione in rete.
* **[!UICONTROL Strong Profanity]**: Un linguaggio molto forte, come gli esploratori e le frasi non sono consentiti sulla televisione di rete e utilizzati con attenzione nei film R e nei programmi TV via cavo maturi. Generalmente queste parole non sono usate in conversazioni educate o casuali e sono dette in una conversazione maleducata con l'intento di danneggiare l'ascoltatore.
* **[!UICONTROL SPAM]**: Contenuto non sollecitato, solitamente commerciale. Utilizza un modello statistico che si basa su una varietà di funzioni (inclusi contenuti di commenti e URL) per contrassegnare un contenuto come SPAM. Potete regolare le soglie di spam per personalizzare le percentuali di tag SPAM per la rete o il sito, su richiesta.
* **[!UICONTROL Mild Insult]**: Insulto del contenuto, come definito da un elenco di parole chiave e pattern di frasi.
* **[!UICONTROL Strong Insult]**: Insulto del contenuto, come definito da un elenco di parole chiave e pattern di frasi.
* **[!UICONTROL Hate Speech]**: Un insulto basato sull'etnia o la religione, specialmente quando l'affiliazione al gruppo bersaglio è in minoranza o protetta.
* **[!UICONTROL ALL CAPS]**: Testo presentato in lettere maiuscole (letto come urlo).
* **[!UICONTROL Mild Threat]**: Una minaccia o un insulto che di solito include una specie di blanda blanda blanda contro un'altra persona. Questa opzione contrassegna le possibili minacce più spesso, ma ha anche un tasso di falsi positivi più alto rispetto a **[!UICONTROL Strong Threat]**.

* **[!UICONTROL Strong Threat]**: Una grave minaccia o un insulto che cita il danno corporeo fruibile a una o più persone, spesso con una forte profanità. Questa opzione contrassegna le possibili minacce meno spesso, ma ha anche un tasso di falsi positivi inferiore rispetto a **[!UICONTROL Mild Threat]**.

* **[!UICONTROL Probable Nudity]**: Un'immagine che potrebbe presentare delle sfumature. Questa opzione contrassegna il carattere meno spesso, ma ha anche un tasso di falsi positivi inferiore a **[!UICONTROL Possible Nudity]**.

* **[!UICONTROL Possible Nudity]**: Un'immagine che potrebbe presentare delle sfumature. Questa opzione contrassegna più spesso il carattere "nudo", ma ha anche un tasso di falsi positivi più elevato rispetto a **[!UICONTROL Probable Nudity]**.

* **[!UICONTROL PII]** (Informazioni Personalmente Identificabili): Informazioni che possono identificare l’utente. Questo può includere un indirizzo e-mail, un indirizzo fisico, un numero di previdenza sociale (per i clienti statunitensi), un numero di carta di credito, una password o qualsiasi cosa che possa essere utilizzata per frode o per ottenere l'identità di un altro utente.
* **[!UICONTROL Livefyre Recommends Trash]**. Impostate l'azione eseguita dal sistema quando la raccomandazione di moderazione automatizzata identifica il contenuto per il rifiuto.  ![](assets/mod_reco1.png)

   >[!NOTE]
   >
   >Per attivare Recommendations per moderazione, contattate il vostro tecnico del supporto Adobe Livefyre.

## Gestione del contenuto non rilevato da SAFE {#section_pjy_5tx_vy}

Sono disponibili diversi strumenti per gestire efficacemente il contenuto non catturato da questo filtro. Le opzioni seguenti sono elencate nell'ordine di elaborazione consigliato.

1. Come moderatore, rimuovete il contenuto dal flusso.
1. Create una regola di contrassegno che indichi se un contenuto è contrassegnato come Spam o Offensive da cinque utenti, impostatelo su Bozo.
1. Divieto per l'utente che pubblica contenuti indesiderati, in modo che tutti i contenuti vadano direttamente nello stato Bozo.
1. Aggiungi parole specifiche che devono sempre essere filtrate nell'elenco delle profanità.

>[!NOTE]
>
>Se un moderatore pubblica dei contenuti catturati dal nostro Filtro Spam, viene comunque contrassegnato come Spam, ma viene automaticamente Approvato e non verrà impostato su Bozo.

Se notate tendenze o pattern di contenuto non rilevati da SAFE, inviate un’e-mail ai CSM con gli ID commento e il testo.



App che utilizzano questa funzione:

* [Carosello](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Commenti](/help/using/c-about-apps/c-comments/c-comments.md)
* [Scheda](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Mappa](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Muro di supporto](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaico](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Recensioni](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Pulsante Carica](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

