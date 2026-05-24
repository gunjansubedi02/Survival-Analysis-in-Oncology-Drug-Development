# Survival Analysis in Oncology Drug Development

**Author:** Gunjan Subedi  
**Programme:** Masters in AI for Drug Development  
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
