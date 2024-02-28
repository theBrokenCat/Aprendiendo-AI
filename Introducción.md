1. Aprendizaje regular: Nuestro uso de algoritmos se basa en usar ciertas entradas, aplicarles una lógica (conociendo el algoritmo), y obtener un resultado.
2. Aprendizaje automático: A ciertas entradas se les aplica unos algoritmos que desconocemos para obtener el resultado

### Ejemplo
Para programar un programa en el que pase de grados Celsius a Fahrenheit se haría de la siguiente forma en los siguientes casos:

- Programación regular:
	def function (C):
		F = C * 1.8 + 32
		return F

- Aprendizaje automático:
	No conocemos la fórmula de conversión, tendremos que usar reglas de tres con varias entradas y varias salidas correspondientes. Celsius[-40, -10, 0, 8] Fahrenheit[-40, 14, 32, 46]

# Red neuronal
Las redes neuronales se separan en capas, con una o más neuronas. Tenemos siempre una *capa de entrada* y una *capa de salida* donde obtendremos el resultado calculado.
Las neuronas se conectan con conexiones. Cada conexión tiene un peso asignado, que representa la importancia entre conexión.
![[conexiones de neuronas.png]]
#convolucional

Cada neurona a excepción de la Capa de entrada tiene un *sesgo* que es un valor numérico
![[operaciones de neuronas.png]]
#lineal

## Inicio de una red neuronal
Al empezar, los valores del peso y del sesgo son completamente aleatorios, llevando a errores. Por ello, lo primero que necesitamos es una gran cantidad de valores de entrada y sus correspondientes salidas, para que la red neuronal aprenda **la relación** entre todos esos valores. Irá viendo si los resultados son muy distintos e irá ajustando los pesos de los *sesgos* y los *pesos*. 

Veamos el ejemplo de pasar de una unidad de grados a otra en el [[De Celsius a Fahrenheit]]
# Tipos de problemas
## Regresión
La salida del modelo o red neuronal es un número. Puede recibir gran cantidad de entradas pero acaba convergiendo en la salida como un número.
![[dibujo varias capas ejemplo 1.png]]
## Clasificación
La salida del modelo o red neuronal no es un número, nuestra red tendrá que decidir a qué categoría o #clase pertenece la entrada. Si tuviéramos 10 clases posibles, nuestra red neuronal tendrá que escoger una.
En estos problemas trabajaremos con imágenes, donde cada neurona de entrada corresponde a un píxel de la imagen. Definiremos varias neuronas de salida como varias clases.
Hay varios [[Tipos de Redes Neuronales]],  la que más se usa es la *red neuronal convolucional*, que es muy usada para la clasificación de imágenes. 

Nosotros trabajaremos con la *red neuronal densa*, para acabar inventando una *red neuronal convolucional*.

Una vez que una neurona suma su *sesgo* y va a dar su resultado, pasaremos el dato por una [[Función de activación]]. 

Una red no deja de ser lineal hasta que añadimos una capa oculta con una función de activación no lineal.

Ejemplos de clasificación:
- [[Gatos o Perros con Tensorflow]]
- [[Gatos o Perros con archivos Locales]]
- [[clasificador_ropa]]