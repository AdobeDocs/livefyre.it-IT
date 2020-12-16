---
description: Mediante Livefyre.js potete personalizzare i timbri relativi a data e ora.
seo-description: Mediante Livefyre.js potete personalizzare i timbri relativi a data e ora.
seo-title: Personalizzare il timbro di data e ora
solution: Experience Manager
title: Personalizzare il timbro di data e ora
uuid: 632ea405-56b7-4664-8d2b-0dd0a7611bd8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---


# Personalizza il timbro data e ora{#customize-the-date-and-time-stamp}

Mediante Livefyre.js potete personalizzare i timbri relativi a data e ora.

Le app Livefyre forniscono il parametro di opzione, datetimeFormat, per specificare il formato della data come descritto di seguito.

* [Terminologia](#c_date_time_stamp/section_xsk_jn4_xz)
* [Formattazione](#c_date_time_stamp/section_ynx_gn4_xz)
* [Designazione simbolo](#c_date_time_stamp/section_inq_2n4_xz)

## Terminologia {#section_xsk_jn4_xz}

* **Le marche** temporali assolute sono definite come ore esatte e specifiche (ad esempio 1 gennaio 2012 12:00)
* **I** timestamp relativi sono definiti come orari generali e meno precisi (ad esempio, 25 secondi fa, 14 minuti fa, 1 giorno fa, 1 anno fa, ecc.)

## Formattazione {#section_ynx_gn4_xz}

Il parametro datetimeFormat ha il seguente comportamento predefinito quando non viene fornito alcun argomento:

* Formato data/ora di: MMMM aaaa (per l’8 gennaio 2012)
* 20160 Minuti (14 giorni) fino a tempo assoluto (14 giorni fino a quando le marche temporali relative diventano timestamp assoluti)

Il parametro datetimeFormat accetta tre possibili tipi di argomenti: datetime, format e string.

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

Un oggetto che specifica AbsoluteFormat e/o minutesBeforeAbsoluteTime. Un valore di MinutiFinoAssolutoTime con un valore pari a -1 renderà immediato il tempo assoluto.

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

Una funzione che utilizza come argomento un oggetto Date e restituisce una stringa data/ora da visualizzare

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

## Designazione simbolo {#section_inq_2n4_xz}

Funzioni di formattazione di datetime seguendo la specifica del pattern definita in JDK, ICU e CLDR, con lievi modifiche per l&#39;uso tipico in JS. Per ulteriori informazioni, vedere la [Documentazione della libreria di chiusura Google](https://developers.google.com/closure/library/docs/overview).

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

Gli elementi contrassegnati con ‘*’ non sono ancora supportati.

Gli elementi contrassegnati con ‘#’ funzionano in modo diverso da Java.

Il numero di lettere del pattern determina il formato.

* **Testo:** 4 o superiore, utilizzare il modulo completo. Meno di 4, utilizzare il formato breve o abbreviato, se esiste. Ad esempio: &quot;EEEE&quot; produce &quot;Lunedì&quot;, &quot;EEE&quot; produce &quot;Luna&quot;.)
* **Numero:** il numero minimo di cifre. Numeri più brevi vengono aggiunti zero a questo importo (ad esempio: Se &quot;m&quot; produce &quot;6&quot;, &quot;mm&quot; produce &quot;06&quot;.) l&#39;anno è trattato in modo speciale; ovvero, se il numero di &quot;y&quot; è 2, l&#39;Anno verrà troncato a 2 cifre. Ad esempio: se &quot;yyyy&quot; produce &quot;1997&quot;, &quot;yy&quot; produce &quot;97&quot;.) A differenza di altri campi, i secondi frazionari vengono aggiunti a destra con zero.
* **Testo e numero:** 3 o superiore, utilizzate il testo. Meno di 3, utilizzare numero. Ad esempio: &quot;M&quot; produce &quot;1&quot;, &quot;MM&quot; produce &quot;01&quot;, &quot;MMM&quot; produce &quot;Jan&quot; e &quot;MMMM&quot; produce &quot;gennaio&quot;.)

Qualsiasi carattere del pattern che non sia compreso negli intervalli di [‘a’...z’] e [&quot;A&quot;.Z&#39;] verrà trattato come testo tra virgolette. Ad esempio, i caratteri come ‘:’, ‘.’, ‘, ‘#’ e ‘@’ verranno visualizzati nel testo temporale risultante anche se non sono racchiusi tra virgolette singole.
