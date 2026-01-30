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
```markdown
## Project Structure

```
project-root/
├── README.md                          # Project overview, objectives, and instructions
├── Train_data.csv                     # Training dataset with building features and claim target
├── Variable Description.csv           # Data dictionary describing all features
├── insurance_claim_prediction.ipynb   # Main Jupyter Notebook containing the full analysis pipeline
├── requirements.txt                   # Python dependencies and versions
├── models/
│   ├── best_logistic_regression_model.pkl    # Serialized tuned logistic regression model
│   ├── random_forest_model.pkl               # Serialized random forest model
│   └── scaler.pkl                            # Fitted StandardScaler for feature scaling
├── preprocessing/
│   ├── preprocessing_pipeline.py      # Reusable preprocessing and feature engineering functions
│   └── imputation_strategies.py       # Custom imputation logic for missing values
├── evaluation/
│   ├── evaluation_metrics.py          # Functions for model evaluation and comparison
│   └── visualization_plots.py         # Functions for generating evaluation visualizations
├── notebooks/
│   ├── 01_eda_exploratory_analysis.ipynb     # Detailed EDA visualizations and insights
│   └── 02_model_tuning_experiments.ipynb     # Hyperparameter tuning experiments and logs
└── outputs/
    ├── model_performance_comparison.csv      # Summary table of all model results
    ├── roc_curves.png                        # ROC curve visualizations
    └── feature_importance.png                # Feature importance plots
```

### File Descriptions

- **insurance_claim_prediction.ipynb**: Main notebook containing the complete pipeline from data loading through model evaluation.
- **models/**: Directory storing serialized trained models and preprocessing artifacts for deployment and reproducibility.
- **preprocessing/**: Reusable Python modules encapsulating data cleaning, imputation, and feature engineering logic.
- **evaluation/**: Helper functions for computing metrics and generating comparison visualizations.
- **notebooks/**: Supplementary notebooks for deep-dive EDA and hyperparameter tuning experiments.
- **outputs/**: Generated reports, visualizations, and performance summaries for stakeholder review.

This modular structure ensures reproducibility, maintainability, and ease of deployment in production environments.
```

