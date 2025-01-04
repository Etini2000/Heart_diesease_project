# Heart Disease Diagnosis Using Biomarkers

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
##The code snipet below
```
import numpy as np
import pandas as pd

np.random.seed(42)

# Number of individuals
n = 1000

# Generate demographic data
data = pd.DataFrame({
    'age': np.random.randint(20, 81, n),
    'gender': np.random.choice(['Male', 'Female'], n),
    'smoker': np.random.choice([0, 1], n, p=[0.7, 0.3]),  # 30% smokers
    'exercise_level': np.random.choice(['Low', 'Moderate', 'High'], n, p=[0.5, 0.3, 0.2])
})

# Generate biomarker data
data['systolic_bp'] = np.random.normal(120, 15, n).clip(90, 200)
data['diastolic_bp'] = np.random.normal(80, 10, n).clip(60, 120)
data['total_cholesterol'] = np.random.normal(200, 30, n).clip(125, 300)
data['hdl'] = np.random.normal(50, 10, n).clip(30, 80)
data['ldl'] = np.random.normal(120, 30, n).clip(80, 190)
data['fasting_glucose'] = np.random.normal(100, 15, n).clip(70, 150)

# Heart disease risk (target)
data['heart_disease'] = (data['age'] > 50).astype(int)  # Simplified rule
data['heart_disease'] |= (data['systolic_bp'] > 140).astype(int)
data['heart_disease'] |= (data['total_cholesterol'] > 240).astype(int)
data['heart_disease'] = data['heart_disease'].apply(lambda x: 1 if x > 0 else 0)

```

## Machine Learning Model

A **Random Forest Classifier** was used to predict heart disease. 
80% training set and 20% testing set was used.
The following evaluation metrics were achieved:

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
- `notebooks/`: Jupyter notebooks for data analysis, modeling, and evaluation <a href = "https://github.com/Etini2000/Heart_diesease_project/blob/main/Heart_disease_project.ipynb"></a>
- `models/`: Saved Random Forest model <a href = "https://github.com/Etini2000/Heart_diesease_project/blob/main/heart_disease_prediction.joblib"></a>
- `visualizations/`: Confusion matrix and feature importance plots
- `dashboard/`: Power BI file for interactive visualization ![Heart Disease Project Summary](https://github.com/user-attachments/assets/45a09035-dcca-4649-8f23-1ead132f6eb0)


## Results
The Random Forest Classifier performed exceptionally well on the simulated dataset, with perfect scores across all evaluation metrics. 
Similarly, the Power BI dashboard provided a simple and actionable insights into heart disease predictors and risk factors among my sample population.


## Acknowledgments
Thanks to 3MTT Nigeria for giving me the opportunity and resources to learn Data Science and Analytics. 
