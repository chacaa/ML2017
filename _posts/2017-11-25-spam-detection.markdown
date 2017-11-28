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
author-bio: I ♥ Machine Learning.
---
Hoy en dia es muy común que las empresas comuniquen sus promociones a través de mensajes de texto, esto genera malestar dado que muchas veces las ofertas/promociones que llegan no son del agrado o no interesan al usuario y para empeorar la situacion aun mas, llegan con mucha frecuencia.
A raíz de este problema es que nos resultó interesante investigar acerca de esto y poder encontrar una manera  de determinar de forma automática cuales mensajes corresponden a spam y cuáles no. Esto podría ser de gran ayuda si luego se quisiera automatizar la eliminación de los mismos o crear un aplicación que bloquee este tipo de mensajes.
Es por esta razón que se busco un dataset el cual nos permitiera realizar dicha investigación.
Lo que se busca con este caso de estudio es poder crear un modelo que permita predecir si un mensaje es SPAM o no.

![imagen de spam](http://cdn.makeuseof.com/wp-content/uploads/2016/10/sms-scam-994x400.jpg)

### Objetivos
* Poder aplicar lo aprendido durante el curso en una apliación real
* Obtener un modelo con una bena predicción
* Aplicar lo aprendido en estas semanas para construir un modelo con buen porcentaje de predicción
* Poder integrar RapidMiner con RapidMiner Server para poder consumir el servicio desde una App

### Análisis del problema
El problema que se plantea es poder a través de un atributo de entrada que corresponde a un SMS en inglés, poder predecir si el mismo corresponde a un mensaje de SPAM o no.
Claramente el caso de estudio plantea un problema de clasificación dado que se busca clasificar el SMS en alguna de las clases de salida. En este caso al solo poder tomar dos valores, SPAM o NO SPAM, y al ser un problema de clasificación podemos hilar más profundo y ver que nos encontramos frente a un claro problema de clasificación binaria.

### Análisis de los datos
El dataset utilizado fue obtenido se llama “SMS Spam Collection”, el mismo se puede encontrar entre los dataset ofrecidos por Kaggle a través de la siguiente [URL](https://www.kaggle.com/uciml/sms-spam-collection-dataset).
El dataset contiene 5.574 observaciones y no presenta valores faltantes. El mismo está compuesto por dos atributos:
* **result**: Corresponde al resultado de la observación, el mismo puede tomar los valores “ham” para el caso cuando el SMS es legítimo, mientras que toma el valor “spam” cuando el SMS es realmente SPAM. El atributo es binomial.
* **message**: Este atributo contiene el contenido del SMS, el cual es un mensaje en idioma inglés. Este atributo es polynomial.

### Técnica de validación del modelo
La técnica utilizada en este caso de estudio fue [Cross Validation](https://en.wikipedia.org/wiki/Cross-validation_(statistics)).

### Herramientas utilizadas
En este caso de estudio se trabajo con la herramientas [RapidMiner](https://docs.rapidminer.com) y [RapidMiner Server](https://docs.rapidminer.com/server).

### Solución
* Documento de la investigación en el siguiente [link](https://github.com/chacaa/ML2017/blob/master/Casos%20de%20estudio/Deteccion%20de%20SPAM/obligatorio%20grupal.pdf).
* Proceso de RapidMiner con la guía para replicar los resultados de la investigación en el siguiente [link](https://github.com/chacaa/ML2017/tree/master/Casos%20de%20estudio/Deteccion%20de%20SPAM), también contiene el código fuente de la aplicación construida para consumir el servicio.

### Análisis de los Resultados 
En el documento ya mostramos los resultados obtenidos por el proceso utilizado pero vamos a analizar los mismos.
![Resultados](https://raw.githubusercontent.com/chacaa/ML2017/master/Casos%20de%20estudio/Deteccion%20de%20SPAM/Results.jpeg)
Como se puede ver en la imagen la exactitud obtenida es del casi 97%, esto quiere decir que casi no hay falsos positivos y/o falsos negativos. La manera de verificar si el resultado obtenido es bueno es verificando el porcentaje recall del proceso, dado que el recall nos dice que cantidad de spam el modelo predijo sobre toda la cantidad de spam que tiene el dataset.

```recall = tp/(tp+fn)```

`tp` es la cantidad de spam que el modelo predijo que era spam y es realmente spam en el dataset.
`fn` es la cantidad de spam que hay en el dataset y que el modelo no predice como spam.
Como la clase a predecir es si el mensaje es spam o no obtuvimos casi un 85% de acierto, por lo que la cantidad de `fn` es baja.
Aparte la `precision` tambien es buena, porque obtuvimos casi 90% de acierto; lo que nos quiere decir que de todo lo que el modelo predijo como spam, solo una pequeña cantidad no lo fue.

```precision = tp/(tp+fp)```

`fp` es la cantidad de predicciones que hizo mal el modelo, es decir que es la cantidad de lo que el modelo predijo como spam y era legitimo.

### Conclusión
Se pudo aplicar todo lo aprendido durante el curso en una aplicación real, que creemos que podría llegar a aportar valor a terceros. Los resultados obtenidos fueron bastante buenos, y no solo se logró brindar una solución al problema sino que también todos los objetivos que se plantearon al principio del proyecto fueron cumplidos.

![Captura App Web](https://raw.githubusercontent.com/chacaa/ML2017/master/Casos%20de%20estudio/Deteccion%20de%20SPAM/webpage.PNG)
Captura de la applicación que consume el servicio, código fuente de la misma en el siguiente [link](https://github.com/chacaa/ML2017/blob/master/Casos%20de%20estudio/Deteccion%20de%20SPAM/spamtest.html).
