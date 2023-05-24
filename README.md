# PROYECTO INDIVIDUAL Nº2: Data Analitycs

## Introducción
Al finalizar el bootcamp de Data Science de Henry, se asignan dos proyectos individuales y un proyecto grupal, con el objetivo de integrar los conocimientos adquiridos en la etapa de bootcamp.

Para el segundo proyecto individual sobre Data Analitycs se realizó un EDA, un análisis descriptivo, se definieron KPIs y se creó un dashboard interactivo sobre accidentes aéreos. 

En [este repositorio](https://github.com/soyHenry/PI03-Analytics) se encuentran las consignas y en [este link](https://github.com/scioffi96/PI_DataAnalitycs/blob/main/AccidentesAviones.csv) se encuentra el dataset.

## EDA: Análisis Exploratorio de los datos

En primera instancia se realizó el análisis exploratorio de los datos a través de un notebook de Python, en [este link](https://github.com/scioffi96/PI_DataAnalitycs/blob/main/proyecto2.ipynb) se puede observar el análisis en notebook en detalle.

Lo primero que se realizó fue cargar el dataset, luego se interpretaron los campos del mismo y se buscaron aquellos campos difíciles de interpretar.
Seguidamente, le dieron nombres más intuitivos a todas las columnas y se eliminaron aquellos campos que no aportarían al análisis. 

Después se realizaron las transformaciones de las columnas que quedaron:

- Se normalizaron las columnas *date, time, route, toal_aboard, passengers_aboard, crew_aboard, total_fatalities, passengers_fatalities* y *crew_fatalities*, eliminando valores nulos y reemplazando valores erróneos (el más común fue encontrar '?' en vez de nulos).
- En base a *location* se creó un nuevo campo llamado *country*, en el que sólo se encuentra el país de la localización. 
- En base a *airline_operator* se creó la columna *category*, la cual dice si el vuelo era militar o comercial.
- A partir de *aircraft_type* : se clasifican los registros según si la aeronave era dirigibles, helicopteros o avión.

- Duplicados: debido a las acciones realizadas previamente, no nos encontramos con duplicados

- Nulos: se encontraron enrte 4% y 5% de valores nulos en cuatro campos del dataset, por lo queno se consideraron representativos respecto al total, por ende no se decidió eliminar dichos registros con el fin de utilizarlos en otros campos.

- Se creó el campo *season*, el cual dice qué estación del año era en el momento del accidente.

- Se creó el campo *surface_type*, en donde se clasifica el tipo de terreno en el cual dice cayó el avión: tierra o agua.

- Se creó el campo *accident_type*, en donde se clasifica el motivo del accidente, entre loas principales motivos se encontrarón: falla en despegue o aterrizaje, terreno, fallas mecanicas, condiciones meteorológicas y errores de navegación.

- Entre otras transformaciones.

Finalmente, a [este dataset](https://github.com/scioffi96/PI_DataAnalitycs/blob/main/dataframe_powerbi) transformado se lo exportó para usarlo en las visualizaciones en PowerBi.

## Análisis Descriptivo

Se puede separar el análisis descriptivo en: análisis cuantitativo y análisis cualitativo.

### Análisis cuantitativo

En el análisis descriptivo lo primero que se realizó fue una descripción de los valores numéricos, como promedios, cantidades, mínimos, máximos, etc.

Luego se realizó un análisis de outliers, donde si bien se encontraron outliers, se decidió dejar los datos ya que no son valores erróneos.

También se realizó una matriz de correlación, donde se observaron variables estrechamente relacionadas.

## Análisis cualitativo

En el análisis cualitativo se realizaron gráficos y una breve interpretación de cada uno. Algunos ejemplos de los gráficos llevados a cabo son: 
- Accidentes y fatalidades por año, 
- Accidentes por mes, día y hora, 
- Accidentes según país, 
- Accidentes según modelo la aeronave,
- Cantidad de vuelos comerciales vs vuelos militares,
- Cantidad de accidentes según su motivo,
- entre otros.

## KPI

Finalmente se sugirieron tres KPI además del KPI propuesto por Henry.

El KPI propuesto es:
- Reducir en 5% la tasa de mortalidad a nivel anual, siendo el número de fallecidos en los accidentes aéreos respecto al total de personas en los vuelos involucrados.

Los KPI sugeridos son: 

- Aumentar la tasa de supervicencia según el total de personas a bordo en 5% anual.
- Reducir 5% anualmente la tasa de accidentes de Estados Unidos respecto al resto de los paises.
- Reducir la tasa de accidentes en despegues o aterrizajes en un 10% anual.

Estos KPI se encuentran presentes en el dashboard, además de otros gráficos.

## Dashboard

Para finalizar con el proyecto, se creó un dashboard en PowerBI para presentar el proyecto.
El mismo se encuentra en este mismo repositorio. 

![Dashboard](https://github.com/scioffi96/PI_DataAnalitycs/blob/main/dashboard_portada.PNG)
