---
description: Personalizza le marche temporali utilizzando Livefyre.js.
title: Personalizzare il timbro di data e ora
exl-id: 77130793-00ba-4a5c-8318-4221d971da6c
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 0%

---

# Personalizza la data e l&#39;ora del timbro{#customize-the-date-and-time-stamp}

Personalizza le marche temporali utilizzando Livefyre.js.

Le app Livefyre forniscono il parametro di opzione datetimeFormat, per specificare il formato di data come descritto di seguito.

* [Terminologia](#c_date_time_stamp/section_xsk_jn4_xz)
* [Formattazione](#c_date_time_stamp/section_ynx_gn4_xz)
* [Designazione del simbolo](#c_date_time_stamp/section_inq_2n4_xz)

## Terminologia {#section_xsk_jn4_xz}

* **Le marche** temporali assolute sono definite come ore esatte e specifiche (ad esempio 1 gennaio 2012 12:00)
* **Le marche** temporali relative sono definite come date generali e meno precise (ad esempio 25 secondi fa, 14 minuti fa, 1 giorno fa, 1 anno fa, ecc.)

## Formattazione {#section_ynx_gn4_xz}

Il parametro datetimeFormat ha il seguente comportamento predefinito quando non viene fornito alcun argomento:

* Formato data/ora di: MMMM gg aaaa (per l’8 gennaio 2012)
* 20160 Minuti (14 giorni) fino al tempo assoluto (14 giorni fino a quando le marche temporali relative diventano marche temporali assolute)

Il parametro datetimeFormat accetta tre possibili tipi di argomento: datetime, format e string.

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

Un oggetto che specifica AbsoluteFormat e/o minutesWaitAbsoluteTime. Un minutesFinoAbsoluteTime con un valore pari a -1 renderà immediatamente il tempo assoluto.

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

Funzione che utilizza come argomento un oggetto Date e restituisce una stringa datetime da visualizzare

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

Funzioni di formattazione di data/ora conformi alle specifiche del pattern definite in JDK, ICU e CLDR, con modifiche minori per l’utilizzo tipico in JS. Per ulteriori informazioni, consulta la [Documentazione della libreria di chiusura di Google](https://developers.google.com/closure/library/docs/overview).

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

Gli elementi contrassegnati con &quot;*&quot; non sono ancora supportati.

Gli elementi contrassegnati con &quot;#&quot; funzionano in modo diverso rispetto a Java.

Il formato viene determinato dal numero di lettere del pattern.

* **Testo:** 4 o superiore, utilizza il modulo completo. Meno di 4, utilizzare il formato breve o abbreviato se esiste. (Ad esempio: &quot;EEEE&quot; produce &quot;lunedì&quot;, &quot;EEE&quot; produce &quot;lun&quot;).
* **Numero:** il numero minimo di cifre. I numeri più brevi vengono aggiunti automaticamente a questa quantità (ad esempio: Se &quot;m&quot; produce &quot;6&quot;, &quot;mm&quot; produce &quot;06&quot;.). l&#39;anno è trattato in modo speciale; cioè, se il numero di &quot;y&quot; è 2, l’anno verrà troncato a 2 cifre. (Ad esempio: se &quot;yyyy&quot; produce &quot;1997&quot;, &quot;yy&quot; produce &quot;97&quot;.) A differenza di altri campi, i secondi frazionari vengono aggiunti a destra con zero.
* **Testo e numero:** 3 o superiore, utilizza il testo. Meno di 3, utilizzare il numero. (Ad esempio: &quot;M&quot; produce &quot;1&quot;, &quot;MM&quot; produce &quot;01&quot;, &quot;MMM&quot; produce &quot;Jan&quot; e &quot;MMMM&quot; produce &quot;gennaio&quot;.)

Qualsiasi carattere del pattern che non rientri negli intervalli di [&quot;a&quot;...&quot;z’] e [&quot;A&quot;..&quot;Z’] sarà trattato come testo tra virgolette. Ad esempio, i caratteri come &quot;:&quot;, &quot;.&quot;, &quot;, &quot;#&quot; e &quot;@&quot; appariranno nel testo temporale risultante anche se non sono racchiusi tra virgolette singole.
