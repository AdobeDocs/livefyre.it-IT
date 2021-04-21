---
description: Il conteggio dei listener è un contatore che tiene traccia del numero di visitatori del sito per un'app su una pagina e visualizza questo numero.
title: Conteggio listener
exl-id: a07e83c2-7465-42ec-9d24-821aac5ab74b
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 0%

---

# Conteggio listener{#listener-count}

Il conteggio dei listener è un contatore che tiene traccia del numero di visitatori del sito per un&#39;app su una pagina e visualizza questo numero.

Conteggio listener è il numero di visitatori del sito che hanno un browser aperto alla pagina in cui viene creata un&#39;istanza di un&#39;app. Questo consente di sapere quanti visitatori del sito si trovano sulla pagina in un dato momento, in modo da poterli tracciare mentre guardano lo streaming o il contenuto live in tempo reale.

Il conteggio dei listener di Livefyre funziona così:

1. Il sito contenente la tua app esegue il ping di un server Livefyre ogni 60 secondi.
1. Il server Livefyre risponde al numero di visitatori del sito sulla pagina che visualizza l’app (definito come il numero di visitatori del sito con un browser aperto a tale pagina).
1. Il numero di visitatori del sito sulla pagina con l’app viene visualizzato sull’app.

App che utilizzano questa funzione:

* [Chat](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Commenti](/help/using/c-about-apps/c-comments/c-comments.md)
* [Recensioni](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)

## Avatar del listener {#section_wcn_kxp_vz}

Il conteggio degli ascoltatori visualizza un massimo di 10 avatar e visualizza gli avatar solo per le persone che hanno fatto clic su **[!UICONTROL Follow]** per la conversazione.

>[!NOTE]
>
>A causa di vincoli di spazio, l’interfaccia mobile visualizza solo il numero di ascoltatori e una piccola icona &quot;persone&quot;.

Il conteggio dei listener Livefyre mostra il numero di persone attive sulla pagina in un dato momento, più il numero di persone che seguono la conversazione. Se un utente è sulla pagina e segue la conversazione, non verrà conteggiato due volte. Ad esempio, se un utente si trova su una pagina e fa clic su **[!UICONTROL Follow]**, il conteggio dei listener non aumenterà; se l&#39;utente fa clic su **[!UICONTROL Unfollow]**, il conteggio non diminuirà.

App che utilizzano questa funzione:

* [Chat](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Commenti](/help/using/c-about-apps/c-comments/c-comments.md)
* [Recensioni](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Memorizza 2](../c-about-apps/c-storify2/c-storify2.md#c_storify2)
