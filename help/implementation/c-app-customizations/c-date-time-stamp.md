---
description: Personalizzate i timestamp con Livefyre. js.
seo-description: Personalizzate i timestamp con Livefyre. js.
seo-title: Personalizzare la data e l'ora
solution: Experience Manager
title: Personalizzare la data e l'ora
uuid: 632 ea 405-56 b 7-4664-8 d 2 b -0 dd 0 a 7611 bd 8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Personalizzare la data e l&#39;ora{#customize-the-date-and-time-stamp}

Personalizzate i timestamp con Livefyre. js.

Livefyre Apps fornisce il parametro di opzione datetimeformat per specificare il formato della data come descritto di seguito.

* [Terminologia](#c_date_time_stamp/section_xsk_jn4_xz)
* [Formattazione](#c_date_time_stamp/section_ynx_gn4_xz)
* [Designazione simboli](#c_date_time_stamp/section_inq_2n4_xz)

## Terminologia {#section_xsk_jn4_xz}

* **Le marche temporali assolute** sono definite come temporali specifici e specifici (ad esempio, 1 gennaio 2012 alle 12:00 PM)
* **Le marche temporali** relative sono definite come ora generale e meno precisa (ad esempio 25 secondi fa, 14 minuti fa, 1 giorno fa, 1 anno fa, ecc.)

## Formattazione {#section_ynx_gn4_xz}

Quando non viene fornito alcun argomento, il parametro datetimeformat ha il comportamento predefinito seguente:

* Formato Datetime di: MMMM g yyyy (per il 8 gennaio 2012)
* 20160 minuti (14 giorni) fino alla durata assoluta (14 giorni fino a quando le marche temporali relative diventano marche temporali assolute)

Il parametro datetimeformat accetta tre possibili tipi di argomenti: datetime, format e stringa.

```
// Example 1 (Datetime format string)  
var convConfig = { 
   "collectionMeta":"eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6InBvc3QgMiIsInVybCI6Imh0dHA6XC9cL29yYW5nZXNhcmVncmVhdC5jb21cL3VzZWExcDcwXzEyXC8_cD01IiwidGFncyI6IiIsImNoZWNrc3VtIjoiYjBiYzRkMmVmY2UyZWZkYzZkYTE4NmQ2ZGZhNmVkYzAiLCJhcnRpY2xlSWQiOjV9.XZJTJgwpiFZCQ6dv8vvl91sMbFSJndzZPTHhmtOaImo", 
   "checksum":"b0bc4d2efce2efdc6da186d6dfa6edc", 
   "siteId":"12345", 
   "articleId":5, 
   "el":"comments1", 
   "datetimeFormat": 'MMM d y Ka' 
}; 
var conv = fyre.conv.load(networkConfig, [convConfig]);
```

Un oggetto che specifica absoluteformat e/o minutesuntilabsolutetime. Un minutesuntilabsolutetime con un valore pari a -1 renderà immediatamente più immediato il tempo assoluto.

```
// Example 2 (Object)  
var convConfig = { 
   "collectionMeta":"eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6InBvc3QgMiIsInVybCI6Imh0dHA6XC9cL29yYW5nZXNhcmVncmVhdC5jb21cL3VzZWExcDcwXzEyXC8_cD01IiwidGFncyI6IiIsImNoZWNrc3VtIjoiYjBiYzRkMmVmY2UyZWZkYzZkYTE4NmQ2ZGZhNmVkYzAiLCJhcnRpY2xlSWQiOjV9.XZJTJgwpiFZCQ6dv8vvl91sMbFSJndzZPTHhmtOaImo", 
   "checksum":"b0bc4d2efce2efdc6da186d6dfa6edc", 
   "siteId":"12345", 
   "articleId":5, 
   "el":"comments1", 
   "datetimeFormat": { 
      minutesUntilAbsoluteTime: 10, 
      absoluteFormat: 'MMM d y Ka' 
   } 
};  
var conv = fyre.conv.load(networkConfig, [convConfig]);
```

Funzione che considera l&#39;argomento di un oggetto Date e restituisce una stringa datetime da visualizzare

```
// Example 3 (Function accepting a Date object, returning a datetime string to display) 
var convConfig = { 
   "collectionMeta":"eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6InBvc3QgMiIsInVybCI6Imh0dHA6XC9cL29yYW5nZXNhcmVncmVhdC5jb21cL3VzZWExcDcwXzEyXC8_cD01IiwidGFncyI6IiIsImNoZWNrc3VtIjoiYjBiYzRkMmVmY2UyZWZkYzZkYTE4NmQ2ZGZhNmVkYzAiLCJhcnRpY2xlSWQiOjV9.XZJTJgwpiFZCQ6dv8vvl91sMbFSJndzZPTHhmtOaImo", 
   "checksum":"b0bc4d2efce2efdc6da186d6dfa6edc", 
   "siteId":"12345", 
   "articleId":5, 
   "el":"comments1", 
   "datetimeFormat": function(theDateInput) { 
      return +theDateInput; 
   } 
};  
var conv = fyre.conv.load(networkConfig, [convConfig]);
```

## Designazione simboli {#section_inq_2n4_xz}

Funzioni di formattazione dati che seguono le specifiche del pattern definite in JDK, ICU e CLDR, con modifiche minori per l&#39;utilizzo tipico in JS. Per ulteriori informazioni, consulta la Documentazione della libreria di chiusura [di Google](https://developers.google.com/closure/library/docs/overview).

```
  Symbol Meaning Presentation        Example 
  ------   -------                 ------------        ------- 
  G        era designator          (Text)              AD 
  y#       year                    (Number)            1996 
  Y* year (week of year)     (Number)            1997 
  u* extended year           (Number)            4601 
  M        month in year           (Text & Number)     July & 07 
  d        day in month            (Number)            10 
  h        hour in am/pm (1~12)    (Number)            12 
  H        hour in day (0~23)      (Number)            0 
  m        minute in hour          (Number)            30 
  s        second in minute        (Number)            55 
  S        fractional second       (Number)            978 
  E        day of week             (Text)              Tuesday 
  e* day of week (local 1~7) (Number)            2 
  D* day in year             (Number)            189 
  F* day of week in month    (Number)            2 (2nd Wed in July) 
  w* week in year            (Number)            27 
  W* week in month           (Number)            2 
  a        am/pm marker            (Text)              PM 
  k        hour in day (1~24)      (Number)            24 
  K        hour in am/pm (0~11)    (Number)            0 
  z        time zone               (Text)              Pacific Standard Time 
  Z        time zone (RFC 822)     (Number)            -0800 
  v        time zone (generic)     (Text)              Pacific Time 
  g* Julian day              (Number)            2451334 
  A* milliseconds in day     (Number)            69540000 
  '        escape for text         (Delimiter)         'Date=' 
  ''       single quote            (Literal)           'o''clock'
```

Gli elementi contrassegnati con &#39;*&#39;non sono ancora supportati.

Gli elementi contrassegnati con &#39;#&#39;funzionano in modo diverso da Java.

Il numero di lettere del pattern determina il formato.

* **Testo:** 4 o più, utilizzare il modulo completo. Meno di 4, utilizzare il modulo breve o abbreviato, se esistente. (Ad esempio: «EEEE» genera «Lunedì», «EEE» genera «Lun».)
* **Numero:** il numero minimo di cifre. A valori più brevi corrisponde zero a questo valore (ad esempio: Se «m» genera «6», «mm» genera «06».) L&#39;anno è gestito in modo specifico; ovvero, se il conteggio dì y&#39;è 2, l&#39;anno verrà troncato a 2 cifre. (Ad esempio: se «aaaa» genera «1997», «yy» genera «97».) A differenza di altri campi, i secondi frazionari vengono inseriti sulla destra con zero.
* **Testo &amp; numero:** 3 o sopra, utilizzate il testo. Meno di 3, usa il numero. (Ad esempio: «M» produce «1», «MM» genera «01», «MMM» genera «Gen» e «MMMM» produce «Gennaio».)

Qualsiasi caratteri nel pattern che non si trova negli intervalli di [&#39;a &#39;. &#39;z&#39;] and [&#39;A &#39;. &#39;Z&#39;] verrà trattato come testo citato. Ad esempio, caratteri comè: &#39;,&#39;. &#39;,&#39;&#39;,&#39;#&#39;è@&#39;saranno visualizzati nel testo ora risultante persino se non vengono incorporati all&#39;interno di virgolette singole.
