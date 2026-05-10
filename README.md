# Movilidad-urbana-y-productividad-econ-mica-en-ciudades-de-LATAM
Analisis sobre la relación que existe entre el tráfico de las principales ciudades de Latinoamerica y el PIB per cápita.

# Resumen ejecutivo

**Contexto & objetivo:**  
Pregunta central del análisis: ¿qué relación existe entre la movilidad urbana (congestión, tiempos de viaje) y la productividad económica (PIB per cápita)?

El análisis revela una correlación débil entre el tráfico y el desarrollo económico per cápita en algunas ciudades estudiadas. No obstante, esta relación no es consistente en todas las urbes latinoamericanas, lo que sugiere que el tráfico vehicular es un indicador insuficiente del desarrollo económico. Las variables seleccionadas para este estudio fueron elegidas con el propósito de identificar patrones relacionales que permitan explicar las variaciones observadas entre ciudades.

**Cobertura de datos:**  
Años analizados, número de ciudades y países incluidos.

Se toman datos del año 2024 ya que es el año más próximo y con más información de la que podemos analizar. Se toman en cuenta solamente ciudades de paises latinoamericanas para tener una perspectiva más próxima a nuestras realidades cercanas.

**Metodología:**  
Los procesos de limpieza aplicados en este reporte consistieron en convertir a formato tipo fecha columnas como UpdateTimeUTC y UpdateTimeUTC en el dataset de eco, cambio de formato de object a float64 por parte de las columnas City GDP/capita y Unemployment ya que se encuentran en %, y eliminar o cambiar de (.) a (,) en columnas city_gdp_capita, unemployment_pct y population_m en el dataset eco.

Para poder relacionar ambos datasets, se utiliza como claves de unión a las columnas "city" y "year", así se mantienen solo las ciudades y años presentes en ambos datasets. De esta manera se realiza la unión de los datasets de trafico y economia por medio de INNER.

El análisis de la distribución del GDP per cápita revela una concentración en el rango de USD 7,000 a USD 11,000. Simultáneamente, se observan valores atípicos (outliers) en el promedio de congestión vehicular (JamsDelay), así como una asociación débil y no generalizable entre la congestión vehicular y el PIB per cápita en las ciudades latinoamericanas analizadas, presente solo en casos específicos.

**Hallazgos iniciales:**  
Los patrones más importantes entre índices de tráfico y GDP per cápita se ubican en ciudades como Mexico City, Lima y Sao Paulo, sin embargo esto no sucede en la misma proporción en todas las ciudades de latinoamerica. Por el momento, no se encontraron anomalías u outliers en los resultados en la correlación de estos datos.

**Recomendaciones**  
Analizando las relaciones entre el trafico y el GDP per cápital, a pesar de que no exista una relación necesaria en todas las ciudades, se podría implementar aciones (propuestas de inversión) en ciudades como Santiago, donde la cantidad de tráfico es considerable, no de los peores casos, pero el GDP per capital es bajo en comparación con ciudades con más ingresos como Mexico City o Montevideo. En un futuro pudiera ser que se puedan utilizar otros parametros a comparar y verificar si se pueden encontrar otro tipo de relaciones.

La ciudad que muestra la mayor correlación significativa entre altos niveles de congestión vehicular y bajos indicadores de productividad económica, sugiriendo ser una ciudad prioritaria para inversión en infraestructura de transporte es Santiago de Chile.
