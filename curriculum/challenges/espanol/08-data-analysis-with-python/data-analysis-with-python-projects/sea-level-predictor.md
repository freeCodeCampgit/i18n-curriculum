---
id: 5e4f5c4b570f7e3a4949899f
title: Pronosticador del nivel del mar
challengeType: 10
forumTopicId: 462370
dashedName: sea-level-predictor
---

# --description--

Estarás <a href="https://gitpod.io/?autostart=true#https://github.com/freeCodeCamp/boilerplate-sea-level-predictor/" target="_blank" rel="noopener noreferrer nofollow">trabajando en este proyecto con nuestro código inicial en Gitpod</a>.

Estamos desarrollando las instrucciones interactivas del currículo de Python. Aunque puedes encontrar los siguientes videos en el canal de YouTube de freeCodeCamp.org que te enseñaran lo necesario para realizar este proyecto:

- <a href="https://www.freecodecamp.org/news/python-for-everybody/" target="_blank" rel="noopener noreferrer nofollow">Python for Everybody Video Course</a> (14 hours)

- <a href="https://www.freecodecamp.org/news/how-to-analyze-data-with-python-pandas/" target="_blank" rel="noopener noreferrer nofollow">How to Analyze Data with Python Pandas</a> (10 hours)

# --instructions--

Analizará un conjunto de datos sobre el cambio del nivel medio del mar a nivel mundial desde 1880. Utilizarás los datos para predecir el cambio del nivel del mar hasta el año 2050.

Utiliza los datos para completar las siguientes tareas:

- Utiliza Pandas para importar los datos de `epa-sea-level.csv`.
- Use matplotlib to create a scatter plot using the `Year` column as the x-axis and the `CSIRO Adjusted Sea Level` column as the y-axis.
- Usa la función `linregress` de `scipy.stats` para obtener la pendiente e intersección con el eje y de la línea de mejor encaje. Dibuja la línea de mejor encaje sobre el diagrama de dispersión. Haz que la línea pase por el año 2050 para predecir el aumento del nivel del mar en ese año.
- Traza una nueva línea de mejor encaje utilizando datos del año 2000 hasta el año más reciente del conjunto de datos. Haz que la línea pase también por el año 2050 para predecir la subida del nivel del mar en 2050 si el ritmo de subida continúa como desde el año 2000.
- La etiqueta x debe ser `Year`, la etiqueta y debe ser `Sea Level (inches)` y el título debe ser `Rise in Sea Level`.

El boilerplate también incluye los comandos para guardar y devolver la imagen.

## Dessarrollo

Write your code in `sea_level_predictor.py`. Para el desarrollo, puedes utilizar `main.py` para probar tu código.

## Pruebas

Las pruebas unitarias para este proyecto están en `test_module.py`. Por defecto las pruebas del archivo `test_module.py` ya están importadas en el archivo `main.py` para su comodidad.

## Enviar

Copia la URL de tu proyecto y envíalo a freeCodeCamp.

## Fuente de datos

<a href="https://datahub.io/core/sea-level-rise" target="_blank" rel="noopener noreferrer nofollow">Global Average Absolute Sea Level Change</a>, 1880-2014 from the US Environmental Protection Agency using data from CSIRO, 2015; NOAA, 2015.


# --hints--

Debería pasar todas las pruebas de Python.

```js

```

# --solutions--

```py
  # Python challenges don't need solutions,
  # because they would need to be tested against a full working project.
  # Please check our contributing guidelines to learn more.
```
