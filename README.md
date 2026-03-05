# BigMart Sales Prediction

## Overview
This project builds a machine learning model to predict product sales at different BigMart outlets. The objective is to understand how product attributes, store characteristics, and pricing factors influence sales, and to develop a model that can accurately estimate item-level sales.

The project follows a complete machine learning workflow including data preprocessing, feature engineering, model training, hyperparameter tuning, and model evaluation.

---

## Problem Statement
Retail businesses often need accurate demand predictions to optimize inventory planning, pricing strategies, and store operations.

The goal of this project is to:
- Predict **item outlet sales**
- Identify key drivers of product sales
- Compare multiple machine learning models
- Select the model that generalizes best to unseen data

---

## Dataset
The dataset used in this project is sourced from Kaggle:

**BigMart Sales Prediction Dataset**  
https://www.kaggle.com/datasets/shivan118/big-mart-sales-prediction-datasets

The dataset contains information about:
- Product characteristics (type, weight, fat content)
- Pricing information (MRP)
- Product visibility in stores
- Store attributes (size, location type, outlet type)
- Historical item-level sales

The dataset is not included in this repository and must be downloaded directly from Kaggle.

---

## Approach

### Data Preparation
The dataset is cleaned and transformed before modeling. Categorical variables are encoded into numerical features, and several new variables are engineered to capture patterns related to store performance, product pricing, and product visibility.

### Feature Engineering
Several features are created to improve model performance, including:
- Outlet-level average sales
- Outlet–item type average sales
- Visibility ratio
- Price-per-weight
- MRP price bins
- Item category extracted from product identifier

These engineered features help capture relationships between product attributes and store behavior.

---

## Models Evaluated

### Linear Models
- Linear Regression
- Elastic Net (Baseline)
- Elastic Net (Optimized)

### Tree-Based Models
- Random Forest (Baseline)
- Random Forest (Optimized)

### Gradient Boosting
- XGBoost (Baseline)
- XGBoost (Optimized)

---

## Model Evaluation
Models are evaluated using multiple metrics to understand prediction accuracy and model generalization:

- Root Mean Squared Error 
- Mean Absolute Error 
- R-Squared Score

Performance is measured separately on **training, validation, and test datasets** to monitor overfitting and ensure reliable model comparison.

---

## Model Selection
Tree-based models outperform linear models, indicating that the relationship between product attributes and sales is nonlinear.

After hyperparameter tuning, **Random Forest (Optimized)** achieves the best validation performance and is selected as the final model.

---

## Feature Importance
Feature importance analysis from the Random Forest model shows that several variables play a significant role in predicting sales, including:

- Item MRP
- Outlet–item type average sales
- Price-per-weight
- Outlet average sales
- Product visibility ratio

These results highlight the importance of both product pricing and store-level characteristics in determining sales.

---
