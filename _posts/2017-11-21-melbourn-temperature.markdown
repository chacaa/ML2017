---
layout: post
title:  Temperatura mínima en Melbourne
subtitle: Caso de estudio
description:  El problema planteado en este caso de estudio es poder crear y entrenar a partir de los datos históricos correspondientes al periodo de 1981-1990 de las temperaturas mínimas diarias de Melbourne, Australia, para poder luego aplicarlo a datos actuales similares para poder predecir la salida, en este caso la temperatura mínima para ese dia.
date:   2017-11-21 20:08:05
categories: casos
featured-image: https://www.cray.com/blog/wp-content/uploads/2015/09/Weather-Blog-Image.jpg
thumbnail-image: https://www.cray.com/blog/wp-content/uploads/2015/09/Weather-Blog-Image.jpg
comments: true
author: Gianni Iaquinta
author-image: http://img.sparknotes.com/content/sparklife/sparktalk/nov2016litchardeathquiz1_MediumWide.jpg
author-bio: I ♥ Machine Learning.
---
Hoy en dia la tecnología a avanzado hasta cierto punto que es posible predecir con mas exactitud los hechos del futuro en base a como se a comportado en su pasado, a este tipo de técnica se la conoce como Time Series.
Este tipo de técnica se aplica en varias áreas como ser finanzas, meteorología, industria, entre otros.
![Melbourne, Australia](http://www.abc.net.au/news/image/8041730-16x9-940x529.jpg)

### Objetivos
* Aplicar lo aprendido sobre Time Series
* Obtener un modelo con una buena predicción

### Análisis del problema
El problema planteado en este caso de estudio es poder crear y entrenar a partir de los datos históricos correspondientes al periodo de 1981-1990 de las temperaturas mínimas diarias de Melbourne, Australia, para poder luego aplicarlo a datos actuales similares para poder predecir la salida, en este caso la temperatura mínima para ese dia.
Dada la estructura intrínseca del problema es ideal para aplicar la técnica de Time Series Forecasting.

### Análisis de los datos
Ref: [https://datamarket.com/data/set/2324/daily-minimum-temperatures-in-melbourne-australia-1981-1990#!ds=2324&display=line](https://datamarket.com/data/set/2324/daily-minimum-temperatures-in-melbourne-australia-1981-1990#!ds=2324&display=line)
* Total de datos: 3650
* Total de atributos: 2
* Total de valores faltantes: 0

Distribución de los datos del dataset:
![gráfica](https://3qeqpr26caki16dnhd19sv6by6v-wpengine.netdna-ssl.com/wp-content/uploads/2016/11/Minimum-Daily-Temperatures.png)

### Técnica de validación del modelo
La técnica utilizada en este caso de estudio es [Cross Validation](https://en.wikipedia.org/wiki/Cross-validation_(statistics)). 

### Herramienta utilizada
En este caso de estudio se trabajo con la herramienta [RapidMiner](https://docs.rapidminer.com).

### Método de aprendizaje utilizado
Para este caso de estudio se trabajará con el método de [Time Series](https://en.wikipedia.org/wiki/Time_series), dentro del [documento adjunto](https://github.com/chacaa/ML2017/tree/master/Casos%20de%20estudio/Temperaturas%20m%C3%ADnimas%20en%20Melbourne/documento.pdf) se explican las razones de la elección del mismo.

### Solución
* Documento de la investigación en el siguiente [link](https://github.com/chacaa/ML2017/tree/master/Casos%20de%20estudio/Temperaturas%20m%C3%ADnimas%20en%20Melbourne/documento.pdf).
* Proceso de RapidMiner con la guía para replicar los resultados de la investigación en el siguiente [link](https://github.com/chacaa/ML2017/tree/master/Casos%20de%20estudio/Temperaturas%20m%C3%ADnimas%20en%20Melbourne).

### Análisis de los Resultados 
En el documento ya mostramos los resultados obtenidos por el proceso utilizado pero vamos a analizar los mismos.
![Resultados](https://raw.githubusercontent.com/chacaa/ML2017/master/Casos%20de%20estudio/Temperaturas%20m%C3%ADnimas%20en%20Melbourne/Results.png)
La gráfica de la imagen muestra la predicción del comportamiento de la temperatura en meses posteriores y dada la imagen de los datos podemos observar que los mismos se predijeron correctamente.

### Conclusión
La técnica es muy utilizada actualmente en la industria, estadistica, finanzas, etc. para poder predecir el posible comportamiento de la variable analizada. Para poder realizar esta prueba se precisa un dataset confiable y grande para poder obtener una buena predicción. Si esto no se cumple pueden haber predicciones erroneas.
 *Análisis de los Resultados* en el [documento del estudio](https://github.com/chacaa/ML2017/tree/master/Casos%20de%20estudio/Temperaturas%20m%C3%ADnimas%20en%20Melbourne/documento.pdf)











