---
description: Installazione delle librerie per le attività lato server di Livefyre
title: Installazione
exl-id: d74f85be-14c0-4f6d-8f16-b688282c0eb0
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 1%

---

# Installazione{#installation}


## Java {#section_yd3_3zk_rz}

Per installare la libreria Java, aggiungi questa dipendenza al POM del progetto:

```
<dependency> 
   <groupId>com.livefyre</groupId> 
   <artifactId>livefyre</artifactId> 
   <version>2.0.3</version> 
</dependency>
```

La libreria Java ha dipendenze dai seguenti moduli:

```
<dependency> 
   <groupId>com.sun.jersey</groupId> 
   <artifactId>jersey-client</artifactId> 
   <version>[1.18.1,)</version> 
</dependency> 
<dependency> 
   <groupId>com.google.code.gson</groupId> 
   <artifactId>gson</artifactId> 
   <version>[2.3,)</version> 
</dependency> 
<dependency> 
   <groupId>com.google.guava</groupId> 
   <artifactId>guava</artifactId> 
   <version>[18.0,)</version> 
</dependency> 
<dependency> 
   <groupId>org.apache.commons</groupId> 
   <artifactId>commons-lang3</artifactId> 
   <version>[3.0.1,)</version> 
</dependency> 
<dependency> 
   <groupId>org.bitbucket.b_c</groupId> 
   <artifactId>jose4j</artifactId> 
   <version>[0.4.1,)</version> 
</dependency> 
```

Per ulteriori informazioni, leggi i documenti Java o vedi l’origine su [GitHub](https://github.com/Livefyre/livefyre-java-utils).

## NodeJS {#section_swj_pwq_rz}

Per installare la libreria NodeJS, esegui questa riga:

`$ npm install livefyre`

La libreria NodeJS ha dipendenze dai seguenti moduli:

```
"restler":">=3.2.0", 
"validator":"=3.5.0", 
"jsonwebtoken": ">=5.0.0" 
```

Per ulteriori informazioni, leggi i documenti NodeJs o vedi l’origine su [GitHub](https://github.com/Livefyre/livefyre-nodejs-utils).

Collegamenti: [Restler](https://github.com/danwrong/restler), [Validator](https://www.npmjs.org/package/validator), [jsonwebtoken](https://github.com/auth0/node-jsonwebtoken).

## PHP {#section_txj_xwq_rz}

Per installare la libreria PHP con Composer, aggiungilo al tuo compositore.json:

```
"require": { 
   "livefyre/livefyre-php-utils": "2.0.4" 
}
```

Quindi installa utilizzando:

```
composer.phar install 
```

Se **non** utilizzi Compositore, ottieni la versione più recente della libreria utilizzando:

```
git clone https://github.com/Livefyre/livefyre-php-utils 
```

Per utilizzare la libreria, aggiungi quanto segue al tuo script PHP:

```
require_once("/path/to/livefyre-php-utils/src/Livefyre.php"); 
```

La libreria PHP ha dipendenze dai seguenti moduli:

```
"ext-json": "*", 
"rmccue/requests": ">=1.0" 
"firebase/php-jwt": ">=2.0" 
```

Per ulteriori informazioni, leggi i documenti PHP o vedi l&#39;origine su [GitHub](https://github.com/Livefyre/livefyre-php-utils).

Collegamenti: [ext-json](https://php.net/manual/en/book.json.php), [Richieste](https://github.com/rmccue/Requests/), [PHP-JWT](https://github.com/firebase/php-jwt/tree/v2.0.0)

## Python {#section_irk_fxq_rz}

Per installare la libreria Python, esegui questa riga:

`$ pip install livefyre`

La libreria Python ha dipendenze dai seguenti moduli:

```
PyJWT >= 1.0.1  
requests >= 2.2.1  
python-dateutil >= 2.2  
enum34 == 1.0  
ordereddict == 1.1 if sys.version_info[:2] < 2.7 
```

Per ulteriori informazioni, leggi i documenti Python o vedi l’origine su [GitHub](https://github.com/Livefyre/livefyre-python-utils).

Collegamenti: [PyJWT](https://github.com/progrium/pyjwt), [Richieste](https://github.com/kennethreitz/requests), [Python-Dateutil](https://pypi.python.org/pypi/python-dateutil), [Enum34](https://pypi.python.org/pypi/enum34), [OrderedDict](https://pypi.python.org/pypi/ordereddict)

## Ruby {#section_fv2_tzq_rz}

Per installare la libreria Ruby, aggiungi questa riga al file Gemfile della tua applicazione:

```
gem 'livefyre' 
```

Oppure installalo tu stesso:

`$ gem install livefyre`

La libreria Ruby ha dipendenze dai seguenti moduli:

```
"jwt", '~> 1.4', ">= 1.4.1"  
"rest-client", '~> 1.8', ">= 1.8.0"  
"addressable", '~> 2.3', ">= 2.3.6" 
```

Per ulteriori informazioni, leggi i documenti Ruby o vedi l&#39;origine su [GitHub](https://github.com/Livefyre/livefyre-ruby-utils).

Collegamenti: [Ruby JWT](https://github.com/firebase/php-jwt/tree/v2.0.0), [REST Client](https://github.com/rest-client/rest-client/), [Addressable](https://github.com/sporkmonger/addressable)
