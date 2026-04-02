# Pediatric Appendicitis Prediction — Clinical Decision Support

ML system for classifying pediatric appendicitis diagnosis and severity from clinical, laboratory, and ultrasound data — achieving 96% accuracy with a live Gradio web application for real-time clinical decision support.

[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![XGBoost](https://img.shields.io/badge/XGBoost-337733?style=for-the-badge&logoColor=white)](https://xgboost.ai)
[![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)](https://pytorch.org)
[![SHAP](https://img.shields.io/badge/SHAP-Explainability-ff6b6b?style=for-the-badge)](https://shap.readthedocs.io)
[![Gradio](https://img.shields.io/badge/Live%20Demo-Gradio%20App-FF7C00?style=for-the-badge&logo=gradio)](https://github.com/EoinHoustoun/Pediatric_Appendicitis)

---

## Overview

- **Problem:** Pediatric appendicitis diagnosis is challenging — misdiagnosis leads to unnecessary surgery or dangerous delays. Clinicians need fast, explainable decision support combining labs, imaging, and clinical signs.
- **Approach:** XGBoost and MLP neural networks trained on the Regensburg Pediatric Appendicitis dataset (782 patients), validated with Monte Carlo cross-validation (200 iterations). SHAP analysis provides per-patient feature attribution. Deployed as a live Gradio web application.
- **Result:** XGBoost achieved **96% accuracy and 95% F1-score** for appendicitis detection; MLP reached **90% accuracy** for severity classification.

---

## Key Features

- Two classification tasks: appendicitis presence (binary) and severity level (multi-class)
- 782 real pediatric patients — demographics, clinical scores, labs (WBC, CRP), and ultrasound findings
- Monte Carlo cross-validation (200 iterations) for statistically robust evaluation
- SHAP feature importance analysis for model explainability — critical in clinical settings
- **Live Gradio web application** for real-time clinical decision support
- Full feature importance pipeline identifying the most diagnostically significant variables

---

## Tech Stack

| Category | Tools |
|---|---|
| Language | Python |
| Models | XGBoost, MLP (PyTorch), Logistic Regression, Random Forest |
| Validation | Monte Carlo Cross-Validation (200 iterations) |
| Explainability | SHAP |
| Deployment | Gradio |
| Libraries | scikit-learn, pandas, NumPy |
| Visualisation | matplotlib, seaborn |

---

## Results

| Task | Best Model | Accuracy | F1-Score |
|---|---|---|---|
| Appendicitis Detection | **XGBoost** | **96%** | **95%** |
| Severity Classification | **MLP (PyTorch)** | **90%** | — |

- SHAP analysis identified WBC count, CRP level, and ultrasound findings as the strongest predictors
- Monte Carlo CV (200 iterations) confirmed results are robust and not due to favourable data splits
- Gradio app enables clinicians to input patient data and receive a probability-based prediction instantly

---

## How to Run

```bash
pip install -r requirements.txt

# Run the Gradio web application
python app.py

# Or explore the full analysis
jupyter notebook
```

---

## Project Structure

```
Pediatric_Appendicitis/
├── appendicitis_analysis.ipynb   # Full ML pipeline and SHAP analysis
├── app.py                        # Gradio web application
├── requirements.txt
└── README.md
```

---

*Part of Eoin Houstoun's Data Science Portfolio — [github.com/EoinHoustoun](https://github.com/EoinHoustoun)*
