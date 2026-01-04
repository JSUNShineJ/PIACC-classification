# PIACC-classification
This project builds supervised classification models on part of the PIAAC dataset. 

Random Forest and XGBoost classifiers were then trained on the cleaned dataset. To address class imbalance, SMOTE-based oversampling (k = 5) was applied to the base XGBosst as well as Random Forest models to enrich minority-class patterns. Model performance was evaluated using cross-validation.

After model selection and tuning, the best-performing model achieved an overall classification accuracy of 79%.

## Data
(1) PIAAC_US_2012_subsample.csv
The dataset includes n=664 respondents, all of them took 14 PSTRE items, 588 variables, including the gold standard “PS_class” as the final variable.

(2) Variable information.xlxs
This document provides a codebook to explains about variable labels and values (esp. for nominal and ordinal variables) in the PIAAC_US_2012_subsample.csv
Variables 3-139 are related to behavioral variables, variables 139-587 are related to background variables, variable 588 is the gold standard “Class”.

More information can be found on OECD PIAAC website:
https://www.oecd.org/skills/piaac/data/


## Methods

(1) Data cleaning on raw, unprocessed survey data  
- Feature selection by removing variables with high missing value proportions.
- Multicollinearity control via correlation filtering
(2) Supervised classification using Random Forest and XGBoost  
- SMOTE oversampling (k = 5) 
- Model evaluation using cross-validation, confusion matrix, and ROC curves.

## Tools

R, tidyverse, caret, ranger, xgboost, ROC curves
