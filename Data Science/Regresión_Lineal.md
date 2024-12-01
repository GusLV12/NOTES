# Ejercicios Regresion Lineal y Regresion Polinomial

## Ejemplo de Uso

Supongamos que queremos predecir el precio de una casa (variable dependiente) en función de su tamaño en metros cuadrados (variable independiente). Con base en un conjunto de datos históricos, podemos calcular los coeficientes \( \beta_0 \) y \( \beta_1 \), y luego usar el modelo para predecir el precio de una casa de tamaño específico.

```py
from sklearn.linear_model import LinearRegression
from sklearn.preprocessing import StandardScaler
import numpy as np

# Datos de ejemplo: tamaño de la casa (en metros cuadrados) y precios (en miles de dólares)
X = np.array([[50], [80], [100], [150], [200]])  # Tamaño en metros cuadrados
y = np.array([150, 200, 250, 300, 350])  # Precio en miles de dólares

# Escalar los datos
scaler_X = StandardScaler()
scaler_y = StandardScaler()

X_scaled = scaler_X.fit_transform(X)
y_scaled = scaler_y.fit_transform(y.reshape(-1, 1)).flatten()

# Crear el modelo y ajustarlo a los datos escalados
modelo = LinearRegression()
modelo.fit(X_scaled, y_scaled)

# Predicción para una casa de 120 metros cuadrados (escalada y luego desescalada)
X_test = np.array([[120]])
X_test_scaled = scaler_X.transform(X_test)
y_pred_scaled = modelo.predict(X_test_scaled)
y_pred = scaler_y.inverse_transform(y_pred_scaled.reshape(-1, 1))

print(f"El precio estimado para una casa de 120 m² es: ${y_pred[0][0]:.2f} mil dólares")

```

### Ejemplo 2

```py

from sklearn.linear_model import LinearRegression
from sklearn.model_selection import train_test_split
from sklearn.metrics import mean_squared_error, r2_score
import pandas as pd
import matplotlib.pyplot as plt
     
data = pd.read_csv('/content/sample_data/Advertising.csv')

X = data['TV'].values.reshape(-1,1)
y = data['Sales'].values

# Dividimos el conjunto entre el conjunto de entrenamiento y testing
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
     

# Entrenamiento del modelo lineal con los datos
lin_reg = LinearRegression()
lin_reg.fit(X_train, y_train)

# Predicción de los valores utilizando el modelo
y_pred = lin_reg.predict(X_test)
print('Predicciones: {}, valores reales: {}'.format(y_pred[:4], y_test[:4]))
# Predicciones: [14.71794394 16.2115484  20.74819743  7.66403631], valores reales: [16.9 22.4 21.4  7.3]


r_squared = lin_reg.score(X_test, y_test) # R^2

rmse = mean_squared_error(y_test, y_pred, squared=False) #RMSE

print(r_squared, rmse)   
# 0.6766954295627076 3.194472431998898

r2_score(y_test, y_pred) # R^2
# 0.6766954295627076

# Gráfico de los datos de test contra el modelo
plt.plot(X_test, y_test, 'ro')
plt.plot(X_test, y_pred.reshape(-1,1))
plt.show()

# Crear una función para automatizar funcion de regresión lineal
def modelos_simple(independiente):
  X = data[independiente].values.reshape(-1,1)
  y = data['Sales'].values
  X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
  lin_reg = LinearRegression()
  lin_reg.fit(X_train, y_train)
  y_pred = lin_reg.predict(X_test)

  print('Predicciones: {}, valores reales: {}'.format(y_pred[:4], y_test[:4]))

  r_squared = lin_reg.score(X_test, y_test) # R^2
  rmse = mean_squared_error(y_test, y_pred, squared=False) #RMSE
  print('R2', r_squared, "RMSE", rmse)

  print('R2', r2_score(y_test, y_pred))

  plt.plot(X_test, y_test, 'ro')
  plt.plot(X_test, y_pred.reshape(-1,1))
  plt.show()
```

## Regresion Polinómica

```py

import pandas as pd
import matplotlib.pyplot as plt
     
# Creación del conjunto de datos
pos = [x for x in range(1,11)]
post = ["Pasante de Desarrollo",
 "Desarrollador Junior",
 "Desarrollador Intermedio",
 "Desarrollador Senior",
 "Líder de Proyecto",
 "Gerente de Proyecto",
 "Arquitecto de Software",
 "Director de Desarrollo",
 "Director de Tecnología",
 "Director Ejecutivo (CEO)"]
salary = [1200.0, 2500.0, 4000.0, 4800.0, 6500.0, 9000.0, 12820.0, 15000.0, 25000.0, 50000.0]

# Creación del conjunto
data = {
    'position': post,
    'years': pos,
    'salary': salary
}

data = pd.DataFrame(data)
data.head()

# Relación entre variables
plt.scatter(data['years'], data['salary'])
plt.show()

# Extracción del avariable dependiente e independiente
X = data.iloc[:, 1].values.reshape(-1,1)
y = data.iloc[:, -1].values

# Crearemos un modelo de regresión lineal
from sklearn.linear_model import LinearRegression
regression = LinearRegression()
regression.fit(X, y)

plt.scatter(data['years'], data['salary'])
plt.plot(X, regression.predict(X), color = "black")
plt.show()

regression.predict([[2]])   
# array([-1305.33333333])

# Regresion Polinímica
from sklearn.preprocessing import PolynomialFeatures
poly = PolynomialFeatures(degree = 4)
X_poly = poly.fit_transform(X)
X_poly
     
# array([[1.000e+00, 1.000e+00, 1.000e+00, 1.000e+00, 1.000e+00],
#       [1.000e+00, 2.000e+00, 4.000e+00, 8.000e+00, 1.600e+01],
#       [1.000e+00, 3.000e+00, 9.000e+00, 2.700e+01, 8.100e+01],
#       [1.000e+00, 4.000e+00, 1.600e+01, 6.400e+01, 2.560e+02],
#       [1.000e+00, 5.000e+00, 2.500e+01, 1.250e+02, 6.250e+02],
#       [1.000e+00, 6.000e+00, 3.600e+01, 2.160e+02, 1.296e+03],
#        [1.000e+00, 7.000e+00, 4.900e+01, 3.430e+02, 2.401e+03],
#       [1.000e+00, 8.000e+00, 6.400e+01, 5.120e+02, 4.096e+03],
#       [1.000e+00, 9.000e+00, 8.100e+01, 7.290e+02, 6.561e+03],
#       [1.000e+00, 1.000e+01, 1.000e+02, 1.000e+03, 1.000e+04]])

# Para la creación del modelo polinómico seguimos utilizando la clase de regresión lineal.
regression_2 = LinearRegression()
regression_2.fit(X_poly, y)

plt.scatter(X, y)
plt.plot(X, regression_2.predict(X_poly), color = "black")
plt.show()

predict = poly.fit_transform([[2]])
regression_2.predict(predict)
# array([1398.34498834])

# R-Squared
from sklearn.metrics import r2_score

y_pred = regression_2.predict(X_poly)
r_squared = r2_score(y, y_pred)
r_squared
# 0.9933186366907111
```
