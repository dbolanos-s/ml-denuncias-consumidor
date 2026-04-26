# 📋 Análisis y Clasificación de Denuncias de Defensa del Consumidor

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-orange?logo=scikit-learn)
![Pandas](https://img.shields.io/badge/Pandas-Data-green?logo=pandas)
![Status](https://img.shields.io/badge/Status-Completado-success)

## 📌 Descripción
Este proyecto realiza un análisis de **33,052 denuncias reales** de consumidores registradas en 2019 y 2020. El objetivo es **predecir el motivo de una denuncia** basándose en variables como el rubro de la empresa, el mes y la comuna, utilizando algoritmos de aprendizaje supervisado.

##  Objetivo
Anticipar problemas frecuentes antes de que escalen, permitiendo una gestión proactiva mediante la clasificación automática de quejas basada en datos históricos.

##  Herramientas Utilizadas
| Herramienta | Uso |
|-------------|-----|
| **Python** | Lenguaje de programación base |
| **Pandas / NumPy** | Limpieza, manipulación y análisis de datos |
| **Matplotlib / Seaborn** | Visualización de distribuciones y correlaciones |
| **Scikit-learn** | Implementación de modelos de Machine Learning y evaluación |

##  Desarrollo Técnico

### 1. Preprocesamiento de Datos
Para preparar el dataset para el modelo, se aplicaron las siguientes técnicas:
- **Detección de Nulos:** Identificación y manejo de datos faltantes en variables críticas.
- **Label Encoding:** Se utilizó `LabelEncoder` de Scikit-learn para transformar las variables categóricas (**Rubro, Mes, Comuna, Motivo**) en valores numéricos, permitiendo el procesamiento por el algoritmo.

### 2. Entrenamiento del Modelo
Se implementó un modelo de **Bosques Aleatorios (Random Forest Classifier)**, seleccionado por su robustez en problemas de clasificación multiclase. El dataset se dividió en:
- **80%** para entrenamiento.
- **20%** para pruebas (Testing).

##  Resultados y Accuracy
Tras el entrenamiento y la validación, el modelo obtuvo los siguientes resultados:

- **Accuracy Score:** `0.8524` (85.24%)
- **Análisis de Error:** El modelo muestra una alta precisión al predecir motivos relacionados con rubros de servicios básicos y telecomunicaciones.

```python
# Métrica obtenida en el entrenamiento
print(f"Accuracy: {model.score(X_test, y_test)}")
# Output: 0.8524368476781122
