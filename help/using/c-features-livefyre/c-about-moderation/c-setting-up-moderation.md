---
description: Utilizza la scheda Moderazione per impostare le regole di moderazione per i contenuti in arrivo, inclusi gli elenchi di profanità, le regole di flag e gli indirizzi IP banditi.
title: Impostazione della moderazione
exl-id: 09fc44c4-7ee1-47fd-ae68-885532a6f03f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '1276'
ht-degree: 0%

---

# Impostazione della moderazione{#setting-up-moderation}

Utilizza la scheda Moderazione per impostare le regole di moderazione per i contenuti in arrivo, inclusi gli elenchi di profanità, le regole di flag e gli indirizzi IP banditi.

## Funzionamento della moderazione {#section_kyf_gvc_t1b}

Puoi moderare il contenuto nei seguenti modi:

* Premodera automaticamente il contenuto per filtrare il contenuto indesiderato in base alle regole impostate prima della pubblicazione.
* Elimina o approva manualmente il contenuto contrassegnato utilizzando la moderazione automatica utilizzando ModQ o il contenuto dell&#39;app nella libreria.
* Identifica i visitatori del sito che pubblicano ripetutamente contenuti offensivi per impedirne la pubblicazione vietando specifici utenti Livefyre, utenti social o indirizzi IP.
* Identifica le persone e i contenuti che possono sempre essere visualizzati dagli utenti inseriti nell’elenco Consentiti o disattivando i filtri per flussi, siti o reti specifici.

È possibile premoderare automaticamente il contenuto nei seguenti modi:

* Imposta regole per contrassegnare automaticamente determinati tipi di contenuto:

   * Imposta le regole di flag per il contenuto contrassegnato dal flag dei visitatori del sito utilizzando **[!UICONTROL Settings > Moderation > Rules]**
   * Imposta le regole SAFE utilizzando **[!UICONTROL Settings > Moderation > Rules]**
   * Divieto per gli utenti Twitter specifici di utilizzare **[!UICONTROL Settings > Streams]**
   * Divieto di indirizzi IP utilizzando **[!UICONTROL Settings > Bans]**
   * Divieto di regione IP per codice del paese su richiesta. Il contenuto proibito verrà contrassegnato come SPAM.

* Crea un elenco di parole che consideri profanity nell&#39;elenco Profanity in **[!UICONTROL Settings > Moderation > Rules]** per la rete o il sito.
* Consenti agli utenti dell’elenco (consentire sempre la visualizzazione del contenuto di questi utenti) utilizzando o disattivando i filtri per flussi, siti o reti specifici.

Dopo aver impostato gli elenchi di profilo, i filtri SAFE e le regole, puoi scegliere se eseguire la premoderazione del contenuto e applicare i filtri SAFE nei flussi. Per ulteriori informazioni, consulta [Opzioni regola flusso per tutte le regole di flusso](/help/using/c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

Livefyre contrassegna il contenuto come **[!UICONTROL Approved]**, **[!UICONTROL Pending]**, **[!UICONTROL Junk]**, ecc. a seconda di dove provengono i contenuti, dove verranno pubblicati e quali regole sono state impostate nel sistema. La tabella seguente descrive in dettaglio le azioni eseguite da Livefyre, a seconda di questi fattori.

## Come funziona la moderazione

| Contenuto Proviene da: | Invio di contenuti a: | Stato di approvazione |
|--- |--- |--- |
| Libreria | App | Contenuto approvato |
| Ricerca social | App | Contenuto approvato |
| Regola flusso | App | Il contenuto è contrassegnato come spazzatura dal filtro SAFE? <br><ul><li>No - Flusso di lavoro di moderazione da flusso a app</li><li>Sì - Contenuto tracciato</li></ul> |
| Libreria | Cartella | Nessun stato (nella cartella, non pubblicato, non eliminato) |
| Ricerca social | Cartella | Nessun stato (nella cartella, non pubblicato, non eliminato) |
| Regola flusso | Cartella | Il contenuto è contrassegnato come spazzatura dal filtro SAFE? <br><ul><li>No - Nessun stato (nella cartella, non pubblicato, non eliminato)</li><li>Sì - Contenuto tracciato</li></ul> |
| Post app | App | Il contenuto è contrassegnato come spazzatura dal filtro SAFE? <br><ul><li>No - Flusso di lavoro di moderazione post-in-app</li><li>Sì - Contenuto tracciato</li></ul> |

## Flusso di lavoro di moderazione da flusso a app {#section_z5z_w4d_t1b}

![](assets/stream_to_app_workflow.png)

Prima che il contenuto di un flusso venga pubblicato in un’app, Livefyre esegue i seguenti controlli per determinare cosa fare con il contenuto:

1. Se SAFE contrassegna il contenuto come spazzatura o goccia, Livefyre lo elimina.
1. Se SAFE non contrassegna il contenuto come spazzatura, Livefyre controlla se la moderazione è attivata.
1. Se la moderazione è attivata, Livefyre contrassegna il contenuto come in sospeso.
1. Se imposti le regole ModQ, allora Livefyre invia il contenuto a ModQ.
1. Se la moderazione non è attivata, Livefyre controlla se SAFE ha segnalato il contenuto.
1. Se SAFE ha segnalato il contenuto, Livefyre lo approva e lo pubblica nell’app.
1. Se SAFE contrassegna il contenuto e non hai impostato regole SAFE, allora Livefyre approva il contenuto e lo pubblica nell’app.
1. Se SAFE contrassegna il contenuto e imposti regole SAFE, Livefyre controlla se hai impostato regole SAFE per lo Stream.
1. Se imposti regole SAFE per il flusso, Livefyre approva il contenuto e lo pubblica nell’app. Se non hai impostato regole SAFE per il flusso, Livefyre utilizza le regole SAFE di moderazione per determinare come gestire il contenuto (inviare a ModQ, spazzatura, ecc.).

## Flusso di lavoro di moderazione post-in-app {#section_fwn_w4d_t1b}

![](assets/post_to_app_workflow.png)

Prima che il contenuto di un post di un’app venga pubblicato in un’app, Livefyre esegue i seguenti controlli per determinare cosa fare con il contenuto:

1. Se il filtro SAFE contrassegna il contenuto come rilascio, Livefyre rilascia il contenuto.
1. Se SAFE non contrassegna il contenuto come rilascio, Livefyre controlla se la moderazione è attivata. Se la moderazione è attivata, Livefyre contrassegna il contenuto come in sospeso. Se imposti le regole ModQ, allora Livefyre invia il contenuto a ModQ come in sospeso. In caso contrario, il contenuto rimane in sospeso in Contenuto app nella libreria.
1. Se la moderazione non è attivata, Livefyre controlla se SAFE ha segnalato il contenuto. In caso contrario, Livefyre approva il contenuto e lo pubblica nell’app.
1. Se SAFE contrassegna il contenuto e imposti regole SAFE, Livefyre utilizza la regola SAFE per determinare come gestire il contenuto (inviare a ModQ, spazzatura, ecc.). Se SAFE contrassegna il contenuto e non hai impostato regole SAFE, allora Livefyre approva il contenuto e lo pubblica nell’app.

## Filtri in blocco {#section_lyk_ktx_vy}

Il filtro collettivo cerca contenuti ripetitivi pubblicati su tutte le reti Livefyre in un breve arco di tempo. Se rilevato, questo contenuto viene contrassegnato come Bulk e quindi eliminato per impostazione predefinita. Anche se il contenuto in blocco può essere generato dall’utente (ad esempio, &quot;Touchdown&quot;) pubblicato ripetutamente in una chat durante una partita di calcio popolare), la maggior parte ha origine con campagne di spam. Questo filtro è indipendente dalla lingua e funziona con qualsiasi lingua. Per personalizzare il filtro di massa, è necessario contattare il supporto Livefyre.

## Regole {#section_gqz_ksk_f1b}

Utilizza la sezione Regole per creare regole di pre-moderazione, basate su flag SICURI e applicati dall’utente. Questo pannello offre due tipi di regole:

* **[!UICONTROL Flag Rules:]** specifica un’azione da eseguire su un commento contrassegnato dagli utenti un numero definito di volte.
* **[!UICONTROL SAFE Rules:]**combinare i flag SAFE con le azioni da eseguire sul contenuto contrassegnato.

Per creare le regole di contrassegno, selezionare il flag (Offensive, Off Topic, Non d’accordo o Spam), immettere il numero di volte in cui deve essere applicato a un contenuto e selezionare l’azione da eseguire. È possibile impostare una regola di flag per ogni opzione di flag (Offensive, Off Topic, Disagreement o Spam).

Puoi creare regole a livello di rete, sito e flusso. Le regole a livello di sito ereditano le regole di rete, a meno che non si configurino diversamente le regole del sito. Le regole del flusso ereditano le regole del sito a meno che non vengano configurate in modo diverso.

Azioni disponibili:

* **[!UICONTROL Trash it:]**invia il commento contrassegnato al cestino.
* **[!UICONTROL Bozo it:]** nasconde il commento contrassegnato da tutti gli utenti, ad eccezione del relativo autore, a cui rimane visibile.
* **[!UICONTROL Pending:]** imposta il contenuto come in sospeso. Se si imposta Premoderazione su ON in **[!UICONTROL Settings > ModQ]**, sarà nel ModQ. Altrimenti sarà solo in Contenuto app.

>[!NOTE]
>
>Livefyre consiglia di creare regole per i commenti Bozo contrassegnati come spam o offensivo da cinque utenti.

## Recommendations di moderazione {#section_ec3_vr3_2cb}

Puoi utilizzare i consigli di moderazione per aiutarti a determinare come moderare i contenuti pubblicati dai visitatori del sito nelle app Livefyre. L’indicatore di raccomandazione per moderazione consiglia di indicare quando è probabile che una parte di contenuto venga eliminata, in base alle azioni eseguite in precedenza su contenuti simili. Per utilizzare Recommendations di moderazione:

1. Attiva la funzionalità Recommendations di moderazione contattando il tuo professionista di supporto Adobe Livefyre.
1. Imposta i consigli di moderazione in Impostazioni di rete.

   Imposta i consigli di moderazione utilizzando l&#39;impostazione **[!UICONTROL Livefyre Recommends Trash]** in **[!UICONTROL Network Settings]**.

   ![](assets/image_mod_reco_trash.png)

1. Imposta una regola SAFE per dire a Livefyre cosa fare con i contenuti che la raccomandazione di moderazione identifica come contenuti che probabilmente verranno eliminati. Per ulteriori informazioni su come impostare una regola SAFE per l&#39;opzione **[!UICONTROL Livefyre Recommends Trash]**, vedere [Moderazione](/help/using/c-features-livefyre/c-about-moderation/c-moderation.md#c_moderation).

   ![](assets/modreco4.png)

1. Utilizza il **[!UICONTROL Moderation Recommendation Indicator]** nel ModQ o nel contenuto dell&#39;app per filtrare il contenuto che la raccomandazione di moderazione identifica come probabile venga eliminato.

   In ModQ l&#39;indicatore si presenta così:  ![](assets/mod_reco1.png)

   Per ulteriori informazioni su come utilizzare Recommendations per moderare i contenuti in ModQ, consulta [ModQ](/help/using/c-features-livefyre/c-about-moderation/c-modq.md#c_modq).

   In Contenuto app, i consigli di moderazione si presentano così:  ![](assets/modreco3.png)

   Per ulteriori informazioni su come utilizzare Recommendations per moderazione nel contenuto delle app, consulta [Contenuti moderati utilizzando il contenuto delle app](/help/using/c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md#c_moderate_content_using_app_content).
