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
El problema planteado en este caso de estudio es poder crear y entrenar a partir de los datos históricos correspondientes al periodo de 1981-1990 de las temperaturas mínimas diarias de Melbourne, Australia, para poder luego aplicarlo a datos actuales similares para poder predecir la salida, en este caso la temperatura mínima para ese dia.
Dada la estructura intrínseca del problema es ideal para aplicar la técnica de Time Series Forecasting.

![Melbourne, Australia](http://www.abc.net.au/news/image/8041730-16x9-940x529.jpg)

### Información del dataset
Ref: [https://datamarket.com/data/set/2324/daily-minimum-temperatures-in-melbourne-australia-1981-1990#!ds=2324&display=line](https://datamarket.com/data/set/2324/daily-minimum-temperatures-in-melbourne-australia-1981-1990#!ds=2324&display=line)
* Total de datos: 3650
* Total de atributos: 2
* Total de valores faltantes: 0

Distribución de los datos del dataset:
![gráfica](https://3qeqpr26caki16dnhd19sv6by6v-wpengine.netdna-ssl.com/wp-content/uploads/2016/11/Minimum-Daily-Temperatures.png)

