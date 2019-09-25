---
description: Installazione delle librerie per le attività lato server di Livefyre
seo-description: Installazione delle librerie per le attività lato server di Livefyre
seo-title: Installazione
solution: Experience Manager
title: Installazione
uuid: f60b4cc7-178f-4a16-ba75-f1d0d171c52f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Installazione{#installation}


## Java {#section_yd3_3zk_rz}

Per installare la libreria Java, aggiungete questa dipendenza al POM del progetto:

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

Per ulteriori informazioni, leggi i documenti Java o vedi l'origine su [GitHub](https://github.com/Livefyre/livefyre-java-utils).

## NodeJS {#section_swj_pwq_rz}

Per installare la libreria NodeJS, eseguire la riga seguente:

`$ npm install livefyre`

La libreria NodeJS ha dipendenze dai seguenti moduli:

```
"restler":">=3.2.0", 
"validator":"=3.5.0", 
"jsonwebtoken": ">=5.0.0" 
```

Per ulteriori informazioni, leggi i documenti NodeJs o vedi l'origine su [GitHub](https://github.com/Livefyre/livefyre-nodejs-utils).

Collegamenti: [Restler](https://github.com/danwrong/restler), [Validator](https://www.npmjs.org/package/validator), [jsonwebtoken](https://github.com/auth0/node-jsonwebtoken).

## PHP {#section_txj_xwq_rz}

Per installare la libreria PHP con Composer, aggiungete questo a composer.json:

```
"require": { 
   "livefyre/livefyre-php-utils": "2.0.4" 
}
```

Quindi effettuate l’installazione utilizzando:

```
composer.phar install 
```

Se **non** utilizzate Composer, ottenete la versione più recente della libreria utilizzando:

```
git clone https://github.com/Livefyre/livefyre-php-utils 
```

Per utilizzare la libreria, aggiungere quanto segue allo script PHP:

```
require_once("/path/to/livefyre-php-utils/src/Livefyre.php"); 
```

La libreria PHP ha dipendenze dai seguenti moduli:

```
"ext-json": "*", 
"rmccue/requests": ">=1.0" 
"firebase/php-jwt": ">=2.0" 
```

Per ulteriori informazioni, leggi i documenti PHP o vedi l'origine su [GitHub](https://github.com/Livefyre/livefyre-php-utils).

Collegamenti: [ext-json](https://php.net/manual/en/book.json.php), [richieste](https://github.com/rmccue/Requests/), [PHP-JWT](https://github.com/firebase/php-jwt/tree/v2.0.0)

## Python {#section_irk_fxq_rz}

Per installare la libreria Python, eseguite questa riga:

`$ pip install livefyre`

La libreria Python ha dipendenze dai seguenti moduli:

```
PyJWT >= 1.0.1  
requests >= 2.2.1  
python-dateutil >= 2.2  
enum34 == 1.0  
ordereddict == 1.1 if sys.version_info[:2] < 2.7 
```

Per ulteriori informazioni, leggi i documenti Python o vedi la fonte su [GitHub](https://github.com/Livefyre/livefyre-python-utils).

Collegamenti: [PyJWT](https://github.com/progrium/pyjwt), [Richieste](https://github.com/kennethreitz/requests), [Python-Dateutil](https://pypi.python.org/pypi/python-dateutil), [Enum34](https://pypi.python.org/pypi/enum34), [OrderedDict](https://pypi.python.org/pypi/ordereddict)

## Ruby {#section_fv2_tzq_rz}

Per installare la libreria Ruby, aggiungete questa riga al file Gemfile dell’applicazione:

```
gem 'livefyre' 
```

Oppure installalo autonomamente:

`$ gem install livefyre`

La libreria Ruby ha dipendenze dai seguenti moduli:

```
"jwt", '~> 1.4', ">= 1.4.1"  
"rest-client", '~> 1.8', ">= 1.8.0"  
"addressable", '~> 2.3', ">= 2.3.6" 
```

Per ulteriori informazioni, leggi i documenti Ruby o vedi l'origine su [GitHub](https://github.com/Livefyre/livefyre-ruby-utils).

Collegamenti: [Ruby JWT](https://github.com/firebase/php-jwt/tree/v2.0.0), [REST Client](https://github.com/rest-client/rest-client/), [indirizzabile](https://github.com/sporkmonger/addressable)
