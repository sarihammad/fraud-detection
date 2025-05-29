# Fraud Detection

A credit card fraud detection system optimized for imbalanced data.

## Features

- Loads and preprocesses the [Credit Card Fraud Detection Dataset](https://storage.googleapis.com/download.tensorflow.org/data/creditcard.csv)
- Uses SMOTE to oversample the minority fraud class
- Trains a baseline Logistic Regression model
- Trains an XGBoost model with tuned hyperparameters
- Optimizes for recall and ROC-AUC to catch fraudulent transactions
- Evaluates models with classification report and ROC curve
