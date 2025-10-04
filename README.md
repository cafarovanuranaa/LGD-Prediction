# LGD Prediction using Linear Regression

This project focuses on predicting Loss Given Default (LGD) using a Linear Regression model built with Python.
It shows a full end-to-end data science workflow, including data preprocessing, feature engineering, scaling, model training, and evaluation.

---

## Project Overview

Loss Given Default (LGD) represents the percentage of exposure that is lost when a borrower defaults on a loan.
Accurate LGD prediction is important for financial institutions to estimate expected credit losses and manage capital efficiently.

---

## Workflow Summary

This notebook includes the main steps of a credit risk modeling process:

1. Exploratory Data Analysis (EDA)
- Checked the dataset structure and data types.
- Generated summary statistics using `describe()`.
- Visualized outliers and distributions using boxplots.


2. Data Cleaning and Outlier Treatment
- Detected and capped outliers using the Interquartile Range (IQR) method.
- Re-visualized numerical variables after treatment to confirm stability.

3. Feature Engineering
- Created aggregated statistical features to capture group-level patterns:
  - Income_mean_by_Region
  - Previous_Defaults_mean_by_Credit_Score
- Combined these features with original predictors to improve model performance.

4. Data Transformation and Scaling
- Converted categorical variables (like Region, Gender, etc.) to numeric format using one-hot or label encoding.
- Applied StandardScaler to standardize numeric features so all predictors are on a comparable scale.

5. Normality and Correlation Analysis
- Tested the normality of continuous variables using the Kolmogorov–Smirnov (K–S) test.
- Used Spearman correlation to check monotonic relationships between predictors and the LGD target.

6. Model Training
- Split the data into training and testing sets.
- Trained a Linear Regression model:

7. Model Evaluation and Deployment
- Evaluated the model performance on the test set using metrics such as MSE, RMSE, and R² score.
- Analyzed results to understand model performance.
- Deployed the trained Linear Regression model to generate LGD predictions on new data.

