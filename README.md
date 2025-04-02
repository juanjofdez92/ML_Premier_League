# Predicción de Over 2.5 goles en la Premier League con Machine Learning

Este proyecto utiliza técnicas de Machine Learning para predecir si un partido de la Premier League terminará con más de 2.5 goles. El objetivo es crear un modelo fiable que maximice el número de aciertos en este tipo de apuestas deportivas.

---

## Estructura del proyecto

- 📁 src/data_sample/ → Dataset original y versiones procesadas 
- 📁 src/models/ → Modelos entrenados guardados en formato .pkl 
- 📁 src/notebooks/ → Desarrollo completo del proyecto en Jupyter (.ipynb) 
- 📁 src/img/ → Gráficos, matrices de correlación, visualizaciones 
- 📄 requirements.txt → Archivo de dependencias 
- 📄 README.md → Descripción general del proyecto


---

## Metodología

1. **Carga y limpieza del dataset**
2. **Filtrado de las últimas temporadas**
3. **Ingeniería de variables (features)**
   - Rachas ofensivas y defensivas
   - Efectividad, precisión, ratio goles/disparos
   - Medias por temporada y por equipo
4. **EDA (Análisis Exploratorio de Datos)**
   - Distribución del target
   - Correlaciones con variables ofensivas
   - Comparativas con boxplots
5. **Entrenamiento de modelos**
   - Random Forest
   - Gradient Boosting
   - LightGBM
   - XGBoost RF
6. **Evaluación y comparación**
   - Métricas: F1-score, precisión, recall, accuracy
   - Foco en clase 1 (Over 2.5)

---

## Métrica objetivo

> Se busca optimizar el **F1-score de la clase 1 (Over 2.5 goles)**, buscando un equilibrio entre:
- **Recall**: Detectar la mayor cantidad de partidos con Over.
- **Precisión**: Minimizar los fallos cuando se predice Over.

---

## Requisitos

Las siguientes librerías son necesarias para ejecutar el proyecto:  
- numpy 
- pandas 
- seaborn 
- matplotlib 
- scikit-learn 
- xgboost 
- lightgbm 
- joblib 
- optuna


Instala todas las dependencias con:

> pip install -r requirements.txt


---

## Cómo usar los modelos entrenados

Los modelos entrenados se encuentran guardados en la carpeta `src/models` en formato `.pkl` (Joblib). Puedes cargarlos fácilmente de la siguiente manera:

import joblib
import pandas as pd
# Cargar el modelo entrenado (ejemplo con LightGBM)
model = joblib.load("../models/LGBMClassifier.pkl")


--- 

## Autor  
***Juan José Fernández Moreno***
📅 Proyecto desarrollado en 2025
🔬 Enfocado en aprendizaje automático aplicado a predicción deportiva


---

## Disclaimer 
Este proyecto se ha realizado con fines académicos y de aprendizaje. No constituye una recomendación real de apuestas deportivas ni garantiza resultados en entornos reales de juego.
