 # Curso Práctico de Regresión Lineal con Python

- [Curso Práctico de Regresión Lineal con Python](#curso-práctico-de-regresión-lineal-con-python)
  - [Modulo 1 Bienvenida al curso](#modulo-1-bienvenida-al-curso)
    - [Clase 1 Introduccion](#clase-1-introduccion)
    - [Clase 2 Regresión Lineal y Machine Learning](#clase-2-regresión-lineal-y-machine-learning)
    - [Clase 3 Explicacion Matematica de la Regresion Lineal](#clase-3-explicacion-matematica-de-la-regresion-lineal)
  - [Modulo 3 Entendiendo el algoritmo de regresión lineal](#modulo-3-entendiendo-el-algoritmo-de-regresión-lineal)
    - [Clase 4 Método de Minimos Cuadrados: Ecuacion](#clase-4-método-de-minimos-cuadrados-ecuacion)
    - [Clase 5 Metodo de Mínimos Cuadrados: Despejando la Ecuacion](#clase-5-metodo-de-mínimos-cuadrados-despejando-la-ecuacion)
    - [Clase 6 Generando Predicciones en Papel](#clase-6-generando-predicciones-en-papel)

## Modulo 1 Bienvenida al curso

### Clase 1 Introduccion

Introduccion por el profesor

Lo mas recomendable antes de iniciar es tomar los cursos de estadística, algebra lineal  e introduccion a machine learning.

### Clase 2 Regresión Lineal y Machine Learning

![ML](/home/vanhelsingx3/Documentos/GitHub/Machine-learning-course/linear regression/img/ML.jpg)

Proceso ML supervisado

1.- Tener observaciones etiquetadas de los datos que vamos a tener
2.-  Set de  entrenamiento y set de validación
3.- Modelo Machine Learner (modelo RL)
4.- Evaluación estadística del modelo.

Una vez se entrene el modelo  podremos predecir datos futuros o pasados fuera del dataset.

Usos de la regresión:

- Estimar crecimiento de la probación
- Predicción del clima
- Predicción del mercado

Uso de Clasificación:

- Retención de clientes
- Diagnósticos
- Clasificación de imágenes

![clasificacion vs lineal](/home/vanhelsingx3/Documentos/GitHub/Machine-learning-course/linear regression/img/clasificacion vs lineal.jpg)

### Clase 3 Explicacion Matematica de la Regresion Lineal

Tenemos dos ejemplos de basicamente el primero es para una regresion lineal con una **pendiente positiva** (los valores de "Y" incrementan al incrementar los valores de "X") y el segundo con una **pendiente Negativa** (los valores de "Y" decrementan al incrementar los valores de "X").

Para ambos casos haremos uso dela ecuacion de regresion lineal 

$Y = b_0 + b_1X$

donde

$Y = $ Variable dependiente (depende de X)
$b_0$ = Constante de proporcionalidad 
$b_1$ = Pendiente de la recta
$X$ = Variable independiente

**Ejemplo 1 Pendiente Positiva**.

![pendiente positiva](/home/vanhelsingx3/Documentos/GitHub/Machine-learning-course/linear regression/img/pendiente positiva.jpg)

**Ejemplo 2 Pendiente Negativa**.

![pendiente negativa](/home/vanhelsingx3/Documentos/GitHub/Machine-learning-course/linear regression/img/pendiente negativa.jpg)

## Modulo 3 Entendiendo el algoritmo de regresión lineal

### Clase 4 Método de Minimos Cuadrados: Ecuacion

A partir de la siguiente tribulación graficamos los puntos en la tabla. Aplicaremos la formula de minimos cuadrados para cada uno de los componentes de $b_1$

<img src="/home/vanhelsingx3/Documentos/GitHub/Machine-learning-course/linear regression/img/ puntos en la tabla.jpg" alt=" puntos en la tabla"  />

Solución.

![solucion](/home/vanhelsingx3/Documentos/GitHub/Machine-learning-course/linear regression/img/solucion.jpg)

El método de mínimos de cuadrados es una función que busca minimizar los residuos en las observaciones.
Por ejemplo, si tengo una serie de mediciones de distancia que corresponden a un mismo elemento, (Es preciso indicar que toda observación presenta un residuo o también llamado error). Podría determinar el valor mas probable con el método de mínimos cuadrados, y la función mejora si es que se le agrega pesos a las observaciones.

### Clase 5 Metodo de Mínimos Cuadrados: Despejando la Ecuacion

Dados los datos de la tabla calculamos entonces $b_1$

![despeje](/home/vanhelsingx3/Documentos/GitHub/Machine-learning-course/linear regression/img/despeje.jpg)

Usando los valores promedio $\bar{x}$ y $\bar{y}$ graficandolos en un plano.

 $\bar{y} = 4.2$  nos permite calcular la constante de proporcionalidad $b0$ de la siguiente manera.

![proporcionalidad](/home/vanhelsingx3/Documentos/GitHub/Machine-learning-course/linear regression/img/proporcionalidad.jpg)

### Clase 6 Generando Predicciones en Papel

A partir e la ecuacion $Y = b_0 + b_1X$ calcularemos valores fuera del set de datos original, calculamos los valores para $x = 6$

![calculamos los valores](/home/vanhelsingx3/Documentos/GitHub/Machine-learning-course/linear regression/img/calculamos los valores.jpg)

Calculamos, y graficamos el punto para obtener la linea de regresion.

![graficamos](/home/vanhelsingx3/Documentos/GitHub/Machine-learning-course/linear regression/img/graficamos.jpg)