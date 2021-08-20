# Laboratorio 1 - Clasificación

## Objetivos

 - Comprender el proceso asociado a la preparación de datos para una tarea de minería de datos de clasificación 
 - Utilizar una herramienta para el preprocesamiento, la limpieza y el perfilamiento de los datos
 - Analizar e identificar los hiperparametros adecuados para los modelos de clasificación.
 - Obtener conclusiones y analizar la matriz de confusión a partir de los modelos generados.
 - Comunicar los hallazgos encontrados a la organización y explicar por que tiene valor para el negocio.
 - Comparar los 3 algoritmos seleccionados y explicar cual recomiendan a la organización

## Herramientas
Durante este laboratorio trabajaremos con las siguientes herramientas:


 - Python
	 - Distribución sugerida: [Anaconda](https://www.continuum.io/downloads) 
		 - La versión de Anaconda es 4.4
		 - La versión usada es la de python 2.7, usar la de python 3 no debería requerir muchos cambios. 
	 - Paquetes:
	   	 - Jupyter Notebook
	   	 - Pandas
		 - scikit-learn

	   	 

## Enunciado 
SaludAndes es una entidad de salud colombiana especializada en los tratamientos para combatir la diabetes. En los ultimos años, SaludAlpes ha presentado distintas problematicas asociadas a los tiempos de atención de los pacientes causada por moras en el proceso de analisis de resultados clinicos para detectar la diabetes. SaludAlpes los ha contratado para agilizar y mejorar el proceso de analisis de resultados clinicos de tal manera que no se presenten moras en el proceso. Su labor como consultor BI es analizar y procesar los datos de tal manera que se pueda determinar si un paciente puede tener diabetes de una manera rapida y efectiva.

Con el fin de lograr el objetivo para el cual fue contratado, se le sugiere realizar los siguientes pasos:

1.	Descargar y entender los datos [HR-Employee-Attrition.csv](HR-Employee-Attrition.csv) utilizando el [diccionario de datos](Diccionario_HR_Employee_Attrition.pdf) .
2.	Realizar un perfilamiento de datos que le permita estudiar el detalle de estos, al igual que identificar el nivel de calidad de los datos y las tareas de transformación que requieren.
2.	Describir el pre-procesamiento que debe realizar para limpiar los datos y dejarlos listos para aplicar los algoritmos que le permitan llevar a cabo esta técnica analítica de clasificación.
3.	Implementar tres algoritmos diferentes: K nearest-neighbours, arboles de decisión y uno de libre elección que permita clasificar los conjuntos de datos de manera correcta. Justificar las decisiones más importantes asociadas al proceso, tales como los criterios utilizados para la selección de hiperparámetros.
4.	Analizar los resultados obtenidos y justificar la utilidad de estos modelos para SaludAlpes.
5.	Desarrollar una presentación donde exponga sus resultados y recomendaciones a SaludAlpes.
6.  Comparar los distintos algoritmos implementados y explicar cual recomendarían a SaludAlpes.

## Entregables 

 - Documento con todos los puntos que debío realizar en el laboratorio. Incluya adicionalmente, la justificación de los cambios realizados al archivo original (punto 2). Incluya en el documento, su reflexión sobre los criterios a utilizar para seleccionar la herramienta a utilizar para el pre-procesamiento.
 - Presentación con los resultados obtenidos (punto 5 de las tareas descritas previamente).
 - Workflow que contiene el proceso realizado si lo hizo en Knime o su equivalente en el programa en el que lo desarrolló.

## Documentación de scikit-learn de apoyo
- [scit-learn](https://scikit-learn.org/stable/supervised_learning.html#supervised-learning)

## Sugerencias

 - Nota 1: Como lo habrá notado, en los datos entregados hay atributos categoricos. Para poder realizar el proceso de clasificación hay que tratar estos valores categoricos.
 - Nota 2: Deberán analizar si los valores de cada columna corresponden a valores adecuados para el negocio, en caso de que sean anómalos deberán tratar dichos valores.
 - Nota 3: Utilizar los datos que sean utiles para determinar un posible diagnostico de diabetes.
 - Nota 4: Para el preprocesamiento de los datos se puede hacer uso de las herramientas del curso o de otras herramientas diferentes según el criterio propio. Acá se harán sugerencias sobre las posibilidades que podría desarrollar.
 

 

* En el caso de python, la librería pandas permite que el procesamiento de grandes conjuntos de datos sea sencilla, así que se sugiere revisar el uso de esta.



