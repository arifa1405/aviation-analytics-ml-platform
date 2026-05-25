# Aviation Analytics ML Platform

An end-to-end aviation analytics and airline delay prediction platform built using AWS EMR, Apache Hive, and Machine Learning.

This project demonstrates a complete data engineering and machine learning workflow for large-scale airline delay analytics using distributed processing and classification models.

---

# Project Overview

The objective of this project is to predict whether a flight will be delayed based on operational flight attributes.

The project combines:

- Distributed data engineering using AWS EMR and Hive
- Large-scale dataset preprocessing
- Feature engineering and model training
- Multi-model evaluation and comparison
- Final prediction generation on unseen target datasets
- Exporting trained models and prediction artifacts

---

# End-to-End Workflow

```text
AWS EMR + Hive
        ↓
Balanced Flight Sampling
        ↓
Merged Airline Dataset
        ↓
Data Cleaning & Feature Engineering
        ↓
Feature Encoding
        ↓
Train/Test Split
        ↓
Model Training
        ↓
Model Evaluation
        ↓
Best Model Selection
        ↓
Target Dataset Prediction
        ↓
Metrics & Predictions Export
```

---

# Technologies Used

## Data Engineering
- AWS EMR
- Apache Hive
- Hadoop Ecosystem
- Distributed Query Processing

## Machine Learning
- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- CatBoost
- Joblib

## Visualization & Development
- Matplotlib
- Seaborn
- Jupyter Notebook
- VS Code
- Git & GitHub

---

# Machine Learning Models Implemented

| Model | Purpose |
|---|---|
| Decision Tree Classifier | Baseline interpretable classifier |
| Random Forest Classifier | Ensemble learning and robustness |
| CatBoost Classifier | Gradient boosting for categorical patterns |
| XGBoost Classifier | Optimized boosting model for best performance |

---

# Best Performing Model

XGBoost achieved the strongest overall performance after threshold tuning and evaluation.

## Final Evaluation Metrics

| Metric | Score |
|---|---|
| Accuracy | 88.46% |
| Precision | 93.37% |
| Recall | 83.11% |
| F1 Score | 87.94% |
| ROC-AUC | 95.72% |

---

# Dataset Engineering

The training dataset was generated using distributed Hive sampling workflows on AWS EMR.

Balanced datasets were created to ensure equal representation of delayed and non-delayed flights.

The final merged dataset was used for preprocessing, feature engineering, encoding, and model training.

## Features Removed During Preprocessing

| Feature | Reason |
|---|---|
| Delayed | Target variable |
| ArrDelay | Data leakage |
| DepDelay | Data leakage |
| AirTime | Missing in target dataset |
| CancellationCode | Sparse / low utility |

---

# Exported Outputs

The project exports:

- Model evaluation metrics CSV
- Target dataset prediction CSV
- Serialized trained models using Joblib

Generated outputs are stored inside:

```text
results/
├── metrics/
├── predictions/
└── trained_models/
```

---

# Repository Structure

```text
aviation-analytics-ml-platform/
│
├── README.md
├── requirements.txt
├── data/
│   └── raw/
├── notebooks/
│   └── Airline_Delay_Prediction_End_to_End.ipynb
├── results/
│   ├── metrics/
│   ├── predictions/
│   └── trained_models/
├── screenshots/
├── docs/
└── presentations/
```

---

# Key Engineering Highlights

- Built distributed Hive workflows for airline data processing
- Performed large-scale dataset merging and preprocessing
- Implemented feature engineering and encoding pipelines
- Compared multiple ML classification models
- Tuned XGBoost threshold for improved F1 performance
- Exported reusable prediction artifacts and trained models
- Structured repository for reproducibility and portfolio presentation

---

# Future Enhancements

Planned future enhancements include:

- Streamlit analytics dashboard
- Real-time prediction APIs
- Flight operations monitoring dashboards
- Weather data integration
- GenAI-powered aviation assistant
- RAG-based aviation analytics chatbot
- LLM-powered operational insights

---

# Author

Arifa Farhath

This project was developed as part of graduate-level machine learning and data engineering work with additional refactoring and production-style repository structuring for portfolio presentation.
