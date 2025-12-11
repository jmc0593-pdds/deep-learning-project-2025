# Deep Learning Project 2025

## Descripción

Este proyecto implementa tres modelos de redes neuronales profundas (MLP, CNN y RNN) para resolver distintos problemas de predicción y clasificación utilizando tres datasets reales. El objetivo es explorar diferentes arquitecturas y técnicas de aprendizaje profundo, analizar sus resultados y aprender sobre el proceso de desarrollo de modelos en machine learning.

**Estudiante:** Jorge Mario Cardona Oliva

## Datasets Utilizados

1. **Adult Income Dataset (`adult.csv`)**
   - Consiste en información de que una persona gana más de 50K al año basado en datos demográficos.
   - Columnas: edad, educación, ocupación, horas trabajadas, país, etc.

2. **Facial Expression Dataset (Carpetas de imágenes por sentimiento)**
   - Clasifica imágenes de rostros humanos en cinco emociones: Angry, Fear, Happy, Sad, Surprise.
   - Imágenes en baja resolución (48x48 a 1000x1000 px aproximadamente).

3. **Seattle Weather Dataset (`seattle-weather.csv`)**
   - Información relacionada al clima  en Seattle usando datos históricos diarios del 2012 al 2015.
   - Columnas: precipitación, temperatura máxima/mínima, viento, fecha, clima.

---

## Modelos Implementados

### 1. MLP (Multilayer Perceptron)
- **Problema:** Clasificación binaria de ingresos (>50K).
- **Preprocesamiento:** Limpieza de datos, normalización de variables numéricas, one-hot encoding de variables categóricas.
- **Arquitectura:** Capas densas con Dropout y activación ReLU/Sigmoid.
- **Resultados:**  
  - Accuracy: ~84%
  - Loss final: ~0.35%

### 2. CNN (Convolutional Neural Network)
- **Problema:** Clasificación de emociones en imágenes de rostros.
- **Preprocesamiento:** Limpieza de imágenes corruptas, redimensionamiento, normalización.
- **Arquitectura:** Capas convolucionales, MaxPooling, Dropout, Flatten, Dense con Softmax.
- **Resultados:**  
  - Accuracy: ~97%
  - Loss final: ~13%

### 3. RNN (Recurrent Neural Network con LSTM)
- **Problema:** Predicción de la categoría de clima en Seattle.
- **Preprocesamiento:** Extracción y normalización de fecha, escalado de variables numéricas, codificación de etiquetas.
- **Arquitectura:** Varias capas LSTM con Dropout y capa densa final.
- **Resultados:**  
  - Accuracy: ~0.08%
  - Loss final: ~100%

---

## Instrucciones de instalación y ejecución

1. **Instalar dependencias**
   ```bash
   pip install -r requirements.txt
   ```

2. **Ejecutar cada notebook**
   - Abre los archivos `MLP/MLP.ipynb`, `CNN/CNN.ipynb` y `RNN/RNN.ipynb` en Jupyter Notebook o VS Code.
   - Ejecuta las celdas en orden para entrenar y probar cada modelo.
   - Los modelos entrenados se guardan como archivos `.keras` y pueden cargarse para predicción sin reentrenar.

## Conclusiones y aprendizajes

- El preprocesamiento de datos es fundamental para obtener buenos resultados en modelos de deep learning.
- Cada arquitectura tiene ventajas según el tipo de datos: MLP para tabulares, CNN para imágenes, RNN para secuencias temporales.
- La regularización (Dropout, EarlyStopping) ayuda a evitar el overfitting.
- La calidad y cantidad de datos impacta directamente en la capacidad predictiva del modelo.
- Aprendí a comparar resultados entre diferentes modelos y a interpretar métricas como accuracy y loss.

---