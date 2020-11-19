# TEAM :tw-1f3b1: - :tw-1f1f3::tw-1f1e6::tw-1f1ee::tw-1f1fb::tw-1f1ea: :tw-1f1e7::tw-1f1e6::tw-1f1fe::tw-1f1ea::tw-1f1f8:

<div align="center">

**TECNOLÓGICO NACIONAL DE MÉXIO**

INSTITUTO TECNOLÓGICO DE TIJUANA

SUBDIRECCIÓN ACADÉMICA
 
DEPARTAMENTO DE SISTEMAS Y COMPUTACIÓN
 
SEMESTRE SEPTIEMBRE 2020 – ENERO 2021

INGENIERÍA EN SISTEMAS COMPUTACIONALES

 
 [![](https://upload.wikimedia.org/wikipedia/commons/2/2e/ITT.jpg)](https://upload.wikimedia.org/wikipedia/commons/2/2e/ITT.jpg)

**PROFESOR**

JOSÉ CHRISTIAN ROMERO HERNÁNDEZ

**CLASE**

DATOS MASIVOS
BDD-1704 SC9A, L - V 18:00 - 19:00 (91L4/0308)


**NAIVE BAYES**


**EQUIPO 8:**

PACHECO RAMÍREZ HUGO ANDRÉS	16210790

RAMIREZ GONZALEZ MARCO ANTONIO 15212341

ROBLES ACOSTA JOSE FRANCISCO 16212368

SANDOVAL CASTRO SEBASTIÁN	16212076


Tijuana, Baja California, al 07 de diciembre de 2020.
 
</div>


[========]


# DESARROLLO

## :tw-1f4a5: Introducción

_El presente documento está diseñado especialmente para mostrar el desarrollo del tema **Naive Bayes **, abarcando desde conceptos generales y ecuaciones necesarias hasta una implementación práctica en una situación real y su aplicación mediante codigo **scala**. Finalmente se incluyen algunas ventajas y desventajas al momento de implementar el algoritmo, así como una conclusión general basada en el análisis resultante a lo largo del desarrollo del documento._

## :tw-1f4d5: Definiciones

:tw-1f4cb: _**Algoritmo:** es un conjunto de instrucciones o reglas definidas y no-ambiguas, ordenadas y finitas que permite, típicamente, solucionar un problema, realizar un cómputo, procesar datos y llevar a cabo otras tareas o actividades._ [[1]](https://es.wikipedia.org/wiki/Algoritmo)

:tw-1f47e: _**Machine Learning:** es una disciplina científica del ámbito de la Inteligencia Artificial que crea sistemas que aprenden automáticamente. Aprender en este contexto quiere decir identificar patrones complejos en millones de datos. La máquina que realmente aprende es un algoritmo que revisa los datos y es capaz de predecir comportamientos futuros. Automáticamente, también en este contexto, implica que estos sistemas se mejoran de forma autónoma con el tiempo, sin intervención humana._ [[2]](https://cleverdata.io/que-es-machine-learning-big-data/)

## :tw-1f4d6: Teoría

### :tw-2753: - ¿Qué es el algoritmo Naive Bayes?

_**Naive Bayes**_ es una clase especial de algoritmo de clasificación de _**Machine Learning**_. Se encuentra basado en una técnica de clasificación estadística llamada _**teorema de Bayes**_.

### :tw-2753: - ¿Por qué el algoritmo Naive Bayes se llama de esa forma?

Primeramente, _**Naive Bayes**_ se traduce literalmente como _**Bayes Ingenuo**_, lo que provoca cuestionarse: ¿por qué ingenuo?

En este algoritmo se asume que las variables predictoras son independientes entre sí, lo que quiere decir que la presencia de una cierta característica en un conjunto de datos no está en absoluto relacionada con la presencia de cualquier otra característica.

En otras palabras, este tipo de algoritmo trata a sus variables de forma separada, ignorando por completo toda regla de relación que pueda llegar a existir como, por ejemplo, cierto orden lógico, cierta estructura, alguna característica en especial, etc.

### :tw-2753: - ¿Para qué se utiliza el algoritmo Naive Bayes?

El algoritmo _**Naive Bayes**_ se utiliza para construir modelos con comportamientos muy buenos. Se hace de una forma más fácil debido a la simplicidad del mismo.

El algoritmo consigue hacer esto ya que proporciona una forma de calcular la probabilidad _**posterior**_ de que ocurra un cierto evento _**A**_, dadas algunas probabilidades de eventos _**anteriores**_.

## :tw-1f4cb: Algoritmo

### :tw-1f523: Ecuación

![ecuacion.png](https://raw.github.com/sebastiansandovalcastro/NaiveBayes/master/imagenes/ecuacion.png)

### :tw-1f4dc: Pasos de uso

Se recomienda utilizar los siguientes cuatro pasos al momento de implementar el algoritmo _**Naive Bayes**_ en problemas de clasificación:

1. Convertir el conjunto de datos en una tabla de frecuencias.

2. Crear una tabla de probabilidad calculando las correspondientes a que ocurran los diversos eventos.

3. Utilizar la ecuación _**Naive Bayes**_ para calcular la probabilidad posterior de cada clase.

4. Seleccionar la clase con la _**probabilidad posterior más alta**_ como resultado de la predicción.

## :tw-1f4dd: Ejemplo teórico

_Presentaremos los conceptos principales del algoritmo Naive Bayes estudiando el siguiente ejemplo:_

###  :tw-1f46b: Alicia, Bruno y la chaqueta roja (ejemplo 1)

Consideremos el caso de dos personas que trabajan en la misma oficina: Alicia y Bruno.
Sabemos que:

- Alicia viene a la oficina 3 días a la semana.
- Bruno viene a la oficina 1 día a la semana.

_(Esta sería nuestra información **anterior**)._

Estamos en la oficina y vemos pasar delante de nosotros a alguien muy rápido, tan rápido que no sabemos si es Alicia o Bruno.

Dada la información que tenemos hasta ahora y asumiendo que solo trabajan 4 días a la semana, las probabilidades de que la persona vista sea Alicia o Bruno, son:

- P(Alicia) = 3/4 = 0.75
- P(Bruno) = 1/4 = 0.25

Cuando vimos a la persona pasar, vimos que él o ella llevaba una chaqueta roja. También sabemos lo siguiente:

- Alicia viste de rojo 2 veces a la semana.
- Bruno viste de rojo 3 veces a la semana.

Así que, para cada semana de trabajo, que tiene cinco días, podemos inferir lo siguiente:

- La probabilidad de que Alicia vista de rojo es → P(Rojo|Alicia) = 2/5 = 0.4
- La probabilidad de que Bruno vista de rojo → P(Rojo|Bruno) = 3/5 = 0.6

Entonces, con esta información, ¿a quién vimos pasar? (en forma de probabilidad)

_(Esta nueva probabilidad será la información **posterior**.)_

Inicialmente conocíamos las probabilidades P(Alicia) y P(Bruno), y después inferíamos las probabilidades de P(Rojo|Alicia) y P(Rojo|Bruno), de forma que las probabilidades reales son:

![probabilidades1.png](https://raw.github.com/sebastiansandovalcastro/NaiveBayes/master/imagenes/probabilidades1.png)

Donde, formalmente, el gráfico previo se vería de la siguiente manera:

![probabilidades2.png](https://raw.github.com/sebastiansandovalcastro/NaiveBayes/master/imagenes/probabilidades2.png)

### :tw-1f4e8: Correo normal y correo spam (ejemplo 2)

Hacer click [aquí](https://youtu.be/O2L2Uv9pdDA?t=67) para ver el ejemplo desarrollado en un vídeo de YouTube.

## :tw-1f4bb: Ejemplo práctico

_Presentaremos los conceptos principales del algoritmo Naive Bayes estudiando el siguiente ejemplo:_

### :tw-1f522: Sample libsvm data

	//Importaciones necesarias.
	import org.apache.spark.ml.classification.NaiveBayes
	import org.apache.spark.ml.evaluation.MulticlassClassificationEvaluator

![1.png](https://raw.github.com/sebastiansandovalcastro/NaiveBayes/master/imagenes/1.png)

	// Cargar los datos guardados en formato LIBSVM como un DataFrame.
	val data = spark.read.format("libsvm").load("C:/Users/Sebas/Desktop/sample_libsvm_data.txt")
	data.show(2)

![2.png](https://raw.github.com/sebastiansandovalcastro/NaiveBayes/master/imagenes/2.png)

	//Separar los datos en sets de entrenamiento y de prueba (30% reservado para pruebas)
	val Array(trainingData, testData) = data.randomSplit(Array(0.7, 0.3), seed = 1234L)

![3.png](https://raw.github.com/sebastiansandovalcastro/NaiveBayes/master/imagenes/3.png)

	// Entrenar un modelo Naive Bayes.
	val model = new NaiveBayes().fit(trainingData)

![4.png](https://raw.github.com/sebastiansandovalcastro/NaiveBayes/master/imagenes/4.png)

	// Seleccionar las filas de ejemplo a mostrar.
	val predictions = model.transform(testData)
	predictions.show()

![5.png](https://raw.github.com/sebastiansandovalcastro/NaiveBayes/master/imagenes/5.png)

	// Selecciona (prediccion, etiqueta de cierto) y calcular errores de prueba
	val evaluator = new MulticlassClassificationEvaluator().setLabelCol("label").setPredictionCol("prediction").setMetricName("accuracy")

	val accuracy = evaluator.evaluate(predictions)

	println(s"Test set accuracy = $accuracy")

![6.png](https://raw.github.com/sebastiansandovalcastro/NaiveBayes/master/imagenes/6.png)

Hacer click [aquí](https://raw.github.com/sebastiansandovalcastro/NaiveBayes/master/scala/Exposicion.scala) para una mejor visualización del código scala.

## :tw-1f3ad: Ventajas y Desventajas

### :tw-1f44d: Ventajas

- Es una forma fácil y rápida de predecir clases para problemas de clasificación binarios y multiclase.

- En casos donde existe presunción de independencia, el algoritmo se comporta mejor que otros modelos de clasificación, incluso con menos datos de entrenamiento.

- Cada distribución puede ser estimada independientemente como si tuviera una sola dimensión, ayudando con problemas derivados de la dimensionalidad y mejorando el rendimiento.

### :tw-1f44e: Desventajas

- Conocidos constantemente como pobres estimadores, por lo que no se suelen tomar muy en serio las probabilidades obtenidas.

- La presunción de independencia _**Naive**_ muy probablemente no reflejará cómo son los datos en el mundo real.

- Cuando el conjunto de datos de prueba tiene una característica que no ha sido observada en el conjunto de entrenamiento, el modelo le asignará una probabilidad de cero y será inútil realizar predicciones.

## :tw-1f52c: Conclusiones

Como conclusiones podemos decir que, una de las mayores ventajas que _**Naive Bayes**_ tiene sobre otros algoritmos de clasificación, es que tiene una gran capacidad para manejar un gran número de variantes gracias al uso independiente que estas mismas reciben. El algoritmo se comporta bien incluso ante la presencia de características irrelevantes y no es relativamente afectado por ellas.

Se puede decir que la magia de este algoritmo se encuentra en su simplicidad, ya que _**Naive Bayes**_ funciona bien desde el principio y ajustar sus parámetros es raramente necesario, además de que su modelo de entrenamiento y procesos de predicción es muy rápido teniendo en cuenta la cantidad de datos que puede manejar.

Por último, a pesar de que las probabilidades obtenidas no se suelen tomar bastante en serio debido a la ignorancia que presenta el algoritmo sobre las características que puedan tener las variantes utilizadas, es una vía muy útil cuando se busca obtener probabilidades de forma rápida y sencilla.

## :tw-1f4da: Fuentes de información

- [[1]](https://es.wikipedia.org/wiki/Algoritmo) **Algoritmo** - Wikipedia
- [[2]](https://cleverdata.io/que-es-machine-learning-big-data/) **¿Qué es Machine Learning?** - Cleverdata (Andrés González)
- [[3]](https://www.youtube.com/watch?v=O2L2Uv9pdDA) **Naive Bayes, Clearly Explained!!!** - YouTube ([StatQuest with Josh Starmer](https://www.youtube.com/channel/UCtYLUTtgS3k1Fg4y5tAhLbw))
- [[4]](https://medium.com/datos-y-ciencia/algoritmos-naive-bayes-fudamentos-e-implementaci%C3%B3n-4bcb24b307f) **Algoritmos Naive Bayes: Fundamentos e Implementación** - Medium ([Victor Roman](https://medium.com/@rromanss23))

##  :tw-270f: Autores

- **PACHECO RAMÍREZ HUGO ANDRÉS** - _16210790_ - [PachecoHugo](https://github.com/PachecoHugo)
- **RAMIREZ GONZALEZ MARCO ANTONIO** - _15212341_ - [MarcoAnRamirez](https://github.com/MarcoAnRamirez)
- **ROBLES ACOSTA JOSE FRANCISCO** - _16212368_ - [JFranciscoRobles](https://github.com/JFranciscoRobles)
- **SANDOVAL CASTRO SEBASTIÁN** - _16212076_ - [sebastiansandovalcastro](https://github.com/sebastiansandovalcastro)

_[Lista de contribuyentes](https://github.com/sebastiansandovalcastro/NaiveBayes/contributors) que participaron en la elaboración de este documento._