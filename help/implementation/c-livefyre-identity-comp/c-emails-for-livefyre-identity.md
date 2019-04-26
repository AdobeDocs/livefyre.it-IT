---
description: nulle
seo-description: nulle
seo-title: E-mail per identità Livefyre
solution: Experience Manager
title: E-mail per identità Livefyre
uuid: 4 e 807803-687 e -4 df 0-94 d 1-b 18 a 48 d 024 e 8
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# E-mail per identità Livefyre{#emails-for-livefyre-identity}

Livefyre Identity invia le seguenti e-mail:

* [Reimposta password e-mail](#c_emails_for_livefyre_identity/section_nd1_whs_p1b)
* [E-mail di verifica](#c_emails_for_livefyre_identity/section_ak5_xhs_p1b)
   * [Invia verifica e-mail per utenti](#c_emails_for_livefyre_identity/section_vyv_yhs_p1b)

* [E-mail di benvenuto](#c_emails_for_livefyre_identity/section_z2v_zhs_p1b)
   * [Invia messaggio di benvenuto agli utenti](#c_emails_for_livefyre_identity/section_kjp_c3s_p1b)

Puoi personalizzare l'aspetto di tutte le e-mail di identità Livefyre in **[!UICONTROL Integration Settings > Email Notifications.]**

## Reimposta password e-mail {#section_nd1_whs_p1b}

Livefyre invia automaticamente un messaggio e-mail di reimpostazione password quando un utente tenta di reimpostare la password.

L'e-mail di ripristino della password si presenta così:

**Oggetto:** Reimposta password

**Corpo:**

Hey there *< username >*,

Si è verificata una richiesta di modifica della password del profilo su *< nome rete >*.

Se avete richiesto questa opzione, fate clic sul collegamento seguente per scegliere una nuova password: *< URL reimpostazione password >*.

*< Nome utente >*, *< nome rete >*e *< URL ripristino password >* vengono generati dinamicamente in base al visitatore del sito e alla rete.

## E-mail di verifica {#section_ak5_xhs_p1b}

Potete inviare un'e-mail di verifica dell'indirizzo e-mail di un utente. Per inviare le e-mail di verifica, è necessario attivare l'opzione in **Impostazioni integrazione > Identità Livefyre**.

L'e-mail di verifica si presenta così:

**Oggetto:** Verifica e-mail

**Corpo:**

Hello *< username >*,

Per verificare l'account, fate clic sul collegamento seguente (o incollate nel browser): *< URL di verifica >*.

Questo collegamento scade dopo 24 ore.

Ringraziamenti,

Il *< nome cliente >* Gruppo

*< Nome utente >*, *< nome rete >*e *< URL di verifica >* vengono generati dinamicamente in base al visitatore del sito e alla rete.

## Invia una verifica e-mail agli utenti {#section_vyv_yhs_p1b}

Potete inviare un messaggio e-mail a un utente per verificare l'indirizzo e-mail che usano per registrarsi a un account. Per inviare un messaggio e-mail di verifica:

1. In Studio, fate clic sull'icona a forma di ingranaggio per modificare le impostazioni di rete.
1. Fate clic **su Impostazioni integrazione > Identità Livefyre.**

1. Passa a Tipi **di accesso**.
1. Fate clic su **Richiedi verifica e-mail** per inviare un messaggio e-mail agli utenti che verificano l'indirizzo e-mail che utilizzano per registrarsi per un account.
1. Passate a **E-mail di rete** per configurare **il logo per e-mail**, l'indirizzo e-mail da utilizzare come indirizzo da (**e-mail da)**e il nome visualizzato da utilizzare per l'indirizzo e-mail (**nome visualizzato e-mail**).

## E-mail di benvenuto {#section_z2v_zhs_p1b}

Potete inviare un messaggio e-mail di benvenuto agli utenti. Per inviare e-mail di benvenuto, è necessario attivare l'opzione in **Impostazioni integrazione** > **Identità Livefyre**.

L'e-mail di benvenuto si presenta così:

**Oggetto:** Benvenuto in *< nome cliente >*

**Corpo:**

Hello *< username >*,

Un account è stato creato su *< nome cliente >*.

Questo account è stato creato su *< URL di riferimento >* dall'indirizzo IP *< Indirizzo IP >*.

In tal caso, puoi ignorare il messaggio e-mail in modo sicuro.

Se non lo avete fatto, contattate `support@livefyre.com`

Thank

The *"customer name"* Team

*«Nome utente», «Nome cliente», «URL di riferimento»* e «Indirizzo IP» vengono generati dinamicamente in base al visitatore del sito e alla rete.

## Inviare un messaggio e-mail di benvenuto a un utente {#section_kjp_c3s_p1b}

Potete inviare un messaggio e-mail di benvenuto a un utente dopo che questi sono registrati per un account. Studio invia questo messaggio e-mail dopo che è stato inviato un messaggio e-mail di verifica, se si è impostato un messaggio e-mail di verifica. Per inviare un messaggio e-mail di benvenuto:

1. In Studio, fate clic sull'icona a forma di ingranaggio per modificare le impostazioni di rete.
1. Clic **[!UICONTROL Integration Settings > Livefyre Identity]**

1. **[!UICONTROL Email Settings]**Passa a.

1. Fate clic per **[!UICONTROL Send Welcome Emails To New Users]** abilitare l'invio delle e-mail.
1. Individuate il **[!UICONTROL Network Email]***logo per e-mail*, l'indirizzo e-mail da utilizzare come indirizzo (**e-mail da)**e il nome visualizzato da utilizzare per l'indirizzo e-mail (**nome visualizzato e-mail**).
