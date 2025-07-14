# 🔬 Predicting Pediatric Appendicitis and Severity Using Machine Learning

This project presents a machine learning-driven clinical decision support tool designed to predict the presence and severity of pediatric appendicitis. By leveraging structured clinical, laboratory, and ultrasound-derived features, it provides rapid and accurate predictions to aid healthcare professionals in diagnosis and treatment planning.

---

## Objectives

- **Diagnosis Prediction:** Classify pediatric patients as having appendicitis or not.
- **Severity Prediction:** Determine whether appendicitis is uncomplicated or complicated.
- **Deployment:** Create an intuitive, interactive web application for real-time decision support in clinical settings.

---

## Dataset

- **Regensburg Pediatric Appendicitis Dataset** (782 patients aged 0-18).
- **Features Include:**
  - Demographics: Age, Sex, BMI
  - Clinical Scores: Alvarado Score, Pediatric Appendicitis Score
  - Physical Symptoms: Rebound tenderness, nausea
  - Lab Results: White Blood Cell (WBC) count, C-Reactive Protein (CRP)
  - Ultrasound Findings: Appendix diameter, free fluids, detectability of appendix
- **Outcomes:**
  - Diagnosis (Appendicitis / No Appendicitis)
  - Severity (Complicated / Uncomplicated)

---

## Methodology

### Data Preprocessing:
- KNN imputation for missing numerical values
- Standardisation of numerical features
- One-hot encoding for categorical features

### Modelling Techniques:
- Logistic Regression
- Elastic Net Regularisation
- Random Forest
- XGBoost (Best performing and selected model)
- Multilayer Perceptron (MLP) Neural Network

### Validation:
- Monte Carlo Cross-Validation (MCCV) with 200 iterations (80% training, 20% testing)
- Metrics Evaluated: Accuracy, Recall, Precision, F1-score, AUC

---

## Results

### Diagnosis (Appendicitis vs. No Appendicitis):
- **Best Model:** XGBoost
- **Mean Accuracy:** 96%
- **Mean F1-score:** 95%
- **Key Predictors:**
  - Detectability of appendix via ultrasound
  - Appendix Diameter
  - Length of hospital stay

### Severity (Complicated vs. Uncomplicated):
- **Best Models:** MLP and XGBoost
- **Mean Accuracy:** 90% (MLP), 81% (XGBoost)
- **Mean F1-score:** 81% (MLP), 78% (XGBoost)
- **Key Predictors:**
  - Length of hospital stay
  - CRP levels

XGBoost selected for deployment due to stable performance and efficiency.

---

## Web Application

An interactive web application was developed using **Gradio**. Users can input patient-specific clinical, laboratory, and imaging data to obtain real-time predictions of appendicitis diagnosis and severity.

---


