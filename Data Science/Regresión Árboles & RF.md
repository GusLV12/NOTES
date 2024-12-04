# Regresión Árboles & Bosques aleatorios

## Árboles de Decisión para Regresión

**Un árbol de decisión es un modelo basado en una estructura jerárquica, donde:**

1. Nodo Raíz: Representa el conjunto completo de datos.
2. Nodos Internos: Son divisiones del conjunto de datos basadas en reglas de decisión que minimizan un criterio de error, como la suma de errores cuadráticos (MSE).
3. Hojas: Contienen el valor promedio (o mediana) de las observaciones de la región a la que pertenece.

Ventajas:

- Fácil de interpretar.
- Maneja características categóricas y numéricas.
- Resistente a valores atípicos en cierto grado.

Limitaciones:

- Propenso al sobreajuste (si el árbol es demasiado profundo).
- Sensible a cambios en los datos (alta varianza).

## Bosques Aleatorios para Regresión

**Un bosque aleatorio es un conjunto de múltiples árboles de decisión entrenados en diferentes subconjuntos del dataset y con diferentes características. Su predicción final se calcula como el promedio de las predicciones de los árboles individuales.
Principales Características:**

    - Bootstrap Aggregating (Bagging):
        Cada árbol se entrena con un subconjunto aleatorio de datos (con reemplazo).
    - Selección aleatoria de características:
        Durante la división en cada nodo, se evalúa solo un subconjunto aleatorio de características, lo que reduce la correlación entre los árboles.
    - Promediado:
        Reduce la varianza al combinar las predicciones de múltiples árboles.

Ventajas:

    - Excelente rendimiento en problemas complejos.
    - Resistente al sobreajuste, ya que combina múltiples modelos.
    - Maneja datos faltantes y relaciones no lineales.

Limitaciones:

    - Menos interpretable que un solo árbol.
    - Requiere más recursos computacionales.

| Característica        | Árbol de Decisión                  | Bosques Aleatorios             |
|-----------------------|-------------------------------------|---------------------------------|
| **Interpretabilidad** | Alta                               | Media                          |
| **Precisión**         | Menor                              | Mayor                          |
| **Varianza**          | Alta (sensibles a cambios)         | Baja (promedio de árboles)     |
| **Riesgo de sobreajuste** | Alto                              | Bajo                           |
