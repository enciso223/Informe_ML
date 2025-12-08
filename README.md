# Predicción de Aprobación de Curso de Matemáticas - Machine Learning

## 📋 Información General

Este repositorio contiene dos proyectos de Machine Learning desarrollados para predecir si un estudiante aprobará un curso de matemáticas. El análisis se realiza utilizando un dataset de 1044 estudiantes con 17 atributos que incluyen información demográfica, educativa y de hábitos de estudio.

**Universidad del Valle**  
**Escuela de Ingeniería de Sistemas y Computación**  
**Curso:** Inteligencia Artificial  
**Autores:** 
- Juan Sebastian Sierra - 202343656
- Jhoan Sebastian Fernandez - 2222772

---

## 🎯 Objetivo del Proyecto

El proyecto tiene como objetivo desarrollar y comparar dos técnicas de Machine Learning para predecir la aprobación de estudiantes en un curso de matemáticas:

1. **Redes Neuronales Artificiales (MLP)** - Cuaderno 1
2. **Árboles de Decisión** - Cuaderno 2

La variable objetivo es `approved`, que toma el valor 1 cuando el estudiante aprueba el curso y 0 en caso contrario.

---

## 📊 Dataset

### Descripción del Dataset
El dataset `student_performance.csv` contiene información de 1044 estudiantes con los siguientes atributos:

#### Variables Categóricas:
- **sex**: Sexo del estudiante (F/M)
- **famsize**: Tamaño de familia (LE3: ≤3 personas, GT3: >3 personas)
- **Pstatus**: Estado de convivencia de los padres (T: juntos, A: separados)
- **Mjob**: Trabajo de la madre (teacher, health, services, at_home, other)
- **Fjob**: Trabajo del padre (teacher, health, services, at_home, other)
- **internet**: Acceso a internet en casa (yes/no)
- **romantic**: En relación romántica (yes/no)

#### Variables Numéricas:
- **age**: Edad (15-22 años)
- **Medu**: Nivel educativo de la madre (0-4)
- **Fedu**: Nivel educativo del padre (0-4)
- **traveltime**: Tiempo de traslado a la institución (1-4)
- **studytime**: Tiempo de estudio semanal (1-4)
- **failures**: Número de veces que ha reprobado el curso (0-4)
- **goout**: Frecuencia de salidas con amigos (1-5)
- **Walc**: Consumo de alcohol en fin de semana (1-5)
- **health**: Estado de salud actual (1-5)

#### Variable Objetivo:
- **approved**: Indica si aprobó el curso (0: No, 1: Sí)

---

## 📓 Notebooks Desarrollados

### 📘 Cuaderno 1: Redes Neuronales (MLP)

**Archivo:** `Cuaderno_1.ipynb`

#### Contenido:
1. **Carga y exploración de datos**: Lectura del archivo CSV y análisis exploratorio
2. **Preprocesamiento**:
   - División de datos: 80% entrenamiento, 20% prueba
   - Normalización de variables numéricas con StandardScaler
   - Codificación de variables categóricas con OneHotEncoder
3. **Construcción de modelos**: 5 redes neuronales con diferentes configuraciones:
   - Variación de capas ocultas y neuronas por capa
   - Diferentes solvers (adam, sgd, lbfgs)
   - Funciones de activación variadas (relu, tanh, logistic)
4. **Evaluación**: Tabla comparativa de accuracy para los 5 modelos
5. **Optimización**: Identificación del mejor modelo y experimentación con hiperparámetro adicional (alpha)
6. **Métricas finales**: Accuracy, Sensibilidad, Especificidad y MAE

#### Modelos Implementados:
Los modelos varían en arquitectura, desde redes simples hasta configuraciones más complejas, permitiendo comparar el rendimiento y encontrar la configuración óptima.

---

### 📗 Cuaderno 2: Árboles de Decisión

**Archivo:** `Cuaderno_2.ipynb`

#### Contenido:
1. **Carga y exploración de datos**: Lectura del archivo CSV y análisis inicial
2. **Preprocesamiento**:
   - División de datos: 80% entrenamiento, 20% prueba
   - Normalización de variables numéricas con StandardScaler
   - Codificación de variables categóricas con LabelEncoder
3. **Árboles con criterio Gini**:
   - 5 árboles con max_depth de 2 a 10 (incrementos de 2)
   - Tabla comparativa de resultados
4. **Árboles con criterio Entropy**:
   - 5 árboles con max_depth de 2 a 10 (incrementos de 2)
   - Tabla comparativa de resultados
5. **Identificación del mejor modelo**: Comparación entre ambos criterios
6. **Experimentación adicional**: Prueba del hiperparámetro min_samples_split
7. **Métricas y visualización**:
   - Accuracy, Sensibilidad, Especificidad
   - Matriz de confusión
   - Gráfico comparativo de accuracy por criterio

#### Análisis Implementado:
El notebook incluye análisis detallado sobre cómo el hiperparámetro min_samples_split afecta el rendimiento del modelo, ayudando a prevenir el sobreajuste.

---

## 🛠️ Requisitos e Instalación

### Dependencias Principales:
```python
scikit-learn
pandas
numpy
matplotlib
```

### Instalación:

```bash
# Clonar el repositorio
git clone https://github.com/tu-usuario/prediccion-estudiantes-ml.git
cd prediccion-estudiantes-ml

# Instalar dependencias
pip install scikit-learn pandas numpy matplotlib
```

---

## 🚀 Cómo Utilizar

### Opción 1: Jupyter Notebook (Local)

1. Asegúrate de tener Jupyter instalado:
```bash
pip install jupyter
```

2. Coloca el archivo `student_performance.csv` en el mismo directorio que los notebooks

3. Inicia Jupyter Notebook:
```bash
jupyter notebook
```

4. Abre el notebook deseado (`Cuaderno_1.ipynb` o `Cuaderno_2.ipynb`)

5. Ejecuta las celdas secuencialmente desde el principio

### Opción 2: Google Colab

1. Sube el archivo `student_performance.csv` a tu Google Drive o cárgalo directamente en Colab

2. Abre el notebook en Google Colab

3. Si el archivo CSV está en Google Drive, monta tu Drive:
```python
from google.colab import drive
drive.mount('/content/drive')
```

4. Ajusta la ruta del archivo CSV según corresponda

5. Ejecuta todas las celdas

### Estructura del Proyecto

```
├── Cuaderno_1.ipynb          # Notebook de Redes Neuronales
├── Cuaderno_2.ipynb          # Notebook de Árboles de Decisión
├── student_performance.csv   # Dataset (debe agregarse)
├── Informe_Machine_learning.pdf  # Documento con especificaciones
└── README.md                 # Este archivo
```

---

## 📈 Resultados Esperados

### Cuaderno 1 - Redes Neuronales:
- Tabla con accuracy de 5 modelos diferentes
- Identificación del modelo con mejor rendimiento
- Análisis del impacto del hiperparámetro alpha
- Métricas completas: Accuracy, Sensibilidad, Especificidad, MAE

### Cuaderno 2 - Árboles de Decisión:
- Dos tablas comparativas (criterio Gini y Entropy)
- Identificación del mejor modelo según max_depth y criterion
- Análisis del hiperparámetro min_samples_split
- Matriz de confusión
- Visualización gráfica comparativa de accuracies

---

## 📊 Métricas de Evaluación

Ambos notebooks calculan las siguientes métricas:

- **Accuracy**: Proporción de predicciones correctas
- **Sensibilidad (Recall)**: Proporción de casos positivos correctamente identificados
- **Especificidad**: Proporción de casos negativos correctamente identificados
- **MAE** (solo Cuaderno 1): Error absoluto medio

---

## 🔍 Aspectos Técnicos Importantes

### Preprocesamiento de Datos:

**Cuaderno 1:**
- Normalización: StandardScaler para variables numéricas
- Codificación: OneHotEncoder para variables categóricas

**Cuaderno 2:**
- Normalización: StandardScaler para variables numéricas
- Codificación: LabelEncoder para variables categóricas

### División de Datos:
Ambos notebooks utilizan:
- 80% para entrenamiento
- 20% para pruebas
- random_state=42 para reproducibilidad

---

## 📝 Notas Adicionales

- Los notebooks están diseñados para ejecutarse de forma secuencial
- Se recomienda ejecutar todas las celdas en orden
- Los modelos utilizan semillas aleatorias (random_state) para garantizar reproducibilidad
- Cada notebook incluye análisis y comentarios explicativos en celdas de markdown

---

## 📖 Referencias

- [Documentación scikit-learn - MLPClassifier](https://scikit-learn.org/stable/modules/generated/sklearn.neural_network.MLPClassifier.html)
- [Documentación scikit-learn - DecisionTreeClassifier](https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeClassifier.html)
- [Documentación Pandas](https://pandas.pydata.org/docs/)

---

## 📄 Licencia

Este proyecto es de uso académico para el curso de Inteligencia Artificial de la Universidad del Valle.

---

## 🤝 Contribuciones

Este es un proyecto académico. Para cualquier consulta o sugerencia, contactar a los autores a través de la Universidad del Valle.

---

**Última actualización:** Diciembre 2024
