# Disease Diagnosis Using Biomarkers

This repository contains a project focused on predicting heart disease using biomarker data from a small population in my local government area. The project involves data generation, machine learning modeling, and interactive visualization.

## Overview
This project explores how biomarkers can help predict heart disease. It includes steps to:
1. Generate a synthetic dataset for a local population.
2. Build and evaluate a machine learning model for heart disease diagnosis.
3. Create an interactive Power BI dashboard to visualize insights from the data.

## Datasset
The <a href = "https://github.com/Etini2000/Heart_diesease_project/blob/main/Heart_disease_MLproject.csv">Dataset</a> includes features such as:
- Demographics: Age, Gender
- Biomarkers: LDL, HDL, Total Cholesterol, Fasting Glucose, systolic, and Diastolic Blood Pressure
- Lifestyle Factors: Smoking status, Exercise level
- Target Variable: Heart Disease (Yes/No)

### Data Generation
The dataset was synthetically generated, using numpy to simulate realistic distributions of biomarker and demographic data for a small local population.

## Machine Learning Model

A **Random Forest Classifier** was used to predict heart disease. The following evaluation metrics were achieved:

- **Accuracy**: 1.0
- **Precision**: 1.0
- **Recall**: 1.0
- **F1 Score**: 1.0

### Confusion Matrix
```
[[ 79   0]
 [  0 121]]
```

### ROC AUC Score
- **ROC AUC Score**: 1.0

### Visualizations
- Confusion matrix visualization.
- Feature importance plot showing the top predictors of heart disease.

## Power BI Dashboard
An interactive PowerBI <a href = "https://github.com/Etini2000/Heart_diesease_project/blob/main/Heart%20Disease%20Project%20Summary.pbix">Dashboard</a> was created to summarize demographic data and lifestyle factors.


## Repository Contents
- `data/`: Synthetic dataset (CSV format)
- `notebooks/`: Jupyter notebooks for data analysis, modeling, and evaluation
- `models/`: Saved Random Forest model
- `visualizations/`: Confusion matrix and feature importance plots
- `dashboard/`: Power BI file for interactive visualization

## Results
The Random Forest Classifier performed exceptionally well on the synthetic dataset, with perfect scores across all evaluation metrics. Similarly, the Power BI dashboard provided a simple and actionable insights into heart disease predictors and risk factors among my sample population.


## Acknowledgments
Thanks to 3MTT Nigeria for giving me the opportunity and resources to learn Data Science and Analytics. 
