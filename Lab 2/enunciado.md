# Laboratorio 3 - Clustering

## Objetivos

- Comprender el proceso asociado con la preparación de datos para una tarea de minería de datos de similitud relacionada con la técnica de segmentación - clustering (agrupación) 

- Aplicar un algoritmo de segmentación como k-means para generar segmentos 

- Obtener conclusiones a partir de los segmentos identificados que sean útiles para una organización. 


## Herramientas

- Librerías principales de Python para procesamiento y visualización de datos como: pandas, sklearn, seaborn, numpy y matplotlib.  
    Se recomienda usar la última distribución disponible de Anaconda Individual Edition, pueden encontrar el instalador en este [enlace](https://www.anaconda.com/products/individual). 

- Ambiente de desarrollo: Jupyter notebook en distribución de Anaconda.  

## Enunciado

### Descripción de negocio

BancAlpes es una entidad bancaria que está realizando una campaña de fidelización para aumentar la retención de usuarios y de esa manera ofrecer mejore productos, servicios y recomendaciones a sus clientes más fieles. Por esta razón, ha recurrido a usted como consultor para que le entregue al equipo de marketing información que pueda ayudarlos a tomar mejores decisiones respecto a las campañas de fidelización próximo trimestre.  

La información que le ha proporcionado el equipo la puede encontrar aquí [link al csv de la información](credit_card_data.csv). Estos datos contienen el resumen de los clientes del último año, en particular, su valor desde el punto de vista de interacciones con la entidad bancaria.  Pueden acceder al diccionario de datos a traves del siguiente link: [diccionario](diccionario.pdf).



### Instrucciones 

La empresa quiere seguir apropiando la metodología CRISP-DM, en específico en su nueva versión ASUM-DM, para el desarrollo de estas iniciativas en analítica de datos, por lo cual le sugiere realizar los siguientes pasos: 

1. Perfilamiento de los datos: en esta etapa es importante saber cuántos datos se tienen (filas y columnas), el tipo de datos de las columnas, cual es la integridad de los datos, cuál es su distribución (discreta o continua). Para esto, es útil aplicar estadística descriptiva sobre los datos, señalando sus principales estadísticos: media, varianza, desviación estándar, etc., para el caso de las columnas numéricas Tenga en cuenta que para su trabajo será mucho más sencillo interpretar una gráfica que una tabla y acompañarla de una síntesis de lo observado.

2. Limpieza de datos: es el procedimiento llevado a cabo para transformar los valores nulos (missing values) o valores atípicos (outliers), también es importante tener en cuenta que para la mayoría de modelos llevar acabo pasos de normalización o estandarización es útil y necesario.  
 
3. Modelamiento: en este paso se lleva a cabo la elección del modelo con el que queremos cumplir nuestra tarea y su refinamiento, en este caso usando el algoritmo de K-Means como base y deberán, realizar y compararlo con otros dos algoritmos como clustering jerárquico, DBScan, HDBScan, Gaussian Mixture. No obstante, en ambientes profesionales la elección del algoritmo, hará parte de su tarea de consultoría. Adicionalmente, se espera que sepan interpretar las funciones implementadas (Jupyter) y, la elección de los hiper-parámetros del modelo y justificar su elección. La sugerencia es explorar la generación de cluster con distintos atributos que puedan llevar a mejores valores de coeficiente de silueta.  

4. Validación: En modelos de aprendizaje no supervisado la validación de los modelos es un reto importante que deben asumir los consultores. En este caso, con el uso de clustering y en particular del algoritmo de K-Means, dado que se trata de un algoritmo particional, la calidad desde el punto de vista cuantitativo, relacionada con los datos utilizados y con el valor de “k” seleccionado, puede validarse utilizando el coeficiente de silueta y ser ajustado siguiendo guías como el método del codo. Información adicional, puede encontrarla en este [enlace](https://towardsdatascience.com/k-means-clustering-algorithm-applications-evaluation-methods-and-drawbacks-aa03e644b48a), para complementar su interpretación.  Una vez realizada la validación cuantitativa, se tiene una segunda parte de la validación que corresponde a la descripción de los resultados obtenidos (clústers y conclusiones del proceso), para la comprensión por parte de la empresa. Esta parte la denominados validación cualitativa. 

5. Tableros de control: El estudiante debe proponer una visualización de los resultados obtenidos  en un tablero de control, de tal manera que el cliente tenga la capacidad de entender los resultados obtenidos en su labor de consultoría.




## Entregables

* Informe del laboratorio con el desarrollo y la evidencia de cada una de las etapas, es importante que incluyan imágenes de gráficas y su interpretación, el informe se espera que no supere las 6 páginas. Además, una presentación corta para el negocio con los resultados, las conclusiones y algunas recomendaciones. 

Nota: Recuerde que la presentación debe estar orientada a los clientes, por lo que se recomienda evitar el uso de términos muy técnicos y utilizar más la interpretación de los resultados con un lenguaje con el que el negocio esté familiarizado. 

* Realice su análisis siguiendo los pasos estipulados previamente en la sección de instrucciones, interprete los resultados obtenidos explícitamente en el informe del laboratorio, así mismo registre sus conclusiones. Al final de su informe, haga una comparación de los algoritmos implementados para identificar sus ventajas y desventajas.  

Algunas preguntas que pueden guiar su desarrollo son: 

1. ¿Qué criterios son importantes para la selección del modelo? 

2. ¿Cómo medir el nivel de desempeñándose del modelo construido? ¿Cómo saber que el modelo construido tiene un buen desempeño?  

3. ¿Qué desventajas tiene este modelo si se quisiera aplicar realizar analítica de datos a nivel profesional? 

4. ¿Cómo varía la calidad del modelo obtenido si aplico diferentes algoritmos? 

5. ¿Qué pasa en la ejecución del algortimo de k-means si se incluyen variables categóricas nominales, Qué tratamiento se les debe aplicar? 

## Sugerencias

Los siguientes links pueden serle de utilidad para la implementación en Python. 

* [Ejemplo de K-Means usando Sklearn](https://jakevdp.github.io/PythonDataScienceHandbook/05.11-k-means.html)

* [Artículo de Towards Data Science: K-means with Sklearn](https://towardsdatascience.com/k-means-clustering-with-scikit-learn-6b47a369a83c)

* [Artículo de Towards Data Science: Introducción al análisis de datos con Python](https://towardsdatascience.com/tips-and-tricks-for-fast-data-analysis-in-python-f108ad32fa90) 


Adicionalmente se incluye este [archivo Jupyter Notebook](K-Means_with_python.ipynb) con un ejemplo de análisis de K-Means para datos de prueba, el cual puede utilizar como base. Recuerde que las etapas de limpieza y perfilamiento de datos deben incluirse en su análisis y son fundamentales para garantizar la calidad de su resultado.  