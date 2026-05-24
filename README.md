# Survival Analysis in Oncology Drug Development


---

# Survival Analysis in Oncology Drug Development

**Author:** Gunjan Subedi
**Programme:** Masters in AI for Drug Development (Independent project developed alongside the programme)
**Dataset:** Simulated Phase III Oncology Trial — Overall Survival (OS)

---

## Overview

This project applies three progressively advanced survival analysis methods to a simulated Phase III oncology clinical trial dataset. The goal is to evaluate whether an experimental drug prolongs overall survival (OS) compared to a standard chemotherapy regimen — the same analytical framework used in real FDA and EMA regulatory submissions.

The notebook progresses from interpretable classical statistics to a deep learning approach, providing both methodological depth and clinical context at each stage.

---

## Methods Implemented

| Method | Type | Purpose |
|---|---|---|
| Kaplan-Meier (KM) | Non-parametric | Survival curves; visual comparison of treatment arms |
| Cox Proportional Hazards | Semi-parametric | Hazard ratios for each clinical covariate |
| DeepSurv (Neural Network) | Deep Learning | Non-linear survival modelling; risk stratification |

---

## Clinical Context

Survival analysis is the backbone of Phase III oncology trials. Regulatory agencies (FDA, EMA) require evidence that a new drug prolongs survival — the methods demonstrated in this notebook are exactly how those decisions are made in practice.

The dataset simulates a realistic oncology trial with clinically meaningful variables including ECOG performance status, cancer stage, PD-L1 biomarker expression, prior therapy lines, and tumor size.

---

## Project Structure

- survival_analysis_oncology.ipynb — Main analysis notebook
- README.md — This file

**Notebook sections:**

1. Environment Setup and Imports
2. Data Loading and Exploratory Analysis
3. Kaplan-Meier Survival Analysis (overall + biomarker subgroup + stage subgroup)
4. Cox Proportional Hazards Model (multivariable + forest plot + assumption checks + predicted curves)
5. DeepSurv Neural Network (architecture + training + evaluation + feature importance)
6. Model Comparison and Summary Figure
7. Clinical Interpretation and Takeaways

---

## Key Results (Simulated Data)

- KM curves show a statistically significant OS benefit for the experimental arm (log-rank test)
- Cox model hazard ratios identify treatment arm, biomarker status, and ECOG performance status as the strongest predictors
- DeepSurv successfully stratifies patients into low- and high-risk groups and captures non-linear covariate interactions missed by the standard Cox model
- C-index comparison between Cox and DeepSurv provides a quantitative measure of predictive improvement

---

## Tools and Libraries

- Python 3.x
- lifelines — Kaplan-Meier and Cox PH fitting, log-rank testing
- PyTorch — DeepSurv neural network implementation
- scikit-learn — preprocessing, train/test split
- pandas, numpy — data manipulation
- matplotlib, seaborn — visualisation

Install dependencies: pip install lifelines scikit-survival torch pandas numpy matplotlib seaborn scipy

---

## Dataset

The dataset is fully simulated for educational and portfolio purposes using clinically realistic parameter ranges. It is not derived from any real patient data. Variables include:

| Variable | Description |
|---|---|
| treatment_arm | Standard chemotherapy vs Experimental drug |
| age | Age at enrollment (years) |
| ecog_ps | ECOG Performance Status (0–2) |
| stage | Cancer stage at enrollment (III or IV) |
| biomarker_positive | Binary biomarker status (e.g. PD-L1 threshold) |
| pdl1_expression_pct | Continuous PD-L1 expression (%) |
| prior_therapies | Number of prior treatment lines |
| tumor_size_cm | Largest tumour diameter (cm) |
| os_months | Overall Survival endpoint (months) |
| os_event | Event indicator: 1 = death, 0 = censored |

---

## References

1. Kaplan EL, Meier P (1958). Nonparametric estimation from incomplete observations. Journal of the American Statistical Association.
2. Cox DR (1972). Regression models and life-tables. Journal of the Royal Statistical Society, Series B.
3. Katzman JL et al. (2018). DeepSurv: personalized treatment recommender system using a Cox proportional hazards deep neural network. BMC Medical Informatics and Decision Making.
4. Harrell FE (2015). Regression Modeling Strategies. Springer.
5. FDA Guidance: Clinical Trial Endpoints for the Approval of Cancer Drugs and Biologics (2018).

---

## About

An independent project developed alongside my Masters in AI for Drug Development. It demonstrates the application of statistical and machine learning methods to clinical trial data analysis — a core competency in computational drug development and clinical data science roles.

---
