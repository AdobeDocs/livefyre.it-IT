---
description: Il motore di filtraggio degli abusi e dello spam Livefyre (SAFE) è un processo in background che analizza tutti i contenuti in arrivo ed è abilitato per tutti i clienti Livefyre.
title: Regole di sicurezza
exl-id: 13cd8df0-c4b7-436e-ba07-64ec67321d6b
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 0%

---

# Regole SAFE{#safe-rules}

Il motore di filtraggio degli abusi e dello spam Livefyre (SAFE) è un processo in background che analizza tutti i contenuti in arrivo ed è abilitato per tutti i clienti Livefyre.



SAFE utilizza regole di pattern e modelli statistici per rilevare spam, abusi, profanità e post in massa (ripetitivi). Lo vedrai di volta in volta referenziato in altri prodotti Livefyre, in particolare gli strumenti di moderazione del contenuto e ModQ.

>[!NOTE]
>
>SAFE è disponibile solo in inglese, ad eccezione della classificazione di spedizione in serie. Se hai bisogno di supporto per altre lingue, contatta il tuo Strategic Account Manager.

## Componenti da studio che utilizzano SAFE {#section_k34_4tx_vy}

I flag applicati da SAFE possono essere utilizzati con i seguenti componenti Studio:

* Regole

   Puoi definire regole SAFE per contrassegnare automaticamente il contenuto e definire come deve essere gestito il contenuto contrassegnato in **[!UICONTROL Network Settings]**.

   Ad esempio, un sito può impostare una tolleranza molto bassa per Profanity e definire regole SAFE che impostano tutti i contenuti contrassegnati come Profane per essere Bozo’d. Altri siti possono definire regole che impostano il contenuto Profano come pre-moderato prima di entrare nel flusso.

* ModQ

   Nel ModQ è possibile moderare il contenuto contrassegnato da regole SAFE e da altre regole di moderazione (ad esempio, SPAM, profanity, ecc.).

* Contenuto dell’app nella libreria

   Il contenuto contrassegnato da SAFE è elencato nella scheda Contenuto app della scheda **[!UICONTROL Library]** . Puoi filtrare il contenuto in base ai flag per moderare il contenuto.

## Opzioni filtro SAFE {#section_pg5_ttx_vy}

SAFE applica i seguenti flag al contenuto filtrato e può essere utilizzato per creare regole e moderare contenuto da Livefyre Studio.

* **[!UICONTROL Profanity List]**: Contenuto redditizio, come definito da un elenco di parole chiave inglesi, basato sull’uso comune.

   Il filtro Profanity cerca una lingua profana, basata su un elenco di parole testate. Se rilevato, il contenuto viene contrassegnato come Profano.

   >[!NOTE]
   >
   >Livefyre fornisce anche un secondo filtro Elenco profitti, personalizzabile a livello di Sito e Rete. Le regole create con l&#39;Elenco profitti avranno la precedenza sulle regole automatizzate derivanti dal filtro Profanity SAFE. Per ulteriori informazioni, consulta la sezione Elenco profitti nella documentazione Impostazioni .

* **[!UICONTROL Mild Profanity]**: Parole e frasi generalmente non accettabili nelle conversazioni educate, ma sono solitamente accettabili nelle conversazioni casuali. Generalmente queste parole e frasi sono consentite dalla televisione in rete.
* **[!UICONTROL Strong Profanity]**: Linguaggio molto forte, come esploratori e frasi non consentite sulla televisione di rete e usate con moderazione nei film classificati R e nei programmi televisivi via cavo maturi. Generalmente queste parole non sono usate in conversazioni educate o casuali e sono dette in una conversazione scortese con l&#39;intento di danneggiare l&#39;ascoltatore.
* **[!UICONTROL SPAM]**: Contenuto non sollecitato, solitamente commerciale. Utilizza un modello statistico che si basa su una varietà di funzioni (tra cui contenuto di commenti e URL) per contrassegnare un contenuto come SPAM. È possibile regolare le soglie dello spam per personalizzare le percentuali di assegnazione tag SPAM per la rete o il sito, su richiesta.
* **[!UICONTROL Mild Insult]**: Contenuto isolante, come definito da un elenco di parole chiave e pattern di frasi.
* **[!UICONTROL Strong Insult]**: Contenuto isolante, come definito da un elenco di parole chiave e pattern di frasi.
* **[!UICONTROL Hate Speech]**: Un insulto basato sull&#39;etnia o la religione, specialmente quando l&#39;affiliazione al gruppo bersaglio è in minoranza o protetta.
* **[!UICONTROL ALL CAPS]**: Testo presentato in lettere maiuscole (letto come urlo).
* **[!UICONTROL Mild Threat]**: Una minaccia o un insulto che di solito include qualche tipo di blanda blanda blanda contro un&#39;altra persona. Questa opzione contrassegna le possibili minacce più spesso, ma ha anche un tasso di falso positivo più elevato di **[!UICONTROL Strong Threat]**.

* **[!UICONTROL Strong Threat]**: Una minaccia grave o un insulto che menzioni danni corporei actionable a una o più persone, spesso con una forte profanità. Questa opzione contrassegna le possibili minacce meno spesso, ma ha anche un tasso di falso positivo inferiore a **[!UICONTROL Mild Threat]**.

* **[!UICONTROL Probable Nudity]**: Un&#39;immagine che potrebbe avere sfumature. Questa opzione contrassegna il carattere meno spesso, ma ha anche un tasso di falso positivo inferiore a **[!UICONTROL Possible Nudity]**.

* **[!UICONTROL Possible Nudity]**: Un&#39;immagine che potrebbe avere sfumature. Questa opzione contrassegna il nudità più spesso, ma ha anche un tasso di falso positivo più alto di **[!UICONTROL Probable Nudity]**.

* **[!UICONTROL PII]** (Informazioni Personalmente Identificabili): Informazioni che possono identificare l’utente. Ciò può includere un indirizzo e-mail, un indirizzo fisico, un numero di previdenza sociale (per i clienti statunitensi), un numero di carta di credito, una password o qualsiasi cosa che può essere utilizzata per frode o per ottenere l’identità di qualcuno.
* **[!UICONTROL Livefyre Recommends Trash]**. Imposta l&#39;azione eseguita dal sistema quando la raccomandazione di moderazione automatizzata identifica il contenuto per il rifiuto.  ![](assets/mod_reco1.png)

   >[!NOTE]
   >
   >Per attivare Moderation Recommendations, contatta il tuo Adobe Livefyre support professional.

## Gestione del contenuto non rilevato da SAFE {#section_pjy_5tx_vy}

Sono disponibili diversi strumenti per gestire efficacemente i contenuti non acquisiti da questo filtro. Le opzioni seguenti sono elencate nell&#39;ordine di elaborazione consigliato.

1. In qualità di moderatore, rimuovi il contenuto dal flusso.
1. Crea una regola di flag che indica se un contenuto è contrassegnato come spam o offensivo da cinque utenti, impostalo su Bozo.
1. Divieti l&#39;utente che pubblica contenuti indesiderati, in modo che tutti i loro contenuti vadano direttamente nello stato Bozo.
1. Aggiungi parole specifiche che devono sempre essere filtrate nell&#39;elenco delle profanità.

>[!NOTE]
>
>Se un moderatore pubblica un contenuto catturato dal nostro Filtro Spam, viene comunque contrassegnato come Spam, ma viene approvato automaticamente e non verrà impostato su Bozo.

Se noti tendenze o pattern di contenuti non rilevati da SAFE, invia un’e-mail ai CSM con gli ID commento e il testo.



App che utilizzano questa funzione:

* [Carosello](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Commenti](/help/using/c-about-apps/c-comments/c-comments.md)
* [Scheda tecnica](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Mappa](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Parete multimediale](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaico](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Recensioni](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Note](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Memorizza 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Pulsante Carica](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)
