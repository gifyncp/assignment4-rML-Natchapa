# Assignment 4: From Accuracy to Accountability

**Course:** DNSC 6330 – Responsible Machine Learning  
**Instructor:** Michael Akinwumi  
**Student:** Natchapa Aunkay (Gift)  

---

## Overview
This project implements an end-to-end reliability audit pipeline for a predictive model using the COMPAS dataset. The goal is to move beyond traditional performance metrics and evaluate whether the model remains **reliable, fair, and robust under real-world conditions**.

The analysis follows Lecture 04 concepts, including distribution drift, generalization, spurious correlations, and robustness testing.

---

## Objectives
This assignment evaluates model behavior across five key dimensions:

- **Distribution Drift** → Has the data changed?
- **Generalization** → Does the model perform well on unseen data?
- **Spurious Correlations** → Is the model learning unstable or biased patterns?
- **Robustness** → Does performance degrade under stress?
- **Slice-Based Evaluation** → Does performance differ across subgroups?

---

## Models Used
- Logistic Regression (baseline, interpretable)
- Gradient Boosted Tree (higher-capacity model)

---

## Dataset
- COMPAS dataset (recidivism prediction)
- Target variable: `two_year_recid`

---

## Libraries Used
- pandas  
- numpy  
- matplotlib  
- seaborn  
- scikit-learn  
- scipy  
- statsmodels  
- shap  

---

## How to Run

1. Open the notebook in Google Colab or Jupyter Notebook  
2. Install required libraries if needed:
   ```bash
   pip install shap statsmodels
3. Run all cells from top to bottom
4. Ensure dataset is loaded correctly

---

## Project Structure

🔹 Part A: Distribution Drift
Compare train vs test distributions
Metrics: PSI, KS test, MMD
Purpose: Detect changes in the data-generating process

🔹 Part B: Generalization
Compare train vs test performance:
AUC
Accuracy
Log Loss
Purpose: Identify overfitting and generalization gap

🔹 Part C: Spurious Correlations
Counterfactual testing (e.g., race/gender swaps)
Measure prediction changes
Purpose: Detect reliance on unstable or biased features

🔹 Part D: Robustness & Stress Testing
Perturb key features (e.g., priors_count)
Perform sensitivity analysis
Purpose: Evaluate stability under realistic changes

🔹 Part E: Slice-Based Evaluation
Evaluate performance across subgroups:
Race
Gender
Age
Metrics:
AUC
FPR / FNR
Purpose: Identify hidden failures in subpopulations

---

## Key Insights
Strong overall performance does not guarantee reliability
Generalization gaps indicate potential overfitting
Subgroup disparities reveal fairness risks
Models must be tested under shift and stress before deployment

---

## Responsible ML Perspective
This project highlights that:
Performance must be evaluated beyond aggregate metrics
Models must remain reliable under changing conditions
Subgroup fairness and robustness are critical for deployment
Monitoring is required to prevent silent model failure

---

## AI Usage Disclosure
Generative AI (ChatGPT) was used to assist with code formatting and improving clarity. All analysis, modeling decisions, and interpretations are my own.
