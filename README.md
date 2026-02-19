# Cancer Patient Survival Analysis

A data science project analyzing clinical cancer registry data (TCGA) to predict patient survival outcomes using machine learning. Evaluates Random Forest, Gradient Boosting, SVR, and XGBoost alongside Kaplan-Meier survival analysis on 988 patient records.

## Overview

This project analyzes comprehensive patient profiles from a cancer registry to identify patterns in patient outcomes and therapy response. It investigates relationships between demographic variables, tumor characteristics, treatment outcomes, and survival metrics.

## Key Results

### Model Performance (Predicting Overall Survival)

| Model | MAE (months) | RMSE (months) | R2 Score |
|-------|-------------|--------------|----------|
| **SVR** | **31.20** | **39.93** | -0.07 |
| Gradient Boosting | 32.18 | 40.09 | -0.08 |
| XGBoost | 35.48 | 44.56 | -0.34 |
| Random Forest | 36.56 | 46.48 | -0.45 |

SVR achieved the best performance. Negative R2 scores across all models highlight the complexity of survival prediction from clinical features alone, suggesting additional molecular or genomic data may be needed.

### Clinical Insights
- Heterogeneous therapeutic responses across patients with similar profiles
- Tumor stage and residual disease show association with survival outcomes
- Kaplan-Meier survival curves reveal distinct patterns across patient subgroups

## Dataset

- **988 patient records** from TCGA (The Cancer Genome Atlas)
- **13 clinical features:** Age at diagnosis, vital status, tumor stage/grade, residual disease, therapy outcome, cancer status, overall survival, progression-free survival, platinum status
- **Survival range:** 0.03 - 179.18 months (mean: 48 months)

## Tech Stack

Python, scikit-learn (Random Forest, SVR), XGBoost, Gradient Boosting, lifelines (Kaplan-Meier), pandas, matplotlib, seaborn

## Methods

1. **Preprocessing:** Missing value imputation (median/mode), label encoding, standardization, 80/20 train-test split
2. **EDA:** Correlation heatmap, distribution analysis, categorical variable plots
3. **Survival Analysis:** Kaplan-Meier curves using lifelines
4. **Regression Models:** Random Forest, Gradient Boosting, SVR, XGBoost

## Project Structure

```
├── DSAF Final Project.ipynb              # Complete analysis notebook
├── augmented_clinical_data.csv           # Dataset (988 records, 13 features)
├── index.html                            # Rendered notebook for web viewing
└── DSAF Domain Area Presentation.pptx    # Project presentation
```

## Collaborators

Kaamala Lalith Sai Reddy, Kaushik Mantha, Preeth Nath Manjunath, Vineel Rayapati, Harshitha Konduru, Saketh Saridena

## How to Run

1. Clone the repository
2. Install dependencies: `pip install pandas numpy scikit-learn xgboost lifelines matplotlib seaborn`
3. Open and run `DSAF Final Project.ipynb`
