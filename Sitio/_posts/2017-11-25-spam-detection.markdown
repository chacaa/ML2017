---
layout: post
title:  Detección de SPAM
subtitle: Caso de estudio
description: Hoy en dia es muy común que las empresas comuniquen sus promociones a través de mensajes de texto, esto genera malestar dado que muchas veces las ofertas/promociones que llegan no son del agrado o no interesan al usuario y para empeorar la situacion aun mas, llegan con mucha frecuencia.
date:   2017-11-25 13:55:47
categories: casos
featured-image: http://www.yomzansi.com/wp-content/uploads/2015/11/avoid-spam-sms-yomzansi.jpg
thumbnail-image: http://www.yomzansi.com/wp-content/uploads/2015/11/avoid-spam-sms-yomzansi.jpg
comments: false
author: Santiago Casás
author-image: http://img.sparknotes.com/content/sparklife/sparktalk/nov2016litchardeathquiz1_MediumWide.jpg
author-bio: I love playing outside, fort building, and skiing powder with my wife and dog.  Currently a front end devloper at AppNeta.
---
Hoy en dia es muy común que las empresas comuniquen sus promociones a través de mensajes de texto, esto genera malestar dado que muchas veces las ofertas/promociones que llegan no son del agrado o no interesan al usuario y para empeorar la situacion aun mas, llegan con mucha frecuencia.
A raíz de este problema es que nos resultó interesante investigar acerca de esto y poder encontrar una manera  de determinar de forma automática cuales mensajes corresponden a spam y cuáles no. Esto podría ser de gran ayuda si luego se quisiera automatizar la eliminación de los mismos o crear un aplicación que bloquee este tipo de mensajes.
Es por esta razón que se busco un dataset el cual nos permitiera realizar dicha investigación.
Lo que se busca con este caso de estudio es poder crear un modelo que permita predecir si un mensaje es SPAM o no.

### Análisis del problema
El problema que se plantea es poder a través de un atributo de entrada que corresponde a un SMS en inglés, poder predecir si el mismo corresponde a un mensaje de SPAM o no.
Claramente el caso de estudio plantea un problema de clasificación dado que se busca clasificar el SMS en alguna de las clases de salida. En este caso al solo poder tomar dos valores, SPAM o NO SPAM, y al ser un problema de clasificación podemos hilar más profundo y ver que nos encontramos frente a un claro problema de clasificación binaria.

### Análisis de los datos
El dataset utilizado fue obtenido se llama “SMS Spam Collection”, el mismo se puede encontrar entre los dataset ofrecidos por Kaggle a través de la siguiente [URL](https://www.kaggle.com/uciml/sms-spam-collection-dataset).
El dataset contiene 5.574 observaciones y no presenta valores faltantes. El mismo está compuesto por dos atributos:
* **result**: Corresponde al resultado de la observación, el mismo puede tomar los valores “ham” para el caso cuando el SMS es legítimo, mientras que toma el valor “spam” cuando el SMS es realmente SPAM. El atributo es binomial.
* **message**: Este atributo contiene el contenido del SMS, el cual es un mensaje en idioma inglés. Este atributo es polynomial.


