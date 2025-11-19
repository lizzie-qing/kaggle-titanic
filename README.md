# kaggle-titanic
Titanic Survival Prediction — Kaggle Machine Learning Project

# Overview

This project is part of the Kaggle “Titanic: Machine Learning from Disaster” competition.
The goal is to build a machine learning model that predicts whether a passenger survived the Titanic shipwreck.

This notebook follows a clean and professional Data Science workflow, suitable for both Kaggle and job-hunting portfolio use.

# Objectives

Perform exploratory data analysis (EDA)
Engineer meaningful features (Title, FamilySize, CabinLetter…)
Build several ML models (Logistic Regression, Random Forest, XGBoost)
Compare model performance using accuracy & AUC
Generate a final submission file for Kaggle

# Project Workflow
### 1. Data Overview

We start by inspecting dataset structure and missing values:

View columns and dtypes

Describe numerical features

Check missing value percentages

Visualize missing pattern with heatmaps

### 2. Exploratory Data Analysis (EDA)

Key visualizations include:

Age distribution

Fare distribution

Survival rate by Sex

Survival rate by Pclass

KDE plot of Age vs Survival

Correlation heatmap

### Key findings:

Females have a much higher survival rate

1st-class passengers survived more

Younger children had higher survival probabilities

# 3. Feature Engineering

To improve model performance, several additional features were created.

### Sex Encoding
male → 0, female → 1
### Embarked Encoding
S → 0, C → 1, Q → 2
### Title Extraction
Extracted from passenger names:
Mr, Mrs, Miss, Master, Other
### Family Features
FamilySize = SibSp + Parch + 1
IsAlone = 1 if FamilySize == 1 else 0
### Ticket Group Size
Number of passengers sharing the same ticket.
### Cabin Letter Extraction
Cabin block A–G encoded as integers.
### Missing Value Handling
Age → median
Fare → median
Embarked → mode

Final feature list included 12 engineered variables.

# 4.Model Training & Validation

### Split:
Train: 80%
Validation: 20% (stratified by Survived)
### Models compared:
Logistic Regression
Random Forest
XGBoost
### Evaluation metrics:
Accuracy
ROC–AUC

# 5. Final Submission

The full training set was used to fit the final Logistic Regression model.
Predictions on test.csv were saved as:
```
submission.csv
```
# Kaggle Score
Public Score: 0.77511

# Tech Stack

Python
Pandas / NumPy
Seaborn / Matplotlib
Scikit-Learn
XGBoost



