# ADANIPORTS Stock Price Prediction Using Regression

## Project Overview

This project focuses on analyzing historical **ADANIPORTS stock market data** and predicting the **Closing Price** using regression techniques.

The project follows a complete machine learning workflow, starting from data cleaning and exploratory data analysis (EDA) to feature selection, model building, and evaluation.

## Objectives

* Analyze historical stock price trends
* Understand relationships between different stock features
* Perform data cleaning and preprocessing
* Identify suitable features for predicting the closing price
* Build and compare regression models
* Evaluate model performance using standard regression metrics

## Dataset

The dataset contains historical stock market data for **ADANIPORTS**.

After data cleaning:

* **Rows:** 3,322
* **Columns:** 14
* **Target Variable:** `Close`

### Features Used

The following features were selected for prediction:

* `Prev_Close`
* `Open`
* `High`
* `Low`
* `Last`

**Target:**

* `Close`

## Data Preprocessing

The following preprocessing steps were performed:

* Standardized column names
* Converted the `Date` column into the appropriate date format
* Checked for missing values
* Filled missing values in the `Trades` column using the median
* Checked for duplicate records
* Removed the `Series` column
* Selected relevant features for modeling

The `Trades` column contained **866 missing values (26.07%)**, which were handled using median imputation.

## Exploratory Data Analysis

The project includes several EDA techniques to understand the dataset:

* Closing price trend analysis
* Daily return analysis
* Correlation analysis
* Moving average analysis
* Volume trend analysis
* Rolling volatility analysis
* Outlier analysis
* Open vs Close price relationship

These visualizations helped understand the behavior and relationships within the stock data before building the models.

## Machine Learning Models

Two regression models were implemented and compared.

### 1. Multiple Linear Regression

Multiple Linear Regression was used to predict `Close` using:

`Prev_Close`, `Open`, `High`, `Low`, and `Last`.

**Performance:**

* **MAE:** 0.8906
* **MSE:** 2.4378
* **RMSE:** 1.5613
* **R²:** ~99.99%

### 2. Polynomial Regression

Polynomial Regression with degree 2 was also implemented to investigate whether a non-linear relationship could improve the prediction.

**Performance:**

* **MAE:** 0.9060
* **MSE:** 2.4306
* **RMSE:** 1.5590
* **R²:** ~99.99%

## Model Comparison

| Model                      |    MAE |    MSE |   RMSE |      R² |
| -------------------------- | -----: | -----: | -----: | ------: |
| Multiple Linear Regression | 0.8906 | 2.4378 | 1.5613 | ~99.99% |
| Polynomial Regression      | 0.9060 | 2.4306 | 1.5590 | ~99.99% |

Both models produced very similar results.

Polynomial Regression achieved slightly lower MSE and RMSE, while Multiple Linear Regression achieved a lower MAE.

Since the difference in performance was very small, **Multiple Linear Regression was selected as the preferred model** because of its simpler structure and easier interpretation.

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

## Project Workflow

```text
Raw Stock Data
      ↓
Data Cleaning
      ↓
Data Preprocessing
      ↓
Exploratory Data Analysis
      ↓
Feature Selection
      ↓
Train-Test Split
      ↓
Regression Models
      ↓
Model Evaluation
      ↓
Model Comparison
      ↓
Final Model Selection
```

## Project Structure

```text
ADANIPORTS-Stock-Price-Prediction/
│
├── Project_Regression.ipynb
├── README.md
└── dataset/
    └── ADANIPORTS.csv
```

## Key Takeaways

* Historical stock features showed strong relationships with the closing price.
* Both Multiple Linear Regression and Polynomial Regression performed very well on the test data.
* The performance difference between the two models was minimal.
* Multiple Linear Regression was selected because it provides comparable performance with a simpler model structure.
* The project provided practical experience with the complete regression workflow using Scikit-learn.

## Disclaimer

This project is created for **educational and machine learning practice purposes**. The predictions should not be considered financial or investment advice.
