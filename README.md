# AINOW-Capstone-Project

# Insurance Building Claim Prediction Model


## Problem Statement

Insurance companies face the challenge of accurately predicting claim likelihood for individual buildings to optimize pricing, capital allocation, and risk management. This project builds a data-driven solution that estimates claim probability using available building and policy features, addressing class imbalance, missing data, and the need for interpretable, calibrated predictions.

## Key Features

- **Comprehensive Data Cleaning**: Handling missing values, type conversions, and malformed entries (e.g., non-numeric tokens in 'NumberOfWindows')
- **Exploratory Data Analysis (EDA)**: Distributions, correlations, target-wise comparisons, and cardinality analysis
- **Feature Engineering**: One-hot encoding of categorical variables, standardization of numeric features, and removal of high-cardinality identifiers
- **Class Imbalance Handling**: SMOTE (Synthetic Minority Over-sampling Technique) applied to training data
- **Multiple Models**: Logistic Regression (interpretable baseline) and Random Forest (non-linear baseline)
- **Hyperparameter Tuning**: GridSearchCV with cross-validation for optimal model performance
- **Comprehensive Evaluation**: Accuracy, precision, recall, F1-score, AUC-ROC, and calibration metrics
- **Reproducibility**: Fixed random states, saved preprocessing pipeline, and clear documentation

## Dataset

- **File**: `Train_data.csv` (~7k rows)
- **Features**: Mixed numeric and categorical building and policy attributes
- **Target**: `Claim` (binary: 1 = at least one claim, 0 = no claim)
- **Supplement**: `Variable Description.csv` (feature definitions)
- **Challenges**: Missing values, class imbalance, malformed entries, and high-cardinality identifiers

## Project Structure
