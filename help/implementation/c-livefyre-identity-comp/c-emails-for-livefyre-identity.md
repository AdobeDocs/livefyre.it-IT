---
description: nulle
seo-description: nulle
seo-title: E-mail per identità Livefyre
solution: Experience Manager
title: E-mail per identità Livefyre
uuid: 4e807803-687e-4df0-94d1-b18a48d024e8
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---


# E-mail per Livefyre Identity{#emails-for-livefyre-identity}

Livefyre Identity invia i seguenti messaggi e-mail:

* [E-mail di ripristino password](#c_emails_for_livefyre_identity/section_nd1_whs_p1b)
* [E-mail di verifica](#c_emails_for_livefyre_identity/section_ak5_xhs_p1b)
   * [Invia verifica e-mail per gli utenti](#c_emails_for_livefyre_identity/section_vyv_yhs_p1b)

* [E-mail di benvenuto](#c_emails_for_livefyre_identity/section_z2v_zhs_p1b)
   * [Invia e-mail di benvenuto agli utenti](#c_emails_for_livefyre_identity/section_kjp_c3s_p1b)

Potete personalizzare l&#39;aspetto di tutte le e-mail di identità Livefyre in **[!UICONTROL Integration Settings > Email Notifications.]**

## E-mail reimpostazione password {#section_nd1_whs_p1b}

Livefyre invia automaticamente un messaggio e-mail di reimpostazione della password quando un utente tenta di reimpostare la password.

Il messaggio e-mail di reimpostazione della password è simile al seguente:

**Oggetto:** Reimposta password

**Corpo:**

Hey lì *&lt;nomeutente>*,

È stata richiesta la modifica della password del profilo su *&lt;nome rete>*.

Se lo avete richiesto, fate clic sul seguente collegamento per scegliere una nuova password: *&lt;URL reimpostazione password>*.

*&lt;username>*,  *&lt;network name=&quot;&quot;>* e  *&lt;password reset=&quot;&quot; URL=&quot;&quot;>* vengono generati in modo dinamico in base al visitatore del sito e alla rete.

## E-mail di verifica {#section_ak5_xhs_p1b}

Potete inviare un messaggio e-mail di verifica dell’indirizzo e-mail di un utente. Per inviare e-mail di verifica, è necessario attivare l&#39;opzione in **Impostazioni integrazione > Identità Livefyre**.

Il messaggio e-mail di verifica è simile al seguente:

**Oggetto:Verifica** E-Mail

**Corpo:**

Ciao *&lt;nome utente>*,

Fate clic sul seguente collegamento (o incollate nel browser) per verificare il vostro account: *&lt;URL verifica>*.

Questo collegamento scade tra 24 ore.

Grazie

Il team *&lt;nome cliente>*

*&lt;username>*,  *&lt;network name=&quot;&quot;>* e  *&lt;verification URL=&quot;&quot;>* vengono generati in modo dinamico in base al visitatore del sito e alla rete.

## Invia una verifica e-mail agli utenti {#section_vyv_yhs_p1b}

Potete inviare un messaggio e-mail a un utente per verificare l’indirizzo e-mail usato per registrarsi a un account. Per inviare un messaggio e-mail di verifica:

1. In Studio, fare clic sull&#39;icona ingranaggio per modificare le impostazioni di rete.
1. Fare clic su **Impostazioni integrazione > Identità Livefyre.**

1. Passare a **Tipi di login**.
1. Fate clic su **Richiedi verifica e-mail** per inviare un messaggio e-mail agli utenti che verifica l&#39;indirizzo e-mail utilizzato per registrarsi a un account.
1. Andate a **Network Email** per configurare il **Logo per Email**, l&#39;indirizzo e-mail da utilizzare come indirizzo da (**Email From**) e il nome visualizzato per l&#39;indirizzo e-mail del mittente (**Email Display Name**).

## E-mail di benvenuto {#section_z2v_zhs_p1b}

Potete inviare un messaggio e-mail di benvenuto agli utenti. Per inviare e-mail di benvenuto, è necessario attivare l&#39;opzione in **Impostazioni integrazione** > **Identità Livefyre**.

Il messaggio e-mail di benvenuto è simile al seguente:

**Oggetto:** Benvenuti a  *&lt;customer name=&quot;&quot;>*

**Corpo:**

Ciao *&lt;nome utente>*,

È stato creato un account su *&lt;nome cliente>*.

Questo account è stato creato su *&lt;URL referral>* dall&#39;indirizzo IP *&lt;Indirizzo IP>*.

Se hai fatto questo, puoi tranquillamente ignorare questa email.

In caso contrario, contattare `support@livefyre.com`

Grazie

Il team *&quot;customer name&quot;*

*&quot;Nome utente&quot;, &quot;nome cliente&quot;, &quot;URL di riferimento&quot;* e &quot;Indirizzo IP&quot; vengono generati dinamicamente in base al visitatore del sito e alla rete.

## Invia un messaggio e-mail di benvenuto a un utente {#section_kjp_c3s_p1b}

Potete inviare un messaggio e-mail di benvenuto a un utente dopo che questi si è registrato per un account. Studio invia questo messaggio e-mail dopo l&#39;invio di un messaggio e-mail di verifica, se avete impostato un messaggio e-mail di verifica. Per inviare un messaggio e-mail di benvenuto:

1. In Studio, fare clic sull&#39;icona ingranaggio per modificare le impostazioni di rete.
1. Clic **[!UICONTROL Integration Settings > Livefyre Identity]**

1. Passare a **[!UICONTROL Email Settings]**.

1. Fate clic su **[!UICONTROL Send Welcome Emails To New Users]** per abilitare l&#39;invio di e-mail.
1. Andate a **[!UICONTROL Network Email]** per configurare il *Logo per E-mail*, l&#39;indirizzo e-mail da utilizzare come indirizzo da (**E-mail da**) e il nome visualizzato per l&#39;indirizzo e-mail del mittente (**Nome visualizzato e-mail**).
