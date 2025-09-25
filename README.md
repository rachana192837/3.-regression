🏠 Housing Price Prediction using Regression
📌 Project Overview

This project applies Linear Regression (along with Lasso and Ridge regularization) to predict house prices from the Housing Dataset.
The workflow includes data preprocessing, model training, evaluation, and interpretation of results.

📂 Steps Implemented
1. Import and Preprocess the Dataset

Loaded the dataset from Housing.xlsx.
Encoded categorical variables (yes/no, furnishingstatus, etc.) using Label Encoding.
Defined price as the target variable (y) and the remaining columns as features (X).

2. Split Data into Train-Test Sets

Used train_test_split from sklearn.model_selection.
Train size = 80%, Test size = 20%.
Ensured reproducibility with a fixed random seed.

3. Fit Linear Regression Model

Trained a Linear Regression model using sklearn.linear_model.LinearRegression.
Also experimented with Lasso and Ridge regression to handle potential multicollinearity and feature selection.

4. Evaluate Model

Evaluation metrics were computed on the test set:
Mean Absolute Error (MAE) → Average absolute difference between predicted and actual values.
Mean Squared Error (MSE) → Squared differences, penalizing larger errors more.
R² Score → Proportion of variance in the target explained by the model.

5. Plot Regression Line & Interpret Coefficients

For visualization, plotted area vs price with a fitted regression line.
Coefficients were extracted for each feature:
Positive coefficient → Feature increases house price.
Negative coefficient → Feature decreases house price.
Example: Larger area or having a guestroom contributes positively to price, while some encoded categorical factors may reduce price.

📊 Results

Linear Regression gave a baseline model with interpretable coefficients.
Lasso Regression shrank some coefficients to zero, performing implicit feature selection.
Ridge Regression reduced coefficient variance, improving stability against multicollinearity.
