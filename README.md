# AQMD - Machine Learning Based Water Potability Classification

## Project Overview
This project extends our physical Air/Water Quality Monitoring Device (AQMD) hardware system toward predictive analytics. By leveraging historical chemical sensor characteristics, we trained an optimized Random Forest ensemble model to classify whether water is potable or non-potable, laying the framework for proactive predictive water-quality alerts within embedded environments.

## Dataset
- **Source:** Water Potability Dataset (Kaggle by Aditya Kadiwal)
- **Size:** 3,276 samples, 9 features
- **Features Analyzed:** pH, Hardness, Solids, Chloramines, Sulfate, Conductivity, Organic Carbon, Trihalomethanes, Turbidity

## Approach
1. **Data Preprocessing:** Handled missing values using Median Imputation (`SimpleImputer`) to navigate missing data naturally found in physical environments.
2. **Feature Scaling:** Applied standard scaling for distance-based estimators.
3. **Data Splitting:** Stratified 80/20 train/test split to perfectly preserve class balance.
4. **Model Training:** Benchmarked Baseline Logistic Regression against a robust Random Forest Classifier (200 estimators).

## Key Metrics Achieved
- **Random Forest Classifier:** 66.92% Accuracy | Weighted F1-Score: 0.63
- **Logistic Regression Baseline:** 60.98% Accuracy (Failed to map the non-linear boundaries of the multi-parameter dataset)

## Feature Importance Takeaways
The physical parameters contributing the highest predictive weight to our classifier are:
1. **pH Level:** 12.94% predictive importance
2. **Sulfate Concentration:** 12.73% predictive importance
3. **Hardness:** 12.29% predictive importance
