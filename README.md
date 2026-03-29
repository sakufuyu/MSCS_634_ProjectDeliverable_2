# Project Deliverable 2

## Dataset
I used the `student-por.csv` file from the Student Performance dataset.

## Goal
The goal of this deliverable was to build regression models to predict the final grade (`G3`).

## Feature Engineering
I created a new feature called `avg_grade`, which is the average of `G1` and `G2`.

I also included categorical features by using one-hot encoding.

## Data Preparation
Before modeling, I converted numeric columns, created a new feature called `avg_grade`, and prepared numeric and categorical data using a preprocessing pipeline.
The pipeline included imputation, scaling, and one-hot encoding.

## Models
I built and compared two regression models:
- Linear Regression
- Ridge Regression

## Evaluation
I evaluated the models using:
- R-squared (R²)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)

I also used 5-fold cross-validation to check model generalization.

## Results
Both models performed well and produced very similar results. Based on both test performance and cross-validation results, Ridge Regression was selected as the best model.

### Test Set Results
- **Linear Regression**
  - R² = 0.848651
  - MSE = 1.475909
  - RMSE = 1.214870

- **Ridge Regression**
  - R² = 0.848736
  - MSE = 1.475086
  - RMSE = 1.214531

### Cross-Validation Results
- **Linear Regression**
  - Mean R² = 0.793911
  - Std R² = 0.042593

- **Ridge Regression**
  - Mean R² = 0.794420
  - Std R² = 0.042912

## Main Findings
Both models were able to predict final grade well.

Ridge Regression performed slightly better than Linear Regression, but the difference was small.

This suggests that earlier grades and student-related features are useful for predicting final academic performance.

## Challenges
One challenge was preparing both numeric and categorical features in the same modeling process.

I solved this by using a preprocessing pipeline with imputation, scaling, and one-hot encoding.