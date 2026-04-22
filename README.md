# Disease Prediction Model - CodeAlpha Task 2

## Project Overview

This repository contains the development of a **Disease Prediction Model** designed to predict the possibility of diseases based on patient medical data. By leveraging machine learning classification techniques, this system assists in early and accurate detection of heart disease using structured clinical data.

This project was completed as part of the **CodeAlpha Machine Learning Internship (Task 2)**.

---

## 📽️ Project Demonstration

You can watch the full video explanation of this project here:
👉 [Project Video Link](https://youtu.be/gLwu765viBU?si=R_piBbZsOdypwTr8)

---

## Problem Statement

The goal is to classify patients into two categories based on clinical features:

- **No Disease (0):** Patient does not have heart disease.
- **Disease (1):** Patient has heart disease.

---

## Dataset

- **Source:** UCI ML Repository
- **Datasets Used:** Heart Disease, Diabetes, Breast Cancer
- **Features Used:** cp, thalach, slope, age, sex, ca, exang, oldpeak, thal

---

## Workflow

1. **Exploratory Data Analysis (EDA):** Visualized feature distributions using heatmaps, scatter plots, box plots, violin plots, and strip plots.
2. **Data Preprocessing:** Verified no null values; selected 9 key features based on correlation analysis.
3. **Model Training:** Trained and evaluated Decision Tree and Random Forest classifiers.
4. **Performance Evaluation:** Used Accuracy, Precision, Recall, F1-Score, and ROC-AUC metrics.
5. **Overfitting Check:** Compared Train vs. Test accuracy and F1-Score to confirm generalization.

---

## 🔍 EDA Key Insights

- Lower **Ca** values are more frequently associated with heart disease.
- Absence of **exercise-induced angina (exang = 0)** correlates with a positive target.
- Lower **Oldpeak** values are linked to disease patients (correlation: -0.43).
- Higher **Chest Pain Type (cp)** categories show a strong positive association with heart disease.
- Patients with heart disease tend to have **higher maximum heart rates (thalach)**.

---

## Results

Both models were compared, and **Random Forest Classifier** was selected as the final model:

| Model | Accuracy | Precision | Recall | F1 Score |
|---|---|---|---|---|
| Decision Tree | 98.53% | 1.00 | 0.97 | 0.98 |
| **Random Forest** | **98.53%** | **1.00** | **0.97** | **0.98** |

### Overfitting Check

| Metric | Training | Testing |
|---|---|---|
| Accuracy | 100% | 98.5% |
| F1 Score | 1.00 | 0.985 |

> The minimal gap between training and testing scores confirms the model **generalizes exceptionally well** with no significant overfitting.

---

## Why Random Forest?

Even with identical scores, Random Forest was preferred because:

1. **Stability** — More stable as it averages across multiple trees.
2. **Generalization** — Handles noise and outliers more effectively.
3. **Reduced Overfitting Risk** — Minimizes the risk common in a single deep Decision Tree.
4. **Reliability** — For medical predictions, an ensemble model is more robust and trustworthy.

---

## Tech Stack

- **Language:** Python
- **Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn

---

**Completed by:** Suryadip Das  
**Internship:** CodeAlpha Machine Learning Internship
