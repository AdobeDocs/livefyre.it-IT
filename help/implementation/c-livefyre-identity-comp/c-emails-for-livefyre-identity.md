---
description: nulle
seo-description: nulle
seo-title: E-mail per identità Livefyre
solution: Experience Manager
title: E-mail per identità Livefyre
uuid: 4e807803-687e-4df0-94d1-b18a48d024e8
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# E-mail per identità Livefyre{#emails-for-livefyre-identity}

Livefyre Identity invia i seguenti messaggi e-mail:

* [E-mail ripristino password](#c_emails_for_livefyre_identity/section_nd1_whs_p1b)
* [E-mail di verifica](#c_emails_for_livefyre_identity/section_ak5_xhs_p1b)
   * [Invia verifica e-mail per utenti](#c_emails_for_livefyre_identity/section_vyv_yhs_p1b)

* [E-mail di benvenuto](#c_emails_for_livefyre_identity/section_z2v_zhs_p1b)
   * [Invia e-mail di benvenuto agli utenti](#c_emails_for_livefyre_identity/section_kjp_c3s_p1b)

Potete personalizzare l'aspetto di tutte le e-mail di identità Livefyre in **[!UICONTROL Integration Settings > Email Notifications.]**

## E-mail ripristino password {#section_nd1_whs_p1b}

Livefyre invia automaticamente un messaggio e-mail di reimpostazione della password quando un utente tenta di reimpostare la password.

Il messaggio e-mail di reimpostazione della password è simile al seguente:

**** Oggetto: Ripristina password

**Corpo:**

Ehi *&lt;username&gt;*,

È stata richiesta la modifica della password del tuo profilo su *&lt;nome rete&gt;*.

Se lo avete richiesto, fate clic sul seguente collegamento per scegliere una nuova password: *&lt;URL reimpostazione password&gt;*.

*&lt;Nome utente&gt;*, *&lt;nome rete&gt;* e *&lt;URL reimpostazione password&gt;* vengono generati dinamicamente in base al visitatore del sito e alla rete.

## E-mail di verifica {#section_ak5_xhs_p1b}

Potete inviare un messaggio e-mail di verifica dell’indirizzo e-mail di un utente. Per inviare e-mail di verifica, è necessario attivare l'opzione in Impostazioni **integrazione &gt; Identità** Livefyre.

Il messaggio e-mail di verifica è simile al seguente:

**** Oggetto: Verifica e-mail

**Corpo:**

Ciao *&lt;nome utente&gt;*,

Fate clic sul seguente collegamento (o incollate nel browser) per verificare il vostro account: *&lt;URL verifica&gt;*.

Questo collegamento scade tra 24 ore.

Grazie

Il team *&lt;nome cliente&gt;*

*&lt;Nome utente&gt;*, *&lt;nome rete&gt;* e *&lt;URL verifica&gt;* vengono generati dinamicamente in base al visitatore del sito e alla rete.

## Invia una verifica tramite e-mail agli utenti {#section_vyv_yhs_p1b}

Potete inviare un messaggio e-mail a un utente per verificare l’indirizzo e-mail usato per registrarsi a un account. Per inviare un messaggio e-mail di verifica:

1. In Studio, fare clic sull'icona ingranaggio per modificare le impostazioni di rete.
1. Fate clic su Impostazioni **integrazione &gt; Identità Livefyre.**

1. Passa a Tipi **di** accesso.
1. Fate clic su **Richiedi verifica** e-mail per inviare un messaggio e-mail agli utenti che verificano l’indirizzo e-mail utilizzato per registrarsi a un account.
1. Passate a E-mail **di** rete per configurare il **Logo per E-mail**, l'indirizzo e-mail da utilizzare come indirizzo da (**E-mail da**) e il nome visualizzato da utilizzare per l'indirizzo e-mail da utilizzare (Nome **visualizzato** e-mail).

## E-mail di benvenuto {#section_z2v_zhs_p1b}

Potete inviare un messaggio e-mail di benvenuto agli utenti. Per inviare e-mail di benvenuto, dovete attivare l'opzione in Impostazioni **** integrazione &gt; Identità **** Livefyre.

Il messaggio e-mail di benvenuto è simile al seguente:

**** Oggetto: Benvenuti in *&lt;nome cliente&gt;*

**Corpo:**

Ciao *&lt;nome utente&gt;*,

È stato creato un account su *&lt;nome cliente&gt;*.

Questo account è stato creato su *&lt;URL di riferimento&gt;* dall'indirizzo IP *&lt;Indirizzo IP&gt;*.

Se hai fatto questo, puoi tranquillamente ignorare questa email.

In caso contrario, contattate `support@livefyre.com`

Grazie

Il team *"customer name"*

*"Nome utente", "nome cliente",* "URL di riferimento" e "Indirizzo IP" vengono generati dinamicamente in base al visitatore del sito e alla rete.

## Invio di un messaggio e-mail di benvenuto a un utente {#section_kjp_c3s_p1b}

Potete inviare un messaggio e-mail di benvenuto a un utente dopo che questi si è registrato per un account. Studio invia questo messaggio e-mail dopo l'invio di un messaggio e-mail di verifica, se avete impostato un messaggio e-mail di verifica. Per inviare un messaggio e-mail di benvenuto:

1. In Studio, fare clic sull'icona ingranaggio per modificare le impostazioni di rete.
1. Fai clic su **[!UICONTROL Integration Settings > Livefyre Identity]**

1. Passa a **[!UICONTROL Email Settings]**.

1. Fate clic **[!UICONTROL Send Welcome Emails To New Users]** per abilitare l'invio di e-mail.
1. Andate **[!UICONTROL Network Email]** a configurare il *Logo per l’e-mail*, l’indirizzo e-mail da usare come indirizzo da (**E-mail da**) e il nome visualizzato da utilizzare per l’indirizzo e-mail del mittente (Nome **visualizzato e-** mail).
