# Breast Cancer Diagnosis: A Machine Learning Classification Study

This repository showcases a comparative machine learning solution for **breast cancer diagnosis** using multiple supervised learning models. The project is a collaborative effort by **Ankita Saha** and **Alisha Rawat**.

---

## Project Overview  

### Objective  
The project aims to evaluate and compare the performance of different machine learning classifiers in identifying **malignant vs benign tumors** using diagnostic measurements. The goal is to determine which model offers the best trade-off between accuracy, reliability, and generalization for healthcare decision support.

---

## Key Features  

- **Multi-Model Evaluation:** Comparison of KNN, Random Forest, Logistic Regression, and Support Vector Machine (SVM).  
- **Baseline vs Tuned Models:** Performance analysis before and after hyperparameter tuning using GridSearchCV.  
- **Medical-Focused Metrics:** Evaluation using Accuracy, Precision, Recall, F1-Score, and ROC-AUC.  
- **Visualization:** Confusion matrices and ROC curves to assess classification behavior.  
- **Standardized Pipeline:** Consistent preprocessing, scaling, and train-test splits for fair comparison.

---

## Problem Statement  

Breast cancer is one of the leading causes of mortality among women worldwide. Although hospitals collect large volumes of diagnostic data, extracting reliable insights for early detection remains a challenge.

This project addresses the following challenges:

- Difficulty in selecting the most effective classifier for medical diagnosis.  
- Risk of false negatives (missed malignant cases).  
- Lack of comparative performance analysis across multiple algorithms.

The dataset is sourced from the **Breast Cancer Wisconsin (Diagnostic) Dataset** from the UCI Machine Learning Repository and contains 30 numeric features extracted from digitized breast mass images.

---
## Dataset  

- **Source:** https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic


## Methodology  

### Data Preparation  
- 80/20 train-test split  
- Numeric feature scaling using **StandardScaler** (for KNN, Logistic Regression, SVM)  
- No scaling for Random Forest  

### Models Used  
- K-Nearest Neighbors (KNN)  
- Random Forest  
- Logistic Regression  
- Support Vector Machine (SVM)  

### Model Optimization  
Each model is evaluated in two stages:  
1. **Baseline model** using default parameters  
2. **Tuned model** using **GridSearchCV (5-fold cross-validation)**  

---

## Results Summary (Tuned Models)

| Model | Accuracy | Precision | Recall | F1 Score | ROC AUC |
|------|----------|-----------|--------|----------|---------|
| KNN (Tuned) | 0.9386 | 0.9730 | 0.8571 | 0.9114 | 0.9825 |
| Random Forest (Tuned) | 0.9737 | 1.0000 | 0.9286 | 0.9630 | 0.9929 |
| Logistic Regression (Tuned) | 0.9737 | 0.9756 | 0.9524 | 0.9639 | 0.9831 |
| **SVM (Tuned)** | **0.9912** | **1.0000** | **0.9762** | **0.9880** | **0.9970** |

**Best Model:** Tuned **SVM** achieved the highest overall performance and strongest class separation.

---

## Technologies Used  

- **Programming Language:** Python  
- **Libraries:** NumPy, Pandas, Scikit-learn, Matplotlib, Seaborn  
- **Model Tuning:** GridSearchCV  
- **Development Environment:** Jupyter Notebook  

---

## Business Impact

- **Better Decision Support:** Compared multiple prediction approaches to identify the most reliable one, helping organizations make more confident, data-driven decisions.

- **Reduced Manual Effort:** Demonstrated how data can be used to automatically classify and prioritize cases, saving time and reducing reliance on manual review.

- **Higher Accuracy in Outcomes:** Showed how tuning and refining models improves result quality, leading to more trustworthy predictions.

- **Scalable Use Case:** The same analysis framework can be applied to other business problems where classification or risk scoring is required.

- **Clear Performance Insights:** Created simple performance comparisons and visuals that make results easy to understand for both technical and non-technical audiences.

---

## Getting Started  

Users can download the `.ipynb` file from this repository and execute it locally in Jupyter Notebook.
