# MIARFID-RNA-2019-20
## RNA Denis Yurii 


### Ejercicio 1 
La clave para resolver el problema mnist fue el aumentación de los datos. Usamos mucho de eso. Utilizamos shift, share, zoom y rotación con grandes argumentos. También una clave para una solución fue un bajo número de batch, por lo que para época tenemos más iteraciones. Y mayor número de iteraciones. Dividimos el programa en dos partes para ver todos los resultados. Todo eso se guarda en el modelo "ggg" y "hhh" en total alrededor de 300 épocas con un tamaño de batch 100, el resultado es 0.9929.

Entonces comenzamos a experimentar. Usamos un tamaño de convolución de 2x2 y obtuvimos un resultado de 0.9453 en 50 épocas y batch75. Con tanh. Relu dio un resultado mucho mejor 0.9903 en menos épocas y más batch. 
Otra topología con convolución 3x3 3x3 5x5 dio el mismo resultado. 0.9942. También utilizamos la normalización y dropout y nuestra propia función de tasa de aprendizaje. Pero los resultados se obtuvieron incluso antes de su uso. 45 épocas. 
Experimentamos con una topología más y nos detuvimos. 0,9858

* [GitHub](https://github.com/LokiAndere/MIARFID-RNA-2019-20/blob/master/Copy_of_MNIST.ipynb) - problema de MNIST


### Ejercicio 2 
Primero usamos el código del maestro y logramos buenos resultados. Pero queríamos practicar nosotros mismos. Y se realizaremos muchos experimentos sobre mnist más simple para utilizar la mejor topología de convolución en el segundo ejercicio. Y utilizamos los mejores resultados de la primera parte (por lo que no esperamos mucho para ver cifar largo - sabíamos qué usar de mnist): aumentación, función de tasa de aprendizaje y topología con paso (3x3 -> 5x5 que no se considera grande, 9x9 o 11x11 es mediano)

0.9104 con 150 épocas y batch 50

Usamos normalización y centración que están construidos en keras. Debe mencionarse que debe hacerse esto a todos los datos de entrada.

Luego comenzamos a experimentar con la topología. Construimos VGG9 improvisado. 0.9024 pero una gran cantidad de variables. Así que tratamos de construirlo deepwise. El resultado fue bajo pero posible. En este momento dejamos de experimentar. 

* [GitHub](https://github.com/LokiAndere/MIARFID-RNA-2019-20/blob/master/cifar.ipynb) - problema de CIFAR


### Proyecto 
Hemos construido una GAN para la generación de las caras.

Lo hacemos utilizando el conocimiento de los dos primeros ejercicios. Primero generamos nuestro propio conjunto de datos. De 50 fotos hacemos 4321 y 2450 fotos con más o menos aumentación.

* [GitHub](https://github.com/LokiAndere/MIARFID-RNA-2019-20/blob/master/genface.ipynb) - generatión de los datos para entrenar

Luego entrenamos una GAN con diferentes topologías y conjuntos de datos. Y puedes ver los resultados. Utilizamos datos y modelos simplificados para un rápido rendimiento de los experimentos. Y vemos qué enfoque da mejores resultados para usar en futuro. El enfoque que usamos en mnist. Experimentamos con datos más simples para resolver problemas más serios más rápido.

* [GitHub](https://github.com/LokiAndere/MIARFID-RNA-2019-20/blob/master/cifar.ipynb) - generatión de las caras de GAN
