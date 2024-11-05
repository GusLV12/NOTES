# Ciencia de Datos

</br>

## Probabilidad con Ciencia de Datos

### Media

La media es el promedio de un conjunto de datos y representa el valor central de una distribución. Se calcula sumando todos los valores y dividiéndolos por el número total de elementos.

**Fórmula**:  
$$
\text{Media} = \frac{1}{N} \sum_{i=1}^{N} X_i
$$  
donde \( N \) es el número de datos y \( X_i \) representa cada valor.

### Mediana

La mediana es el valor central de un conjunto de datos ordenados. Si el número de elementos es impar, la mediana es el valor que se encuentra en el centro. Si el número de elementos es par, la mediana es el promedio de los dos valores centrales.

### Moda

La moda es el valor que aparece con mayor frecuencia en un conjunto de datos. Un conjunto de datos puede tener:

    - Una sola moda (unimodal): Si un valor es el más frecuente.
    - Dos modas (bimodal): Si hay dos valores que son igualmente frecuentes.
    - Sin moda: Si no hay un valor que se repita más de una vez.

### Correlación

La correlación mide la fuerza y la dirección de la relación lineal entre dos variables. Se expresa como un valor entre -1 y 1, donde:

    1: Correlación positiva perfecta.
    -1: Correlación negativa perfecta.
    0: No hay correlación.

### Covarianza

La covarianza mide cómo dos variables cambian juntas. Una covarianza positiva indica que las variables tienden a aumentar juntas, mientras que una negativa indica que una variable tiende a disminuir cuando la otra aumenta. A diferencia de la correlación, la covarianza no se escala entre -1 y 1.

### Coeficiente de Determinación (R²)

El R² es una medida estadística que indica qué proporción de la varianza en la variable dependiente es explicada por las variables independientes en un modelo de regresión lineal. Un valor de R2R2 más cercano a 1 indica un mejor ajuste del modelo.

### Dispersión

La dispersión mide cuánto varían los datos respecto a la media, indicando la extensión o variabilidad de los valores. Algunas medidas comunes son la varianza y el rango intercuartílico.

(No tiene una fórmula específica, ya que es un concepto general que agrupa varias medidas).

### Varianza

La varianza es el promedio de los cuadrados de las desviaciones respecto a la media. Cuanto mayor es la varianza, mayor es la dispersión de los datos.

**Fórmula**:  
$$
\text{Varianza} = \frac{1}{N} \sum_{i=1}^{N} (X_i - \text{Media})^2
$$  

### Desviación Estándar

La desviación estándar es la raíz cuadrada de la varianza y mide cuánto se alejan en promedio los datos respecto a la media. Es útil para entender la dispersión en unidades originales de los datos.

**Fórmula**:  
$$
\text{Desviación Estándar} = \sqrt{\frac{1}{N} \sum_{i=1}^{N} (X_i - \text{Media})^2}
$$

## Evento de Probabilidad

Un evento de probabilidad es un conjunto de posibles resultados de un experimento aleatorio. Especifica las circunstancias bajo las cuales ocurren ciertos resultados, como obtener "cara" al lanzar una moneda. Los eventos se representan con variables aleatorias, que asignan valores numéricos a los posibles resultados de un experimento.

## Variables Aleatorias

Una variable aleatoria es una función que asigna un valor numérico a cada resultado de un experimento. Las variables aleatorias permiten modelar y cuantificar la ocurrencia de eventos, facilitando el cálculo de probabilidades en distintos escenarios.

## Ensayo de Bernoulli

Un ensayo de Bernoulli es un experimento aleatorio con solo dos resultados posibles: éxito o fracaso (generalmente representados como 1 y 0, respectivamente). Cada ensayo tiene una probabilidad fija de éxito \( p \), y los resultados son independientes de otros ensayos. Este tipo de ensayo es la base de la distribución binomial.
