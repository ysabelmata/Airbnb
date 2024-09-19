## BI Airbnb

## Introducción 

En la era digital, y gracias a la constante recopilación de datos, la toma de decisiones informada se ha convertido en un pilar fundamental para el éxito empresarial. El Business Intelligence (BI) emerge entonces como una herramienta esencial, permitiendo a las organizaciones transformar grandes cantidades de datos en información significativa para tomar decisiones y accionar. El BI va más allá de la simple recopilación de datos; implica el análisis profundo y la interpretación de patrones, proporcionando una visión clara de las operaciones empresariales y permitiendo la identificación de oportunidades estratégicas, mejorar la eficiencia operativa y mantenerse ágiles en un entorno empresarial dinámico y competitivo.

## Caso

En un mundo donde la economía compartida y la hospitalidad convergen, plataformas como Airbnb han transformado la forma en que las personas buscan y ofrecen alojamientos. En este contexto, maximizar la eficiencia y la rentabilidad se ha vuelto esencial tanto para los anfitriones como para la propia plataforma. El presente proyecto se enfoca en la exploración y análisis de datos relacionados con la disponibilidad de habitaciones en Airbnb, utilizando herramientas y conceptos de Business Intelligence (BI) para desentrañar patrones, identificar oportunidades y mejorar la toma de decisiones estratégicas.
La diversidad de información generada por la interacción de anfitriones y huéspedes en la plataforma Airbnb crea un vasto conjunto de datos. Desde detalles sobre las propiedades, precios y ubicaciones, hasta la retroalimentación de los huéspedes, la riqueza de estos datos proporciona una oportunidad única para aplicar técnicas de BI. Al emplear estrategias de integración de datos y relaciones entre tablas, buscamos descubrir conocimientos profundos que permitan a los anfitriones y a Airbnb en sí, optimizar la disponibilidad de habitaciones, maximizar los ingresos y mejorar la experiencia del usuario.
Este análisis exploratorio utilizará técnicas avanzadas de BI para visualizar tendencias, identificar patrones y comprender los factores que influyen en la ocupación de los alojamientos. Desde la temporada alta hasta las preferencias regionales, se examinarán diversos aspectos para desentrañar información valiosa. 


## Temas

- :hammer_and_wrench: [Herramientas](#herramientas)
- </> [Lenguajes](#lenguajes)
- :gear: [Procesamiento y preparación de datos](#procesamiento-y-preparación-de-datos)
- :memo: [Ficha Técnica y Documentación](/Ficha_Tecnica/README.md)
- :bar_chart: [Visualización y Análisis de Datos](/Visualizacion/README.md)
- :heavy_check_mark: [Conclusiones y Recomendaciones](/Presentacion/README.md)


## Objetivo

Proporcionar una base sólida para la toma de decisiones informada, permitiendo a los interesados tomar medidas estratégicas para mejorar la eficiencia operativa y la rentabilidad en el dinámico ecosistema de Airbnb.

   
## Procesamiento y preparación de datos

1. Conectar/importar datos a herramientas:

* Se creó el proyecto airbnb y el conjunto de datos Dataset en BigQuery.

* Tablas importadas: 

    - Host: 37485 registros.
    - Reviews: 48875 registros.
    - Rooms: 48875 registros.

2. Identificar y manejar valores nulos.

    - host_name : 18 nulos.
    - last_review : 10039 nulos.
    - reviews_per_month : 1019 nulos.
    - availability_365 : 156 nulos.

3. Identificar y manejar valores duplicados:

* No se encontraron registros duplicados.

4. Identificar y manejar datos discrepantes en variables categóricas.

* Se creó la tabla hosts_limpia con 36881 registros , luego de quitar nulos y datos discrepantes.
* Se creó la tabla reviews_limpia con 38694 registros, luego de quitar nulos y datos discrepantes.
* Se creó la tabla rooms_limpia con 48710 registros, luego de quitar nulos y datos discrepantes. 

5. Comprobar y cambiar tipo de dato.

* Se cambió el host_id de la tabla hosts_limpia a número entero en power bi.
* Se cambió el id, host_id, price, y number_of_reviews a número entero y el campo last_review a fecha,  de la tabla hosts_limpia en power bi.
* Se cambió el id a número entero de la tabla rooms_limpia en power bi.

6. Relacionar tablas

Se relacionaron las tablas:
* host_limpia y reviews_limpia por el campo host_id.
* rooms_limpia y reviews_limpia por el campo id.

7. Crear nuevas variables (se utilizaron formulas DAX)

* Columna año en la tabla reviews.
* Columna review_id.
* Columnas: precio por habitacion, porcentaje de habitaciones disponibles, y total de huespedes por año.


Para ver el diseño de la Estructura de la Base de datos revisar: [Ficha Técnica y Documentación](/Ficha_Tecnica/FTBusinessIntelligence.pdf)

## Herramientas

* BigQuery
* Power Bi
* Google Docs
* Google Slide

## Lenguajes

* SQL




