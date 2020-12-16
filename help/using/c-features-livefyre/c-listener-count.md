---
description: Il conteggio listener è un contatore che tiene traccia del numero di visitatori del sito per un'app su una pagina e visualizza questo numero.
seo-description: Il conteggio listener è un contatore che tiene traccia del numero di visitatori del sito per un'app su una pagina e visualizza questo numero.
seo-title: Numero listener
solution: Experience Manager
title: Numero listener
uuid: fdd7cfe4-ae69-4d31-baa2-8978368fc3e8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---


# Conteggio listener{#listener-count}

Il conteggio listener è un contatore che tiene traccia del numero di visitatori del sito per un&#39;app su una pagina e visualizza questo numero.

Conteggio listener è il numero di visitatori del sito che dispongono di un browser aperto sulla pagina in cui viene creata un&#39;istanza dell&#39;app. Questo consente di sapere quanti visitatori del sito si trovano sulla pagina in un dato momento, in modo da poterli tracciare mentre guardano lo streaming o il contenuto live in tempo reale.

Il numero di Listener di Livefyre funziona così:

1. Il sito contenente l’app esegue il ping di un server Livefyre ogni 60 secondi.
1. Il server Livefyre risponde con il numero di visitatori del sito sulla pagina che visualizza l&#39;App (definito come il numero di visitatori del sito con un browser aperto alla pagina).
1. Il numero di visitatori del sito sulla pagina con l&#39;app viene visualizzato nell&#39;app.

App che utilizzano questa funzione:

* [Chat](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Commenti](/help/using/c-about-apps/c-comments/c-comments.md)
* [Recensioni](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)

## Avatar del listener {#section_wcn_kxp_vz}

Il numero di listener visualizza un massimo di 10 avatar e visualizza gli avatar solo per le persone che hanno fatto clic su **[!UICONTROL Follow]** per la conversazione.

>[!NOTE]
>
>A causa di vincoli di spazio, l&#39;interfaccia mobile visualizza solo il numero di listener e una piccola icona &quot;persone&quot;.

Il conteggio listener Livefyre visualizza il numero di persone attive sulla pagina in un dato momento, più il numero di persone che seguono la conversazione. Se un utente è sulla pagina e segue la conversazione, non verrà conteggiato due volte. Ad esempio, se un utente si trova su una pagina e fa clic su **[!UICONTROL Follow]**, il numero di listener non aumenta; se l&#39;utente fa clic su **[!UICONTROL Unfollow]**, il conteggio non diminuirà.

App che utilizzano questa funzione:

* [Chat](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Commenti](/help/using/c-about-apps/c-comments/c-comments.md)
* [Recensioni](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Storify 2](../c-about-apps/c-storify2/c-storify2.md#c_storify2)

