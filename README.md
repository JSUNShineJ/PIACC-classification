# PIACC-classification
This project builds supervised classification models on part of the PIAAC dataset. 

Random Forest and XGBoost classifiers were then trained on the cleaned dataset. To address class imbalance, SMOTE-based oversampling (k = 5) was applied to the Random Forest models to enrich minority-class patterns. Model performance was evaluated using cross-validation.

After model selection and tuning, the best-performing model achieved an overall classification accuracy of 79%.

## Methods

- Data cleaning on raw, unprocessed survey data  
- Feature selection by removing variables with high missing value proportions.
- Multicollinearity control via correlation filtering  
- Supervised classification using Random Forest and XGBoost  
- SMOTE oversampling (k = 5) applied to Random Forest  
- Model evaluation using cross-validation, confusion matrix, and ROC curves.

## Tools

R, tidyverse, caret, ranger, xgboost, ROC curves
