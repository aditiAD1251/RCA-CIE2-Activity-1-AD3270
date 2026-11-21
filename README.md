# Linear Regression on Ames Housing Dataset

**Course:** Regression and Classification (RCA) — CIE 2 (Activity 1)  
**Roll Number:** AD3270  
**Repository:** `RCA-CIE2-Linear-Regression-AD3270`

---

## Overview

This repository presents a simple linear regression workflow on the **Ames Housing Dataset** to predict house sale prices (`SalePrice`) from above-ground living area (`Gr Liv Area`). It covers exploratory inspection, missing-value imputation, train-test splitting, Ordinary Least Squares (OLS) model training with `scikit-learn`, and test-set evaluation.

---

## Dataset

* **Source:** [Ames Housing Dataset on Kaggle](https://www.kaggle.com/datasets/shashanknecrothapa/ames-housing-dataset)
* **Raw File:** `AmesHousing.csv`
* **Cleaned File:** `AmesHousing_Cleaned.csv`
* **Size:** 2,930 records and 82 features

---

## Methodology & Workflow

1. **Exploratory Data Analysis:** Inspected dataset shape, data types, sample rows, and summary statistics.
2. **Data Cleaning:**
   * Audited missing values (`15,749` missing entries across `27` columns) and duplicate rows (`0` duplicates).
   * Imputed missing numerical values using column medians and missing categorical values using column modes, leaving `0` missing values in `AmesHousing_Cleaned.csv`.
3. **Train-Test Split:**
   * Used `Gr Liv Area` as the predictor ($X$) and `SalePrice` as the target ($y$).
   * Split the data into an **80% training set** (2,344 samples) and a **20% test set** (586 samples) with `random_state=42`.
4. **Model Training & Evaluation:**
   * Fit a `LinearRegression` model on the training set and evaluated predictions on the held-out test set.

---

## Results

### Learned Regression Equation

$$\text{SalePrice} = 19250.56 + (106.73 \times \text{Gr Liv Area})$$

* **Intercept:** `19250.5596`
* **Slope (`Gr Liv Area`):** `106.7292`

### Test Set Performance (586 Samples)

| Metric | Value |
| :--- | :--- |
| **Mean Absolute Error (MAE)** | `41,365.51` |
| **Mean Squared Error (MSE)** | `3,821,184,066.27` |
| **Root Mean Squared Error (RMSE)** | `61,815.73` |
| **R-squared ($R^2$)** | `0.5234` |

---

## Repository Contents

* `*.ipynb` — Jupyter Notebook containing data exploration, preprocessing, model training, and evaluation
* `AmesHousing.csv` — Original dataset
* `AmesHousing_Cleaned.csv` — Preprocessed dataset with missing values imputed
* `README.md` — Project documentation

---

## Conclusion

Above-ground living area (`Gr Liv Area`) shows a clear positive linear relationship with house sale price (`SalePrice`), explaining **52.34%** of the variance ($R^2 = 0.5234$) on the test set with a slope of roughly `106.73` per square foot. At the same time, the test RMSE of `61,815.73` indicates substantial remaining error, showing that a single linear predictor cannot capture all price variation on its own and that adding more relevant housing features or exploring non-linear/regularized models would be logical next steps.
