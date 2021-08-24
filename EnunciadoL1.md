# Laboratorio 1 - Clasificación

## Objetivos

 - Comprender el proceso asociado a la preparación de datos para una tarea de minería de datos de clasificación 
 - Utilizar una herramienta para el preprocesamiento, la limpieza y el perfilamiento de los datos
 - Analizar e identificar los hiperparametros adecuados para los modelos de clasificación.
 - Obtener conclusiones y analizar la matriz de confusión a partir de los modelos generados.
 - Comunicar los hallazgos encontrados a la organización y explicar por qué tiene valor para el negocio.
 - Comparar los 3 algoritmos seleccionados y explicar cuál recomiendan a la organización.

## Herramientas
Durante este laboratorio trabajaremos con las siguientes herramientas:


 - Python
	 - Distribución sugerida: [Anaconda](https://www.continuum.io/downloads) 
		 - La versión de Anaconda es 4.4
		 - La versión usada es la de python 2.7, usar la de python 3 no debería requerir muchos cambios. 
	 - Paquetes:
	   	 - Jupyter Notebook
	   	 - Pandas
		 - Scikit-learn

	   	 

## Enunciado 
SaludAlpes es una entidad de salud colombiana que se especializa atender pacientes diagnosticados con diabetes. Entre las actividades principales de SaludAlpes destaca el análisis de resultados de laboratorio para la detección de diabetes. Dicho análisis es manual, por lo que cada medico especialista debe analizar cada uno de los resultados de laboratorio para diagnosticar la diabetes, por lo que en los últimos años, SaludAlpes ha presentado distintas problemáticas asociadas a los tiempos de atención de los pacientes causada por moras en el proceso de análisis de resultados clínicos para detectar la diabetes. SaludAlpes los ha contratado para agilizar y mejorar el proceso de análisis de resultados clínicos de tal manera que no se presenten moras en el proceso. Su labor como consultor BI es analizar y procesar los datos de tal manera que se pueda determinar si un paciente puede tener diabetes de una manera rapida y efectiva.

Con el fin de lograr el objetivo para el cual fue contratado, se le sugiere realizar los siguientes pasos:

1.	Descargar y entender los datos [SaludAlpes_diagnosticos_dataset.csv](SaludAlpes_diagnosticos_dataset.csv) utilizando el [diccionario de datos](SaludAlpes_diagnosticos_dataset_dictionary.pdf).
2.	Realizar un perfilamiento de datos que le permita estudiar el detalle de estos, al igual que identificar el nivel de calidad de los datos y las tareas de transformación que se requieren. Adicionalmente es obligatorio presentar tableros de control mostrando las estadisticas del dataset, tales como cantidad de columnas, cantidad de datos, valores nulos, promedio de cada variable entre otros posibles datos que puedan proveer a SaludAlpes.

### Ejemplo de posible tablero de control
![img](Dashboard-ej.jpg)


2.	Describir el preprocesamiento que debe realizar para limpiar los datos y dejarlos listos para aplicar los algoritmos que le permitan llevar a cabo esta técnica analítica de clasificación.
3.	Implementar tres algoritmos diferentes: K nearest-neighbours, arboles de decisión y uno de libre elección que permita clasificar los conjuntos de datos de manera correcta. Justificar las decisiones más importantes asociadas al proceso, tales como los criterios utilizados para la selección de hiperparámetros y las modificaciones a los datos para cada algoritmo.
4.	Analizar los resultados obtenidos y justificar la utilidad de estos modelos para SaludAlpes.
5.  Comparar los distintos algoritmos implementados y explicar cuál recomendarían a SaludAlpes.
6.	Desarrollar una presentación donde exponga sus resultados y recomendaciones a SaludAlpes.

## Entregables 

 - Documento con todos los puntos que debe realizar en el laboratorio. Incluya adicionalmente, la justificación de los cambios realizados al dataset original (punto 2). Incluya en el documento, su reflexión sobre los criterios a utilizar para seleccionar la herramienta a utilizar para el preprocesamiento.
 - Presentación con los resultados obtenidos (punto 5 de las tareas descritas previamente).
 - Notebook que contiene el proceso realizado.
 - Archivo que contiene el tablero de control creado.

## Documentación de scikit-learn de apoyo
- [scit-learn](https://scikit-learn.org/stable/supervised_learning.html#supervised-learning)

## Sugerencias

 - Nota 1: Como lo habrá notado, en los datos entregados hay atributos categóricos. Para poder realizar el proceso de clasificación hay que tratar estos valores categóricos.
 - Nota 2: Deberán analizar si los valores de cada columna corresponden a valores adecuados para el negocio, en caso de que sean anómalos deberán tratar dichos valores.
 - Nota 3: Utilizar los datos que sean útiles para determinar un posible diagnóstico de diabetes.
 - Nota 4: Para el preprocesamiento de los datos y los tableros de control se puede hacer uso de las herramientas del curso o de otras herramientas diferentes según el criterio propio.
 - Nota 5: Revisar el diccionario y verificar que los datos correspondan con niveles posibles de los examenes clínicos.
 - Nota 6: En el caso de python, la librería pandas permite que el procesamiento de grandes conjuntos de datos sea sencilla, así que se sugiere revisar el uso de esta.



 ## IMPORTANTE

 - Cada integrante del grupo debe estar encargado de la implementación de un algoritmo distinto, sin embargo, todos los integrantes del grupo deben tener la capacidad de explicar lo realizado por los demás compañeros y determinar la mejor solución para SaludAlpes. (Aclaración: El análisis de resultados y su justificación debe ser realizado en grupo)

 - Es importante aclarar que las notas dentro de un mismo grupo de laboratorio pueden variar ya que en los puntos 2 y 3 cada integrante está encargado de la implementación de un algoritmo distinto, por lo que dichos puntos se evaluan individualmente y no grupalmente.
 

 


