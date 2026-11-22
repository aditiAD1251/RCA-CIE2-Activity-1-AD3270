# RCA CIE 2 – Activity 1: Multiple Linear Regression

## 1. Project Overview

This project is submitted for Regression and Classification Algorithms (RCA), CIE 2 – Activity 1.

The objective is to build Simple Linear Regression and Multiple Linear Regression models to predict house prices using different housing features.

**Role:** Data Scientist predicting house prices.

## 2. Dataset Information

- **Dataset Name:** Ames Housing Dataset
- **Dataset Source:** Kaggle
- **Dataset Link:** https://www.kaggle.com/datasets/shashanknecrothapa/ames-housing-dataset
- **Dataset Size:** 2,930 rows and 82 columns.

### Selected Features

**Input Features (X):**
- Gr Liv Area
- Overall Qual
- Year Built

**Target Variable (y):**
- SalePrice

## 3. Work Completed

The following tasks were performed in the notebook:

1. Importing required libraries.
2. Loading and inspecting the dataset.
3. Checking missing values and duplicates.
4. Data cleaning and preprocessing.
5. Performing Exploratory Data Analysis (EDA).
6. Creating scatter plots and a correlation heatmap.
7. Selecting important features using Pearson correlation.
8. Performing manual regression calculations using the Normal Equation.
9. Checking manual results using Scikit-learn.
10. Splitting data into training and testing sets.
11. Building Simple Linear Regression.
12. Building Multiple Linear Regression.
13. Calculating regression coefficients and intercept.
14. Evaluating models using MAE, MSE, RMSE, R² and Adjusted R².
15. Comparing both models.
16. Creating actual versus predicted plots.
17. Performing residual analysis.
18. Checking multicollinearity using VIF.
19. Predicting the price of a new house.
20. Writing conclusions and limitations.

## 4. Methodology

- **Algorithms:** Simple Linear Regression and Multiple Linear Regression.
- **Training Data:** 2,344 rows.
- **Testing Data:** 586 rows.
- **Train-Test Split:** 80:20.
- **Random State:** 42.

Manual regression calculations were performed using two features and verified using Scikit-learn.

## 5. Model Evaluation Results

The models achieved the following results on the test dataset:

| Evaluation Metric | Single-Feature Model | Multiple-Feature Model |
|---|---:|---:|
| MAE | 36,141.27 | 29,135.30 |
| MSE | 2.796 × 10⁹ | 1.957 × 10⁹ |
| RMSE | 52,878.68 | 44,242.55 |
| R² | 0.651 | 0.756 |
| Adjusted R² | 0.651 | 0.755 |

### Model Comparison

The Multiple Linear Regression model performed better than the Single Linear Regression model.

It has lower prediction errors and a higher R² score of 0.756.

This shows that using three features gives better house price predictions than using only one feature.

## 6. Regression Equation

The Multiple Linear Regression equation is:

SalePrice = -1067424.84 + 61.63(Gr Liv Area) + 25249.81(Overall Qual) + 507.93(Year Built)

The coefficients show how each feature is related to house price while keeping the other features constant.

## 7. Residual Analysis and VIF

The following graphs were created:

- Residual Plot
- Residual Histogram
- Actual vs Predicted Plot

### VIF Results

| Feature | VIF |
|---|---:|
| Gr Liv Area | 1.517 |
| Overall Qual | 2.219 |
| Year Built | 1.590 |

All VIF values are below 5, showing no serious multicollinearity among the selected features.

## 8. New House Prediction

A new house was given the following details:

- Gr Liv Area = 1436.5
- Overall Qual = 6
- Year Built = 1972

**Predicted House Price: $174,240.79**

## 9. Project Files

The repository contains:
`RCA-CIE2-ACT1.ipynb` – Complete Jupyter Notebook.
`AmesHousing.csv` – Original dataset.
`Cleaned_housing.csv` – Cleaned dataset.
`README.md` – Project description.

## 10. Technologies Used

- Python
- Google Colab / Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## 11. Conclusion

In this activity, Simple Linear Regression and Multiple Linear Regression were implemented using the Ames Housing dataset.

The models were evaluated and compared using different regression metrics.

The Multiple Linear Regression model performed better, achieving an R² score of 0.756.

This activity helped in understanding manual regression calculations, model building, prediction and model evaluation.

## 12. Limitations

- Only three features were used for prediction.
- House prices depend on many other factors.
- The model may not predict every house price accurately.
- Predictions are estimates, not guaranteed prices.

## 13. GitHub Submission Details

**Student GitHub ID:**  
https://github.com/complexiota

**Student Name:** Aditi Balasaheb Pawar

**Roll Number:** AD3270

**Class:** T.Y. B.Tech AI & DS

**Division:** B

**Academic Year:** 2026–27

---

Submitted as part of CIE 2 – Regression and Classification Algorithms.
