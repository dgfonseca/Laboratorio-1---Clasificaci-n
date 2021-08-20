# Laboratorio 1 - Reglas de asociación

## Objetivos

 - Comprender el proceso asociado a la preparación de datos para una tarea de minería de datos de agrupamiento por afinidad relacionada con la técnica de reglas de asociación
 - Utilizar una herramienta para el preprocesamiento de datos y la generación de reglas de asociación
 - Obtener conclusiones a partir de las reglas de asociación identificadas.

## Herramientas
Durante este laboratorio trabajaremos con las siguientes herramientas:

 - [Knime](https://www.knime.com/) con los nodos de Association Rule Learner 
 - [OpenRefine](http://openrefine.org/) - Opcional
 - Python
	 - Distribución sugerida: [Anaconda](https://www.continuum.io/downloads) 
		 - La versión de Anaconda es 4.4
		 - La versión usada es la de python 2.7, usar la de python 3 no debería requerir muchos cambios. 
	 - Paquetes:
	   	 - Jupyter Notebook
	   	 - Pandas
	   	 

## Enunciado 
Una de las tareas clave de los Departamentos de Recursos Humanos de las empresas es determinar qué factores mantienen a los empleados en sus puestos de trabajo y cuáles impulsan a otros a irse. En algunos casos estas decisiones están determinadas por condiciones laborales. Sin embargo, la deserción de empleados también se puede presentar debido a razones más de índole personal. Por ejemplo, el retiro puede obedecer a una actualización de conocimientos (estudios) que abre otras oportunidades para el trabajador, a razones familiares que impliquen mudarse lejos del lugar de trabajo o a imperativos de salud. Es decir, la disminución de una plantilla de empleados no obedece necesariamente a problemas con su empleador, sino que puede responder a factores relacionados con las condiciones y desarrollos de vida de cada uno. 

Para las empresas sería de gran valor identificar con suficiente antelación los empleados que podrían considerar el abandono de sus puestos de trabajo y los factores relacionados con estas decisiones. Con este objetivo en mente, Recursos Humanos Alpes ha recopilado un conjunto de datos sobre los empleados que están trabajando actualmente dentro de la empresa y los que han renunciado, caracterizados por un conjunto de variables socioeconómicas. En la primera etapa de este proyecto ha decidido contratarlo a Usted para que, apoyado en la minería de datos, identifique los patrones que caracterizan tanto a los empleados que abandonan como a los que permanecen en sus puestos de trabajo.

Con el fin de lograr el objetivo para el cual fue contratado, se le sugiere realizar los siguientes pasos:

1.	Descargar y entender los datos [HR-Employee-Attrition.csv](HR-Employee-Attrition.csv) utilizando el [diccionario de datos](Diccionario_HR_Employee_Attrition.pdf) .
2.	Realizar un perfilamiento de datos que le permita estudiar el detalle de estos, al igual que identificar el nivel de calidad de los datos y las tareas de transformación que requieren.
2.	Describir el pre-procesamiento que debe realizar para limpiar los datos y dejarlos listos para aplicar los algoritmos que le permitan llevar a cabo esta técnica analítica de reglas de asociación.
3.	Diseñar un flujo de trabajo que permita obtener conocimiento en forma de reglas de asociación de los patrones identificados en los datos compartidos. Justificar las decisiones más importantes asociadas a la generación de las reglas de asociación, tales como los criterios utilizados para la selección de parámetros.
4.	Analizar los resultados obtenidos y justificar la utilidad de estas reglas para AlpesSec.
5.	Desarrollar una presentación donde exponga sus resultados y recomendaciones a AlpesSec.

## Entregables 

 - Documento con todos los puntos que debío realizar en el laboratorio. Incluya adicionalmente, la justificación de los cambios realizados al archivo original (punto 2). Incluya en el documento, su reflexión sobre los criterios a utilizar para seleccionar la herramienta a utilizar para el pre-procesamiento.
 - Presentación con los resultados obtenidos (punto 5 de las tareas descritas previamente).
 - Workflow que contiene el proceso realizado si lo hizo en Knime o su equivalente en el programa en el que lo desarrolló.

## Nodos de Knime de apoyo
- [Column Expressions](https://hub.knime.com/knime/extensions/org.knime.features.expressions/latest/org.knime.expressions.base.node.formulas.FormulasNodeFactory)
- ScatterPlot

## Sugerencias

 - Nota 1: Como lo habrá notado, en los datos entregados hay atributos numéricos. Para obtener las reglas de asociación hay que transformar estos valores numéricos continuos a percentiles o rangos. En el caso de los rangos, hay que decidir los rangos más adecuados para representar cada columna y así manejar valores categóricos.
 - Nota 2: Para hacer uso del nodo “Association Rule Learner”, debe haber una columna de entrada, con forma de “bitVector” o de colección. En este caso, se sugiere utilizar el formato de colección.  Si desea, puede utilizar un nodo “Association Rule Learner (Borgelt)”, para el cual debe determinar el tipo de dato que recibe dicho nodo.
 - Nota 3: Recuerde ajustar los parámetros de confianza y soporte de las reglas.
 - Nota 4: Para el preprocesamiento de los datos se puede hacer uso de las herramientas del curso o de otras herramientas diferentes según el criterio propio. Acá se harán sugerencias sobre las posibilidades que podría desarrollar.
* En primer lugar, para transformar las columnas con knime puede recorrer todas las columnas de una tabla haciendo uso de los siguientes nodos. Se sugiere incluirlos en un metanodo para recorrer toda la tabla y no detallar cada iteración. El funcionamiento básico consiste en un nodo de inicio del ciclo, una serie de nodos intermedios que procesan cada columna, y un nodo de finalización. Al estar conectado a los nodos de ciclo, los demás nodos tienen acceso a las variables de flujo currentIteration y currentColumnName, que serán de utilidad para procesar cada columna al permitir manipular el valor de las variables presentes en cada nodo. 
![KNIME- Recorridos - opc1](img/CiclosL2.png) 
Ejemplo:
![KNIME- Recorridos Configuración del Nodo - opc1](img/NumberToStringL2.png) 

 
* En segundo lugar, puede transformar las columnas a rangos con un único nodo “Numeric binner”, asignando rangos que pueda justificar a cada una de las columnas de la tabla. Este nodo transformará los datos al rango correspondiente según lo que se haya definido.
* En tercer lugar, puede hacer uso de otros lenguajes de programación como R o Python (u otros). Estos dos son conocidos por las herramientas que ofrecen para procesar datos y su facilidad para realizar cálculos estadísticos que pueden ser útiles para discretizar datos. En el caso de python, la librería pandas permite que el procesamiento de grandes conjuntos de datos sea sencilla, así que se sugiere revisar el uso de esta.



- A continuación presentamos posibles workflow en KNIME para generar reglas de asociación. 

![KNIME- Reglas de asociación - opc1](img/Reglas.PNG)
![KNIME- Reglas de asociación - opc2](img/ReglasDeAsociacion2.PNG)

- Esta es la rúbrica que se usará para calificar el laboratorio

![Rúbrica L1](img/RubricaL1.PNG)


