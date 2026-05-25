# Aviation Analytics ML Platform

An end-to-end aviation analytics and airline delay prediction platform built using AWS EMR, Hive, and Machine Learning.

## Project Overview

This project focuses on predicting airline delays using distributed data engineering workflows and machine learning classification models.

The workflow includes:
- Distributed data processing using AWS EMR and Hive
- Balanced sampling strategy for delayed and non-delayed flights
- Dataset merging and preprocessing
- Training and evaluating multiple machine learning models
- Final prediction on unseen target datasets

## Architecture Workflow

```text
Hive Sampling
      ↓
Balanced Datasets
      ↓
Merged Dataset
      ↓
Data Cleaning
      ↓
Feature Engineering
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
```

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- CatBoost
- AWS EMR
- Apache Hive
- Matplotlib
- Seaborn
- Jupyter Notebook

## Models Implemented

- Decision Tree Classifier
- Random Forest Classifier
- CatBoost Classifier
- XGBoost Classifier

## Best Performing Model

XGBoost achieved the best overall performance during evaluation.

### Final Metrics

| Metric | Score |
|---|---|
| Accuracy | 88.46% |
| Precision | 93.37% |
| Recall | 83.11% |
| F1 Score | 87.94% |

## Dataset Engineering

The project uses balanced datasets sampled from distributed Hive tables.

Each team member contributed data from assigned airline records and merged them into a consolidated dataset for model training.

### Features Removed

| Feature | Reason |
|---|---|
| Delayed | Target Variable |
| ArrDelay | Data Leakage |
| DepDelay | Data Leakage |
| AirTime | Missing in Target Dataset |

## Repository Structure

```text
aviation-analytics-ml-platform/
│
├── README.md
├── requirements.txt
├── notebooks/
├── data/
├── results/
├── presentations/
├── screenshots/
└── docs/
```

## Future Enhancements

Planned future enhancements include:
- Streamlit dashboard
- GenAI-powered aviation assistant
- RAG-based aviation analytics chatbot
- Real-time flight delay prediction APIs
- Weather and operational data integrations

## Contributors

This project was completed as part of a collaborative academic group project.

Primary contributions include:
- AWS EMR and Hive workflow
- Balanced dataset generation
- Data preprocessing and feature engineering
- Model evaluation and comparison
- XGBoost optimization and analysis
