🔍 Detección de Fraudes en Transacciones Bancarias / Credit Card Fraud Detection
📌 Descripción / Description

ES:
Este proyecto implementa un pipeline de Machine Learning para la detección de fraudes en transacciones bancarias.
Utiliza el dataset Credit Card Fraud Detection
, que contiene transacciones europeas de septiembre de 2013.

EN:
This project implements a Machine Learning pipeline for credit card fraud detection.
It uses the Credit Card Fraud Detection dataset
, which contains European transactions from September 2013.

🎯 Objetivos / Objectives

ES: Analizar el dataset, entrenar un modelo baseline y mejorar la precisión ajustando el umbral de decisión.

EN: Analyze the dataset, train a baseline model, and improve precision by adjusting the decision threshold.

🗂️ Estructura del Proyecto / Project Structure
proyecto-de-analisis-de-datos/
│
├── data/
│   └── raw/creditcard.csv
│
├── models/                        # Modelos guardados / Saved models
│
├── reports/
│   ├── figures/                   # Gráficas / Figures
│   └── metrics.txt                # Métricas / Metrics
│
├── src/
│   ├── train_full.py              # Entrenamiento / Training script
│   ├── eda.py                     # Análisis exploratorio / Exploratory Data Analysis
│   ├── features.py                # Ingeniería de características / Feature Engineering
│   ├── utils.py                   # Funciones auxiliares / Helper functions
│
├── requirements.txt
├── Makefile
└── README.md

⚙️ Instalación y Uso / Installation & Usage

ES:

git clone <URL_DEL_REPOSITORIO>
cd proyecto-de-analisis-de-datos

python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt

make train


EN:

git clone <REPOSITORY_URL>
cd proyecto-de-analisis-de-datos

python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt

make train

📊 Resultados / Results

Baseline (umbral 0.5 / threshold 0.5):

ROC AUC ≈ 0.97

PR AUC ≈ 0.72

Recall alto pero muchos falsos positivos / High recall but many false positives

Umbral ajustado (precision ≥ 0.70 / adjusted threshold):

Menos falsos positivos / Fewer false positives

Recall ≈ 0.84

F1-score ≈ 0.76

Figuras / Figures:

Confusion Matrix (Baseline / Threshold)

ROC Curve

PR Curve

🛠️ Tecnologías / Technologies

Python 3.x

NumPy, Pandas

Scikit-learn

Matplotlib, Seaborn

Imbalanced-learn

XGBoost

📌 Conclusiones / Conclusions

ES:
El modelo baseline es un buen punto de partida, pero el desbalance obliga a ajustar umbrales. Ajustar la precisión objetivo permite reducir falsos positivos sin perder demasiado recall.

EN:
The baseline model is a good starting point, but class imbalance requires threshold adjustment. Setting a target precision reduces false positives without losing too much recall.