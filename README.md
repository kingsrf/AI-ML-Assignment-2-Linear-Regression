# AI-ML-Assignment-2-Linear-Regression

**Author:** King Sambonge

## Project Description

This project applies the principles of the Machine Learning lifecycle to predict house prices using a simple linear regression model. The goal is to load, clean, and engineer features from a real-world dataset, train a model, and evaluate its performance.

**Dataset:** King County House Price Dataset
* This is a public dataset from Kaggle containing house sale prices for King County, Washington, recorded between May 2014 and May 2015.
* **Target Variable:** `price` (the sale price of the house).

## 2. Data Cleaning & Feature Engineering

### Data Cleaning
1.  **Column Selection:** Loaded the dataset and selected three key columns: `price`, `sqft_living`, and `yr_built`.
2.  **Missing Values:** Checked for `null` values in the selected columns and dropped any rows containing them to ensure data quality.
3.  **Outlier Handling:** To prevent extreme values from skewing the simple regression model, I removed the top and bottom 1% of data points for both the `price` and `sqft_living` columns.

### Feature Engineering
1.  **Selected Feature:** `sqft_living` was chosen as the single predictor variable (`X`) for the simple linear regression model. This feature represents the total interior living space in square feet.
2.  **Engineered Feature:** A new feature, `house_age`, was created. This was calculated by subtracting the `yr_built` from `2015` (the most recent year in the dataset). While not used in the final *simple* linear model, this step fulfills the feature engineering requirement.

## 3. Final Model Evaluation

The model was trained on 80% of the cleaned data and evaluated on the remaining 20% (the test set).

* **Model:** Simple Linear Regression (`price` ~ `sqft_living`)
* **Mean Squared Error (MSE):** 45,327,322,979.62
* **R-squared ($R^2$):** 0.4275 (or 42.75%)

The $R^2$ value indicates that approximately **42.75%** of the variability in house prices (in the test set) can be explained by the `sqft_living` feature alone. The MSE is large because it is in squared-dollar units.