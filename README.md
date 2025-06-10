# Fraud Detection

A credit card fraud detection system optimized for highly imbalanced data, using SMOTE, Logistic Regression, and XGBoost, with performance tuned for recall and ROC-AUC.

## Features

- Loads, preprocesses and cleans the [Credit Card Fraud Detection Dataset](https://storage.googleapis.com/download.tensorflow.org/data/creditcard.csv)
- Uses SMOTE to oversample the minority fraud class
- Trains a baseline Logistic Regression model
- Trains an XGBoost model with tuned hyperparameters
- Optimizes for recall and ROC-AUC to catch fraudulent transactions
- Evaluates models with classification report and ROC curve

## Why This Problem Is Tricky

- The dataset is heavily imbalanced: only ~0.17% of transactions are fraud.
- Optimizing for accuracy leads to models that predict everything as non-fraud.
- High recall is essential. Missing fraud is costlier than false alarms.
- I implemented oversampling, class weighting, and threshold adjustments to build a more realistic detection system.

## Results

| Metric              | Logistic Regression | XGBoost   |
|---------------------|---------------------|-----------|
| ROC-AUC             | 0.95+               | 0.9771    |
| Recall              | 0.65                | 0.86      |
| Precision           | 0.83                | 0.60      |
| F1-score            | 0.73                | 0.71      |

Logistic Regression is surprisingly decent as a baseline, but XGBoost offers better recall and AUC, which is more important in fraud systems.
