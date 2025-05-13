# ChurnClassifier – Bank Customer Churn Prediction

## Overview
**ChurnClassifier** is a machine learning-based classification system designed to predict customer churn in a banking context. The goal is to identify customers who are likely to exit the bank and enable proactive retention strategies based on data-driven insights.

## Objectives
- Preprocess and encode customer data
- Train and evaluate multiple classification models
- Select the best-performing model based on F1 and ROC AUC scores
- Generate predictions for unseen customer data

## Dataset
- **Train file**: `train.csv`
- **Test file**: `test.csv`
- **Target**: `Exited` (1 = customer left, 0 = customer stayed)
- **Notable features**:
  - Gender
  - Geography
  - Credit Score, Balance, Estimated Salary
  - Tenure, Number of Products
  - Active Member, Age

## Key Components

### 1. Data Preprocessing
- Encoded categorical features (`Gender`, `Geography`) using **LabelEncoder**
- Removed irrelevant fields: `id`, `CustomerId`, `Surname`
- Standardized numerical features using **StandardScaler**

### 2. Model Training and Evaluation
Trained and tested the following models using F1 Score and ROC AUC:
- Logistic Regression
- Decision Tree
- **Random Forest** (best-performing)

### 3. Test Set Prediction
- Preprocessed test dataset similarly
- Used the trained **Random Forest** model to predict `Exited` status
- Saved predictions in `results.csv` for submission

## Technologies Used
- Python
- pandas, numpy
- scikit-learn

## Results
- **Random Forest** achieved the best F1 and ROC AUC scores
- Final predictions exported for deployment or submission
