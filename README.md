# Proyecto Final — Text Mining & Image Recognition

**Postgrado en Análisis y Predicción de Datos — Tercer Trimestre 2026**

## Integrantes

- **20011152 — Samuel Isaac Gómez Moreno**
- **25002775 — Luis Felipe Zárate de León**

---

# Problema 1 — Word Cloud

## Objetivo

Realizar un análisis de texto y generar nubes de palabras a partir del corpus proporcionado, identificando usuarios y términos con mayor frecuencia.

## Resultados principales

Top 3 usuarios mencionados:

1. **@mileycyrus — 4580 menciones**
2. **@tommcfly — 3904 menciones**
3. **@ddlovato — 3474 menciones**

## Archivos

- `Proyecto_Final_Problema1_WordCloud.ipynb`
- `corpus/` — corpus generados
- `wordclouds/` — WordCloud Top 10
- `resultados/` — frecuencias y tablas

---

# Problema 2 — Fruits and Vegetables Recognizer

## Objetivo

Construir y comparar tres arquitecturas de Redes Neuronales Convolucionales (CNN) para clasificar imágenes de frutas y vegetales.

Se trabajó con seis categorías:

**Frutas**
- Apple
- Banana
- Orange

**Vegetales**
- Carrot
- Potato
- Tomato

## Dataset

Se utilizó el **Fruits and Vegetables Dataset de Kaggle**, de Mukhriddin Mukhiddinov.

Para el experimento se seleccionaron **7,200 imágenes**, distribuidas de forma equilibrada:

- Apple: 1,200
- Banana: 1,200
- Orange: 1,200
- Carrot: 1,200
- Potato: 1,200
- Tomato: 1,200

División utilizada:

- **Entrenamiento:** 5,040 imágenes
- **Validación:** 1,080 imágenes
- **Prueba:** 1,080 imágenes

El dataset completo no se incluye en el repositorio debido a su tamaño. El Notebook lo descarga desde Kaggle durante su ejecución.

## Arquitecturas evaluadas

Se compararon tres modelos:

1. `CNN_1_Basica`
2. `CNN_2_Intermedia`
3. `CNN_3_Mejorada`

## Resultados

| Modelo | Test Loss | Test Accuracy |
|---|---:|---:|
| **CNN_1_Basica** | 0.344062 | **90.93%** |
| CNN_3_Mejorada | **0.276100** | 90.74% |
| CNN_2_Intermedia | 0.477419 | 84.63% |

De acuerdo con el criterio de **mayor Test Accuracy**, el modelo seleccionado fue:

**CNN_1_Basica — 90.93%**

La CNN 1 clasificó correctamente **982 de las 1,080 imágenes de prueba**.

La CNN 3 obtuvo una exactitud muy cercana (90.74%) y presentó el menor Test Loss (0.2761).

## Matriz de confusión

La evaluación de `CNN_1_Basica` mostró un desempeño equilibrado entre las seis categorías.

Las clases **orange, carrot y tomato** alcanzaron un recall de **92.78%**, mientras que **potato** presentó el menor recall, con **88.33%**.

## Conclusión

Los resultados muestran que una arquitectura más compleja no necesariamente obtiene una mayor exactitud.

Aunque `CNN_3_Mejorada` obtuvo el menor Test Loss, `CNN_1_Basica` consiguió la mayor exactitud sobre el conjunto de prueba.

Por esta razón, siguiendo el criterio definido para el proyecto, se seleccionó **CNN_1_Basica como modelo final**.

## Archivos del Problema 2

- `Proyecto_Final_Problema2_CNN_FINAL.ipynb` — Notebook final ejecutado
- `comparacion_modelos.csv` — comparación de las tres CNN

---

# Ejecución

## Problema 1

Abrir:

`Proyecto_Final_Problema1_WordCloud.ipynb`

y ejecutar las celdas en orden.

## Problema 2

Abrir:

`Proyecto_Final_Problema2_CNN_FINAL.ipynb`

Se recomienda utilizar **Google Colab con GPU T4**.

El Notebook realiza:

1. Instalación e importación de librerías.
2. Descarga del dataset.
3. Selección de las seis clases.
4. División de los datos.
5. Preparación de imágenes.
6. Construcción de tres arquitecturas CNN.
7. Entrenamiento.
8. Comparación de modelos.
9. Curvas de aprendizaje.
10. Evaluación sobre el conjunto de prueba.
11. Matriz de confusión y métricas.
12. Selección del modelo final.

---

# Tecnologías utilizadas

- Python
- TensorFlow / Keras
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- KaggleHub
- Google Colab
- GitHub
