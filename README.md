# Machine-Learning-Projects
# Data Analysis and Modeling Project

This repository contains Python code for two main data analysis tasks:
1. **Classification** – Predicting the survival status of passengers using Decision Tree and K-Nearest Neighbors (KNN) classifiers.
2. **Regression** – Predicting life expectancy using Linear Regression, Ridge Regression, and a custom implementation of a Random Forest Regressor.

The code is organized into interactive cells (denoted by `# %%`) and can be executed in an environment such as Jupyter Notebook or Visual Studio Code.

---

## Overview

The project demonstrates end-to-end data processing, model training, hyperparameter tuning, and evaluation for both classification and regression problems.

- **Classification Task:**  
  - **Dataset:** `data.csv`  
  - **Target Variable:** `survived`  
  - **Preprocessing:**  
    - Removal of non-informative columns (`ID` and `name`)
    - Encoding categorical variables (e.g., converting `sex` into numerical codes)
    - Handling missing values (using median imputation for `age` and replacing other missing values with `-1`)
  - **Models:**  
    - Decision Tree Classifier (tuned over a range of tree depths and criteria)
    - K-Nearest Neighbors (KNN) Classifier (tuned for the number of neighbors from 3 to 30)
  - **Evaluation:**  
    - Accuracy, F1 score, confusion matrices, ROC curves, and AUC scores
  - **Final Model:**  
    - KNN with an optimal `n_neighbors` (found to be 11) was selected based on performance.

- **Regression Task:**  
  - **Dataset:** `data.csv`  
  - **Target Variable:** `Life expectancy`  
  - **Preprocessing:**  
    - Imputation of missing numeric values with the column mean
    - One-hot encoding for categorical variables (e.g., the `Status` column)
    - Converting other categorical columns to numerical codes and handling missing values by replacing them with `-1`
  - **Models:**  
    - Linear Regression
    - Ridge Regression
    - **Custom Random Forest Regressor:** A custom ensemble of Decision Trees built by sampling the data randomly (with replacement)
  - **Evaluation:**  
    - Root Mean Squared Error (RMSE) and Mean Absolute Error (MAE)
  - **Final Model:**  
    - The custom Random Forest model provided the best performance on the validation and test sets.

Both tasks also include processing of an evaluation dataset (`evaluation.csv`) where predictions are generated and saved in a `results.csv` file.

---


