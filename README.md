# Heart-Disease-Project- Heart Disease Data Analysis

Overview
This project analyzes the Heart Disease UCI dataset to identify factors influencing heart disease. The dataset, sourced from Cleveland, Hungary, Switzerland, and VA Long Beach, contains 920 patient records with 16 features, including age, cholesterol, chest pain type, and heart disease diagnosis. The goal is to explore relationships between clinical variables and heart disease, addressing questions about age, cholesterol, chest pain, sex, maximum heart rate, and exercise-induced angina.

Objectives
Investigate how age and cholesterol levels affect heart disease likelihood.
Examine the influence of chest pain type on heart disease risk and its variation by sex.
Assess the association between maximum heart rate and exercise-induced angina with heart disease.

Dataset
Source: UCI Heart Disease Dataset (Kaggle).
Features: 16 columns, including:
age, sex, cp (chest pain type), trestbps (resting blood pressure), chol (cholesterol), fbs (fasting blood sugar), restecg (ECG results), thalch (maximum heart rate), exang (exercise-induced angina), oldpeak (ST depression), slope, ca (major vessels), thal (thalassemia), num (heart disease diagnosis: 0 = no disease, 1+ = disease).
Challenges: Missing values (e.g., 611 in ca, 486 in thal), zero values in trestbps and chol, and negative oldpeak values.
Methods

Data Cleaning
Duplicates: None found.
Missing Values:
Categorical: Imputed with mode (fbs, restecg, exang, slope).
Numerical: Imputed with median (trestbps, chol, thalch, oldpeak).
High missingness: ca imputed with -1, thal with 'unknown'.

Outliers:
Zero trestbps and chol replaced with median.
Negative oldpeak set to 0.
Data Types: Categorical variables converted to category type; fbs and exang standardized to 0/1.
Target: num binarized (0 = no disease, 1 = disease).


Analysis
Exploratory Data Analysis (EDA):
Analyzed 6+ variables (age, chol, thalch, cp, sex, exang).
Used 5+ visualization types (histograms, bar plots, box plots, scatter plots, heatmaps).

Key Questions:
Age and cholesterol vs. heart disease.
Chest pain type and sex vs. heart disease.
Maximum heart rate and exercise-induced angina vs. heart disease.

Key Findings
Age: Older patients (~55.9 years) are more likely to have heart disease than younger ones (~50.5 years).
Cholesterol: Slightly higher in heart disease patients (~244.1 mg/dl vs. ~238.5 mg/dl), but not a strong predictor.
Chest Pain Type: Asymptomatic pain strongly associated with heart disease.
Sex: Males have a higher heart disease prevalence than females.
Maximum Heart Rate: Lower rates correlate with heart disease.
Exercise-Induced Angina: Strong predictor (83.68% disease prevalence with angina vs. 38.94% without).

Repository Contents
heart_disease_uci.csv: Raw dataset.
analysis.ipynb: Jupyter notebook with data cleaning, EDA, visualizations, and findings.
README.md: This file.
Tools Used
Python: Pandas, NumPy, Matplotlib, Seaborn.
Environment: Jupyter Notebook.

How to Run
Clone the repository:
git clone https://github.com/your-username/heart-disease-analysis.git

Install dependencies:
pip install -r requirements.txt
Open analysis.ipynb in Jupyter Notebook and run the cells.

Future Improvements
Add statistical tests (e.g., t-tests, chi-square) to quantify relationships.
Include more visualizations (e.g., correlation heatmaps, pair plots).
Build a predictive model (e.g., logistic regression, random forest) to classify heart disease.

Contact
For questions or collaboration, reach out via GitHub Issues or email at assem.ayman.refaat@gmail.com


