# Disease Diagnosis Using Biomarkers

This repository contains a project focused on predicting heart disease using biomarker data from a small population in [Your State]. The project involves data generation, machine learning modeling, and interactive visualization.

## Overview
This project explores how biomarkers can help predict heart disease. It includes steps to:
1. Generate a synthetic dataset for a local population.
2. Build and evaluate a machine learning model for heart disease diagnosis.
3. Create an interactive Power BI dashboard to visualize insights from the data.

## Datasset
The <a href = "https://github.com/Etini2000/Heart_diesease_project/blob/main/Heart_disease_MLproject.csv">Dataset</a> includes features such as:
- Demographics: Age, Gender
- Biomarkers: LDL, HDL, Total Cholesterol, Fasting Glucose, etc.
- Lifestyle Factors: Smoking status, Exercise level
- Target Variable: Heart Disease (Yes/No)

### Data Generation
The dataset was synthetically generated to simulate realistic distributions of biomarker and demographic data for a small local population.

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
An interactive Power BI dashboard was created to:
- Summarize key demographic and biomarker statistics.
- Visualize the distribution of biomarkers by heart disease status.
- Highlight relationships between lifestyle factors and heart disease risk.
- Display a correlation matrix and other insightful visualizations.

## Repository Contents
- `data/`: Synthetic dataset (CSV format)
- `notebooks/`: Jupyter notebooks for data analysis, modeling, and evaluation
- `models/`: Saved Random Forest model
- `visualizations/`: Confusion matrix and feature importance plots
- `dashboard/`: Power BI file for interactive visualization

## How to Run the Project

### Prerequisites
- Python 3.8+
- Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`
- Power BI Desktop

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/heart-disease-diagnosis.git
   cd heart-disease-diagnosis
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Jupyter notebook for model training and evaluation:
   ```bash
   jupyter notebook notebooks/heart_disease_modeling.ipynb
   ```
4. Open the Power BI dashboard:
   - Navigate to the `dashboard/` folder and open the `.pbix` file in Power BI Desktop.

## Results
The Random Forest Classifier performed exceptionally well on the synthetic dataset, with perfect scores across all evaluation metrics. The Power BI dashboard provides actionable insights into heart disease predictors and risk factors.

## Future Work
- Expand the dataset to include real-world data.
- Explore additional machine learning algorithms for comparison.
- Incorporate advanced data visualization techniques in Power BI.

## License
This project is licensed under the MIT License.

## Acknowledgments
Thanks to [Your State] for inspiring this work. Special mention to open-source tools and the Power BI community for enabling impactful data visualization.

---

Feel free to contribute or raise issues to improve this project!
