# Thermal Runaway Prediction in Lithium-Ion Batteries using Machine Learning

## Overview

Thermal runaway is one of the primary safety concerns in lithium-ion batteries, where rapid heat generation can lead to catastrophic cell failure. Early prediction of thermal runaway enables timely intervention and improves battery safety in electric vehicles and energy storage systems.

This project develops a machine learning pipeline to classify battery states as **Safe** or **Thermal Runaway** using experimental mechanical abuse data obtained from standardized **single-side indentation tests**. Multiple supervised and unsupervised learning algorithms are evaluated to identify the most effective approach for early thermal runaway detection.

---

## Objectives

- Construct a labeled dataset from experimental battery measurements.
- Engineer predictive features from voltage and temperature signals.
- Compare supervised and unsupervised machine learning models.
- Evaluate model performance using standard classification metrics.

---

## Dataset

The dataset consists of experimental measurements collected during standardized **single-side indentation tests** on lithium-ion cells.

Features include:

- Temperature
- Voltage
- State of Charge (SOC)
- Time-series derived features
- Engineered temperature and voltage trends

The target variable is a binary label:

- **0 → Safe**
- **1 → Thermal Runaway**

---

## Machine Learning Pipeline

### Data Preprocessing

- Missing value handling
- Feature scaling
- Class imbalance handling
- Train-test split

### Feature Engineering

Engineered features include:

- Temperature rate of change
- Voltage rate of change
- Voltage difference
- Rolling temperature statistics
- Time-series derived features

### Models Implemented

Supervised Models

- XGBoost
- Logistic Regression

Unsupervised Models

- Isolation Forest
- K-Means Clustering

---

## Evaluation Metrics

Models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC

Threshold optimization was performed to improve classification performance.

---

## Results

Among all evaluated models, **XGBoost** achieved the best overall performance. The supervised models consistently outperformed the unsupervised approaches for thermal runaway classification.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- Matplotlib
- Seaborn

---


## Key Learnings

Through this project I learned:

- Building end-to-end machine learning pipelines
- Feature engineering for time-series sensor data
- Handling imbalanced datasets
- Threshold optimization
- Comparing supervised and unsupervised learning algorithms
- Model evaluation using multiple performance metrics

---

## Future Work

- Incorporate sequential deep learning models (LSTM/GRU)
- Explore Transformer-based time-series models
- Improve explainability using SHAP values
- Develop an early-warning prediction framework for battery safety
