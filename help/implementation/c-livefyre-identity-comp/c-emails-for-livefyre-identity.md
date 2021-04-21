---
title: E-mail per Livefyre Identity
description: E-mail per Livefyre Identity
exl-id: c8127eef-8fb8-4703-ba34-ef12453f1754
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 0%

---

# E-mail per Livefyre Identity{#emails-for-livefyre-identity}

Livefyre Identity invia le seguenti e-mail:

* [Ripristina e-mail password](#c_emails_for_livefyre_identity/section_nd1_whs_p1b)
* [E-mail di verifica](#c_emails_for_livefyre_identity/section_ak5_xhs_p1b)
   * [Invia verifica e-mail agli utenti](#c_emails_for_livefyre_identity/section_vyv_yhs_p1b)

* [E-mail di benvenuto](#c_emails_for_livefyre_identity/section_z2v_zhs_p1b)
   * [Invia e-mail di benvenuto agli utenti](#c_emails_for_livefyre_identity/section_kjp_c3s_p1b)

Puoi personalizzare l’aspetto di tutte le e-mail di Livefyre Identity in **[!UICONTROL Integration Settings > Email Notifications.]**

## E-mail per reimpostazione password {#section_nd1_whs_p1b}

Livefyre invia automaticamente un&#39;e-mail di reimpostazione della password quando un utente prova a reimpostare la password.

L’e-mail di reimpostazione della password si presenta così:

**Oggetto:** Ripristino della password

**Corpo:**

Ciao *&lt;username>*,

È stata inviata una richiesta di modifica della password del tuo profilo su *&lt;network name>*.

Se lo hai richiesto, fai clic sul seguente link per scegliere una nuova password: *&lt;URL per la reimpostazione della password>*.

*&lt;username>*,  *&lt;network name=&quot;&quot;>* e  *&lt;password reset=&quot;&quot; URL=&quot;&quot;>* vengono generati in modo dinamico in base al visitatore del sito e alla rete.

## E-mail di verifica {#section_ak5_xhs_p1b}

Puoi inviare un’e-mail di verifica dell’indirizzo e-mail di un utente. Per inviare e-mail di verifica, devi attivare l’opzione in **Impostazioni integrazione > Identità Livefyre**.

L’e-mail di verifica si presenta così:

**Oggetto:** Verifica delle e-mail

**Corpo:**

Ciao *&lt;username>*,

Fai clic sul seguente link (o incolla nel tuo browser) per verificare il tuo account: *&lt;URL di verifica>*.

Questo link scadrà tra 24 ore.

Grazie

Il team *&lt;nome cliente>*

*&lt;username>*,  *&lt;network name=&quot;&quot;>* e  *&lt;verification URL=&quot;&quot;>* vengono generati in modo dinamico in base al visitatore del sito e alla rete.

## Invia una verifica e-mail agli utenti {#section_vyv_yhs_p1b}

Puoi inviare un’e-mail a un utente per verificare l’indirizzo e-mail che utilizza per registrarsi a un account. Per inviare un messaggio e-mail di verifica:

1. In Studio, fai clic sull&#39;icona ingranaggio per modificare le impostazioni di rete.
1. Fai clic su **Impostazioni integrazione > Identità Livefyre.**

1. Passa a **Tipi di accesso**.
1. Fai clic su **Richiedi verifica e-mail** per inviare un messaggio e-mail agli utenti che verificano l’indirizzo e-mail che utilizzano per registrarsi a un account.
1. Passa a **E-mail di rete** per configurare il **Logo per e-mail**, l’indirizzo e-mail da utilizzare come indirizzo e-mail (**E-mail da**) e il nome visualizzato da utilizzare per l’indirizzo e-mail del mittente (**Nome visualizzato e-mail**).

## E-mail di benvenuto {#section_z2v_zhs_p1b}

Puoi inviare un messaggio e-mail di benvenuto agli utenti. Per inviare e-mail di benvenuto, devi attivare l’opzione in **Impostazioni integrazione** > **Identità Livefyre**.

L’e-mail di benvenuto si presenta così:

**Oggetto:** Benvenuto in  *&lt;customer name=&quot;&quot;>*

**Corpo:**

Ciao *&lt;username>*,

È stato creato un account su *&lt;nome cliente>*.

Questo account è stato creato su *&lt;URL di riferimento>* dall&#39;indirizzo IP *&lt;Indirizzo IP>*.

Se lo hai fatto, puoi tranquillamente ignorare questa e-mail.

In caso contrario, contatta `support@livefyre.com`

Grazie

Il team *&quot;customer name&quot;*

*&quot;Nome utente&quot;, &quot;nome cliente&quot;, &quot;URL di riferimento&quot;* e &quot;Indirizzo IP&quot; vengono generati in modo dinamico in base al visitatore del sito e alla rete.

## Invia un messaggio e-mail di benvenuto a un utente {#section_kjp_c3s_p1b}

Puoi inviare un messaggio e-mail di benvenuto a un utente dopo che si è registrato per un account. Se imposti un messaggio e-mail di verifica, Studio invia questo messaggio e-mail dopo l’invio di un messaggio e-mail di verifica. Per inviare un messaggio e-mail di benvenuto:

1. In Studio, fai clic sull&#39;icona ingranaggio per modificare le impostazioni di rete.
1. Clic **[!UICONTROL Integration Settings > Livefyre Identity]**

1. Passa a **[!UICONTROL Email Settings]**.

1. Fai clic su **[!UICONTROL Send Welcome Emails To New Users]** per abilitare l’invio di e-mail.
1. Passa a **[!UICONTROL Network Email]** per configurare il *Logo per E-mail*, l’indirizzo e-mail da utilizzare come indirizzo da (**E-mail da**) e il nome visualizzato da utilizzare per l’indirizzo e-mail da (**Nome visualizzato e-mail**).
