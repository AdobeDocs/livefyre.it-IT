---
description: Il conteggio dei listener è un contatore che tiene traccia del numero di visitatori del sito per un'app su una pagina e visualizza questo numero.
seo-description: Il conteggio dei listener è un contatore che tiene traccia del numero di visitatori del sito per un'app su una pagina e visualizza questo numero.
seo-title: Conteggio listener
solution: Experience Manager
title: Conteggio listener
uuid: fdd 7 cfe 4-ae 69-4 d 31-baa 2-8978368 fc 3 e 8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Conteggio listener{#listener-count}

Il conteggio dei listener è un contatore che tiene traccia del numero di visitatori del sito per un&#39;app su una pagina e visualizza questo numero.

Numero listener è il numero di visitatori del sito che hanno un browser aperto alla pagina su cui viene creata un&#39;istanza di un&#39;app. Questo consente di sapere quanti visitatori del sito si trovano sulla pagina in un determinato momento, in modo da poterli tenere traccia durante lo streaming o il contenuto live in tempo reale.

Il conteggio dei listener di Livefyre funziona come segue:

1. Il sito contenente l&#39;app invia un ping a Livefyre Server ogni 60 secondi.
1. Il server Livefyre risponde al numero di visitatori del sito nella pagina che visualizza l&#39;app (definito come numero di visitatori del sito con un browser aperto a quella pagina).
1. Il numero di visitatori del sito nella pagina con l&#39;app viene visualizzato nell&#39;app.

App che utilizzano questa funzione:

* [Chat](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Commenti](/help/using/c-about-apps/c-comments/c-comments.md)
* [Recensioni](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)

## Avatar listener {#section_wcn_kxp_vz}

Il conteggio dei listener visualizza un massimo di 10 avatar e visualizza avatar solo per coloro che hanno fatto clic **[!UICONTROL Follow]** per la conversazione.

>[!NOTE]
>
>A causa di vincoli di spazio, l&#39;interfaccia mobile visualizza solo il numero di listener e un&#39;icona di tipo «persone».

Livefyre Listener Count visualizza il numero di persone attive sulla pagina in un determinato momento, oltre al numero di persone che seguono la conversazione. Se qualcuno si trova sulla pagina e dopo la conversazione, tale utente non sarà conteggiato due volte. Ad esempio, se un utente si trova su una pagina e su un clic **[!UICONTROL Follow]**, il conteggio dei listener non aumenterà; se l&#39;utente fa clic **[!UICONTROL Unfollow]** su di esso, il conteggio non diminuisce.

App che utilizzano questa funzione:

* [Chat](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Commenti](/help/using/c-about-apps/c-comments/c-comments.md)
* [Recensioni](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Storify 2](../c-about-apps/c-storify2/c-storify2.md#c_storify2)

