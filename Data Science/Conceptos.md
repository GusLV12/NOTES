# Ciencia de Datos

</br>

## Conceptos

### Outliers (Valores Atípicos)

Los outliers son datos que están muy alejados de la mayoría de los otros puntos en un conjunto de datos. Pueden afectar la precisión de un modelo de regresión lineal, ya que tienen un impacto desproporcionado en la línea de mejor ajuste.

## Variables Continuas y discretas

### Variable Discreta

**Una variable discreta es aquella que puede tomar un número finito o contable de valores específicos. No puede tomar valores intermedios entre dos valores consecutivos y, en general, representa conteos o categorías.**

Ejemplos de variables discretas:

    Número de hijos en una familia (0, 1, 2, etc.).
    Número de estudiantes en una clase.
    Lanzamientos de un dado: los resultados posibles son 1, 2, 3, 4, 5, o 6.
    Cantidad de autos en un estacionamiento.
    Cantidad de productos vendidos en una tienda.

### Variables Continua

**Una variable continua es aquella que puede tomar cualquier valor dentro de un rango o intervalo. Puede tener infinitos valores dentro de un rango dado y puede incluir fracciones y decimales. En general, representa mediciones.**

Ejemplos de variables continuas:

    Peso de una persona en kilogramos (por ejemplo, 70.5 kg, 80.2 kg).
    Altura de una persona en metros (por ejemplo, 1.75 m, 1.82 m).
    Tiempo que tarda un auto en recorrer cierta distancia (por ejemplo, 5.3 segundos).
    Temperatura de una ciudad (puede ser cualquier valor, como 21.3°C, 15.8°C).
    Distancia recorrida por un atleta (por ejemplo, 10.5 km, 12.25 km).

# Modelos de Machine Learning

## Regresión Lineal

La **regresión lineal** es un método estadístico que se utiliza para modelar la relación entre una variable dependiente (o respuesta) y una o más variables independientes (o explicativas). La relación se modela como una línea recta, con la ecuación general:

$$
y = \beta_0 + \beta_1 x + \epsilon
$$

donde:

- \( y \): variable dependiente (lo que queremos predecir).
- \( x \): variable independiente (predictora).
- \( \beta_0 \): intercepto o término constante, el valor de \( y \) cuando \( x = 0 \).
- \( \beta_1 \): coeficiente de la pendiente, que representa el cambio en \( y \) por cada unidad de cambio en \( x \).
- \( \epsilon \): término de error, que representa las desviaciones de los datos con respecto al modelo lineal.

## Objetivo de la Regresión Lineal

El objetivo de la regresión lineal es encontrar los valores de \( \beta_0 \) y \( \beta_1 \) que minimicen el error entre los valores predichos por el modelo y los valores observados en los datos. Este error se mide comúnmente utilizando el **error cuadrático medio** (MSE), dado por:

$$
\text{MSE} = \frac{1}{n} \sum_{i=1}^n (y_i - \hat{y}_i)^2
$$

donde:

- \( y_i \): valor real de la variable dependiente en el \( i \)-ésimo punto de datos.
- \( \hat{y}_i \): valor predicho de la variable dependiente en el \( i \)-ésimo punto de datos.
- \( n \): número total de puntos de datos.

## Fórmulas para los Coeficientes

Los valores óptimos de \( \beta_0 \) y \( \beta_1 \) en una regresión lineal simple pueden calcularse mediante las siguientes fórmulas:

### Pendiente \( \beta_1 \)

$$
\beta_1 = \frac{\sum_{i=1}^n (x_i - \bar{x})(y_i - \bar{y})}{\sum_{i=1}^n (x_i - \bar{x})^2}
$$

### Intercepto \( \beta_0 \)

$$
\beta_0 = \bar{y} - \beta_1 \bar{x}
$$

donde:

- \( \bar{x} \): media de los valores de \( x \).
- \( \bar{y} \): media de los valores de \( y \).

## Interpretación de los Coeficientes

- **Intercepto** \( \beta_0 \): es el valor de \( y \) cuando \( x = 0 \). Representa el punto donde la línea de regresión corta el eje \( y \).
- **Pendiente** \( \beta_1 \): indica cuánto cambia \( y \) por cada unidad de cambio en \( x \). Si es positivo, \( y \) aumenta a medida que \( x \) aumenta, y si es negativo, \( y \) disminuye a medida que \( x \) aumenta.

## Predicción con el Modelo

Una vez que se han calculado \( \beta_0 \) y \( \beta_1 \), podemos hacer predicciones de \( y \) para cualquier valor dado de \( x \) utilizando la ecuación del modelo:

$$
\hat{y} = \beta_0 + \beta_1 x
$$

donde \( \hat{y} \) es el valor predicho de \( y \) para un valor dado de \( x \).

## Regresión Polinómica

**La regresión polinómica es un tipo de regresión en la que se ajusta un modelo polinómico a los datos. La regresión polinomica puede ajustar curvas más complejas, como polinomios de grado superior.**

Ventajas y desventajas:

- Ventajas

1. Modelo más flexible: Puede adaptarse a relaciones no lineales y capturar patrones más complejos en los datos.
2. Mayor poder predictivo: Puede proporcionar predicciones más precisas cuando la relación es mejor representada por una curva.

- Desventajas

1. Riesgo de Overfitting: con polinomios de grado alto, hay un riesgo de ajustar el modelo demasiado a los datos de entrenamiento y tener un redimiento deficiente con nuevos datos.
2. Menor interpretabilidad: A medida que aumenta el grado del polinomio, el modelo se vuelve más complejo y menos interpretable.
3. Elección del grado del polinomio: Determinar el grado adecuado del polinomio puede ser un desafío y puede requerir técnicas de validación del modelo.
