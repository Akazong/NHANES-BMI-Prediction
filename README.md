# Predicting Body Mass Index Among U.S. Adults Using Machine Learning

## Overview

This project uses data from the U.S. National Health and Nutrition Examination Survey (NHANES) to evaluate machine-learning regression models for predicting Body Mass Index (BMI) among adults.

Data from three NHANES survey cycles (2013–2014, 2015–2016, and 2017–2018) were integrated, cleaned, explored, and analysed using eight regression algorithms.

A particular focus of the project was assessing how strongly model performance depended on waist circumference, an anthropometric measurement closely related to BMI.

## Research Question

**To what extent can demographic, socioeconomic, lifestyle, clinical and anthropometric data predict BMI among U.S. adults across different machine-learning regression models?**

A secondary analysis examined whether strong predictive performance could be maintained when waist circumference was excluded.

## Dataset

**Source:** National Health and Nutrition Examination Survey (NHANES), U.S. Centers for Disease Control and Prevention (CDC).

Survey cycles:
- 2013–2014
- 2015–2016
- 2017–2018

The final analytical dataset contained **16,943 adults aged 18 years and older with available BMI measurements**.

## Machine-Learning Models

Eight regression algorithms were evaluated:

1. Linear Regression
2. Ridge Regression
3. Lasso Regression
4. Decision Tree Regression
5. Random Forest Regression
6. Gradient Boosting Regression
7. Support Vector Regression
8. K-Nearest Neighbours Regression

Model performance was evaluated using **R², RMSE and MAE**.

## Key Results

Random Forest achieved the strongest overall predictive performance:

- **R²:** 0.8576
- **RMSE:** 2.79 kg/m²
- **MAE:** 1.95 kg/m²

Gradient Boosting was the second-best model.

Waist circumference was the dominant Random Forest feature. When waist circumference was excluded, Random Forest performance decreased substantially:

- **R² with waist circumference:** 0.8576
- **R² without waist circumference:** 0.4967
- **R² after tuning the no-waist model:** 0.5074

The sensitivity analysis demonstrated that the strong performance of the full Random Forest model depended substantially on waist circumference.

## Repository Structure

```text
NHANES-BMI-Prediction/
├── notebooks/
│   ├── 01_data_collection_integration.ipynb
│   ├── 02_data_cleaning_preprocessing.ipynb
│   ├── 03_exploratory_data_analysis.ipynb
│   └── 04_regression_modelling.ipynb
├── outputs/
│   └── regression_model_comparison.csv
├── README.md
├── requirements.txt
└── .gitignore
## Analysis Workflow

1. NHANES data collection and integration across three survey cycles
2. Data cleaning and preprocessing
3. Exploratory data analysis
4. Regression modelling and model comparison
5. Random Forest feature-importance analysis
6. Sensitivity analysis with and without waist circumference
7. Hyperparameter tuning of the no-waist Random Forest model

## Tools and Libraries

- Python
- pandas
- NumPy
- Matplotlib
- Seaborn
- scikit-learn
- Jupyter Notebook

## Data Availability

This project uses publicly available data from the U.S. National Health and Nutrition Examination Survey (NHANES). Raw NHANES data files are not stored in this repository. The notebooks document the data integration and processing workflow used to construct the analytical dataset.

## Author

**Etheline W. Akazong**

PhD in Biochemistry | Research Scientist | Data Science & Health Analytics
