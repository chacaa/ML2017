## Caso de estudio - Enfermedades cardíacas

### Problema
El problema se basa en el estudio de enfermedades cardíacas, a partir del estudio de 4 dataset de datos tomados de 4 lugares geográficamente distantes (Cleveland - EE.UU. EAST, Hungría, Suiza, y VA Long Beach - EE.UU. WEST), obtenidos del sitio web de la Universidad de California (Irvine). El objetivo principal de este estudio es la predicción de la existencia de enfermedades al corazón del paciente. A partir de estos datasets, se pretende lograr una predicción de si el paciente padece/rá (o no) una enfermedad cardíaca. 
Dado lo costoso de los tratamientos médicos para enfermedades cardíacas, la intención es poder a partir de estos datos, predecir  cuales son aquellos pacientes con mayor riesgo de enfermedades cardíacas, y así tratar a este tipo de pacientes de forma preventiva, y no reactiva. Con esto se disminuirían tanto los costos de tratamiento reactivo, así como evitar posibles cuadros cardíacos.

### Método de aprendizaje utilizado
Para este caso de estudio se trabajará con el método de [Regresión Logística](https://en.wikipedia.org/wiki/Logistic_regression), dentro del documento adjunto se explican las razones de la elección del mismo.

### Técnicas de separación de datos para la validación  
Las técnicas utilizadas en este caso de estudio son [Cross Validation](https://en.wikipedia.org/wiki/Cross-validation_(statistics)) y [Split Validation](https://docs.rapidminer.com/studio/operators/validation/split_validation.html).

### Herramienta utilizada
En este caso de estudio se trabajo con la herramienta [RapidMiner](https://docs.rapidminer.com).
