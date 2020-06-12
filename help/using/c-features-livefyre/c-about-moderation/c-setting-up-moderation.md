---
description: Utilizzate la scheda Moderazione per impostare le regole di moderazione per il contenuto in entrata, inclusi gli elenchi di profanità, le regole di flag e gli indirizzi IP vietati.
seo-description: Utilizzate la scheda Moderazione per impostare le regole di moderazione per il contenuto in entrata, inclusi gli elenchi di profanità, le regole di flag e gli indirizzi IP vietati.
seo-title: Impostazione della moderazione
solution: Experience Manager
title: Impostazione della moderazione
uuid: 0ec53fdb-08c2-4058-88cb-2f6f4b56a95b
translation-type: tm+mt
source-git-commit: 52f59cd15f315aa93be198f6eb586f008c18a384
workflow-type: tm+mt
source-wordcount: '1299'
ht-degree: 0%

---


# Impostazione della moderazione{#setting-up-moderation}

Utilizzate la scheda Moderazione per impostare le regole di moderazione per il contenuto in entrata, inclusi gli elenchi di profanità, le regole di flag e gli indirizzi IP vietati.

## Come funziona la moderazione {#section_kyf_gvc_t1b}

Potete moderare i contenuti nei seguenti modi:

* Consente di premoderare automaticamente il contenuto per filtrare i contenuti indesiderati in base alle regole configurate prima della pubblicazione.
* Eliminate o approvate manualmente il contenuto contrassegnato con la premoderazione automatica utilizzando ModQ o Contenuto app nella libreria.
* Identificate i visitatori del sito che pubblicano ripetutamente contenuti offensivi per impedire loro di pubblicare contenuti, vietando specifici utenti Livefyre, utenti social o indirizzi IP.
* Identificare le persone e i contenuti che possono sempre essere visualizzati consentendo l&#39;inserimento nell&#39;elenco degli utenti o disattivando i filtri per flussi, siti o reti specifici.

Potete eseguire automaticamente la premoderazione dei contenuti nei seguenti modi:

* Impostare regole per contrassegnare automaticamente determinati tipi di contenuto:

   * Imposta regole di flag per il contenuto contrassegnato dal flag dei visitatori del sito tramite **[!UICONTROL Settings > Moderation > Rules]**
   * Configurare le regole SAFE utilizzando **[!UICONTROL Settings > Moderation > Rules]**
   * Divieto di utilizzo di utenti Twitter specifici **[!UICONTROL Settings > Streams]**
   * Divieto di indirizzi IP tramite **[!UICONTROL Settings > Bans]**
   * Divieto di regione IP per codice paese per richiesta. I contenuti vietati saranno contrassegnati come SPAM.

* Crea un elenco di parole che consideri blanità nell&#39;Elenco profitti **[!UICONTROL Settings > Moderation > Rules]** per la tua rete o il tuo sito.
* Consentire agli utenti dell&#39;elenco (consentire sempre la visualizzazione del contenuto di questi utenti) di utilizzare o disattivare i filtri per flussi, siti o reti specifici.

Dopo aver impostato gli elenchi di profanità, i filtri SAFE e le regole, potete scegliere se eseguire la premoderazione del contenuto e applicare i filtri SAFE nei flussi. Per ulteriori informazioni, vedere Opzioni regola [flusso per tutte le regole](/help/using/c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)di flusso.

Livefyre contrassegna il contenuto come **[!UICONTROL Approved]**, **[!UICONTROL Pending]**, **[!UICONTROL Junk]** ecc. a seconda di quale origine del contenuto, dove verrà pubblicato e quali regole avete impostato nel sistema. Nella tabella seguente sono descritte dettagliatamente le azioni eseguite da Livefyre, a seconda di questi fattori.

## Come funziona la moderazione

| Il Contenuto Viene Da: | Invio Di Contenuto A: | Stato approvazione |
|--- |--- |--- |
| Libreria | App | Contenuto approvato |
| Ricerca social | App | Contenuto approvato |
| Regola flusso | App | Il contenuto è contrassegnato come Junk dal filtro SAFE? <br><ul><li>No - Flusso di lavoro di moderazione da flusso a app</li><li>Sì - Contenuto con traccia</li></ul> |
| Libreria | Cartella | Nessun stato (nella cartella, non pubblicato, non eliminato) |
| Ricerca social | Cartella | Nessun stato (nella cartella, non pubblicato, non eliminato) |
| Regola flusso | Cartella | Il contenuto è contrassegnato come Junk dal filtro SAFE? <br><ul><li>No - Nessuno stato (nella cartella, non pubblicato, non cancellato)</li><li>Sì - Contenuto con traccia</li></ul> |
| Post app | App | Il contenuto è contrassegnato come Junk dal filtro SAFE? <br><ul><li>No - Flusso di lavoro di moderazione post-app</li><li>Sì - Contenuto con traccia</li></ul> |

## Flusso di lavoro di moderazione da flusso a app {#section_z5z_w4d_t1b}

![](assets/stream_to_app_workflow.png)

Prima che il contenuto di un flusso venga pubblicato su un’app, Livefyre esegue i seguenti controlli per determinare le operazioni da eseguire con il contenuto:

1. Se SAFE contrassegna il contenuto come spazzatura o rilascio, Livefyre trascina il contenuto.
1. Se SAFE non contrassegna il contenuto come spazzatura, Livefyre verifica se la moderazione è attivata.
1. Se la moderazione è attivata, Livefyre contrassegna il contenuto come in sospeso.
1. Se configurate le regole ModQ, Livefyre invia il contenuto a ModQ.
1. Se la moderazione non è attivata, Livefyre verifica se SAFE ha contrassegnato il contenuto.
1. Se SAFE ha segnalato il contenuto, Livefyre approva il contenuto e lo pubblica nell&#39;app.
1. Se SAFE contrassegna il contenuto e non avete impostato regole SAFE, Livefyre approva il contenuto e lo pubblica nell&#39;app.
1. Se SAFE contrassegna il contenuto e imposti regole SICUREZZA, Livefyre verifica se avete impostato regole SICURE per il Flusso.
1. Se configurate le regole SAFE per il flusso, Livefyre approva il contenuto e lo pubblica nell&#39;app. Se non avete impostato regole SAFE per il flusso, Livefyre utilizza le regole SAFE di moderazione per determinare come gestire il contenuto (invio a ModQ, cestino, ecc.).

## Flusso di lavoro di moderazione post-app {#section_fwn_w4d_t1b}

![](assets/post_to_app_workflow.png)

Prima che il contenuto di un post dell&#39;app venga pubblicato su un&#39;app, Livefyre esegue i seguenti controlli per determinare le operazioni da eseguire con il contenuto:

1. Se il filtro SAFE contrassegna il contenuto come rilascio, Livefyre rilascia il contenuto.
1. Se SAFE non contrassegna il contenuto come rilascio, Livefyre verifica se la moderazione è attivata. Se la moderazione è attivata, Livefyre contrassegna il contenuto come in sospeso. Se configurate le regole ModQ, Livefyre invia il contenuto a ModQ come in sospeso. In caso contrario, il contenuto rimane in sospeso in Contenuto app nella libreria.
1. Se la moderazione non è attivata, Livefyre verifica se SAFE ha contrassegnato il contenuto. In caso contrario, Livefyre approva il contenuto e lo pubblica nell&#39;app.
1. Se SAFE contrassegna il contenuto e imposti regole SAFE, Livefyre utilizza la regola SAFE per determinare come gestire il contenuto (invio a ModQ, cestino, ecc.). Se SAFE contrassegna il contenuto e non avete impostato regole SAFE, Livefyre approva il contenuto e lo pubblica nell&#39;app.

## Filtri di massa {#section_lyk_ktx_vy}

Il filtro di massa cerca contenuti ripetitivi pubblicati su tutte le reti Livefyre entro un breve intervallo di tempo. Se rilevato, il contenuto viene contrassegnato come Bulk e quindi eliminato per impostazione predefinita. Anche se il contenuto in massa può essere generato dall’utente (ad esempio, &quot;Touchdown!&quot;) pubblicato ripetutamente in una chat durante una partita di calcio popolare), la maggior parte ha origine con campagne di spam. Questo filtro è indipendente dalla lingua e funziona con qualsiasi lingua. Per personalizzare il filtro di massa, è necessario contattare il supporto Livefyre.

## Regole {#section_gqz_ksk_f1b}

Utilizzate la sezione Regole per creare regole di pre-moderazione, basate su flag SICURI e applicati dall&#39;utente. Questo pannello offre due tipi di regole:

* **[!UICONTROL Flag Rules:]** specificate un’azione da eseguire su un commento contrassegnato dagli utenti un numero definito di volte.
* **[!UICONTROL SAFE Rules:]**combinare i flag SAFE con le azioni da eseguire sul contenuto contrassegnato.

Per creare regole di contrassegno, selezionate il flag (Offensivo, Disattivato, Non d’accordo o Spam), immettete il numero di volte in cui deve essere applicato a un contenuto e selezionate l’azione da intraprendere. È possibile impostare una regola di contrassegno per ciascuna opzione di flag (Offensivo, Disattivato, Non d&#39;accordo o Spam).

Puoi creare regole a livello di rete, sito e flusso. Le regole a livello di sito ereditano le regole di rete, a meno che le regole del sito non vengano configurate in modo diverso. Le regole di flusso ereditano le regole del sito a meno che non le configuriate in modo diverso.

Azioni disponibili:

* **[!UICONTROL Trash it:]**invia il commento contrassegnato al cestino.
* **[!UICONTROL Bozo it:]** nasconde il commento contrassegnato da tutti gli utenti, ad eccezione del relativo autore, a cui resta visibile.
* **[!UICONTROL Pending:]** imposta il contenuto come in sospeso. Se si imposta Premoderazione su Attivato in **[!UICONTROL Settings > ModQ]**, il valore sarà in ModQ. In caso contrario si troverà solo in Contenuto app.

>[!NOTE]
>
>Livefyre consiglia di creare delle regole per i commenti Bozo contrassegnati come Spam o Offensive da cinque utenti.

## Raccomandazioni per moderazione {#section_ec3_vr3_2cb}

Potete utilizzare le raccomandazioni di moderazione per determinare in che modo moderare il contenuto pubblicato dai visitatori del sito nelle app Livefyre. L&#39;indicatore di raccomandazione moderazione consiglia di specificare quando è probabile che una parte del contenuto venga eliminata, in base alle azioni precedentemente eseguite su contenuti simili. Per utilizzare le raccomandazioni di moderazione:

1. Attivate la funzionalità Moderation Recommendations (Raccomandazioni per moderazione) contattando il vostro tecnico del supporto Adobe Livefyre.
1. Configurate le raccomandazioni di moderazione in Impostazioni di rete.

   Configurate le raccomandazioni di moderazione utilizzando l&#39; **[!UICONTROL Livefyre Recommends Trash]** impostazione in **[!UICONTROL Network Settings]**.

   ![](assets/image_mod_reco_trash.png)

1. Configurate una regola SAFE per indicare a Livefyre cosa fare con il contenuto che la raccomandazione di moderazione identifica come contenuto che verrà probabilmente ignorato. Per ulteriori informazioni su come impostare una regola SAFE per l&#39; **[!UICONTROL Livefyre Recommends Trash]** opzione, vedere [Moderazione](/help/using/c-features-livefyre/c-about-moderation/c-moderation.md#c_moderation).

   ![](assets/modreco4.png)

1. Utilizzate **[!UICONTROL Moderation Recommendation Indicator]** in ModQ o in Contenuto app per filtrare il contenuto che la raccomandazione di moderazione identifica come probabile che venga cancellato.

   In ModQ, l’indicatore si presenta così:  ![](assets/mod_reco1.png)

   Per ulteriori informazioni su come utilizzare le raccomandazioni per moderare il contenuto in ModQ, consultate [ModQ](/help/using/c-features-livefyre/c-about-moderation/c-modq.md#c_modq).

   Nel contenuto dell&#39;app, le raccomandazioni di moderazione hanno l&#39;aspetto seguente:  ![](assets/modreco3.png)

   Per ulteriori informazioni sull&#39;utilizzo di Recommendations per moderazione in Contenuto app, consultate [Moderate Content Using App Content (Utilizzo di contenuti](/help/using/c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md#c_moderate_content_using_app_content)app per moderazione).
