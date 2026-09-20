# House Prices Regression

## Project Overview

This project focuses on predicting house prices using the **House Prices: Advanced Regression Techniques** dataset from Kaggle.

The project covers the complete machine learning workflow, starting from **Exploratory Data Analysis (EDA)** and data preprocessing, then building and evaluating regression models.

## Dataset

The dataset is from the Kaggle House Prices competition:

**House Prices: Advanced Regression Techniques**

The dataset contains information about residential properties, including features related to:

* House quality
* Living area
* Garage
* Basement
* Neighborhood
* Bathrooms
* Year built
* Sale price

The target variable is:

`SalePrice`

## Project Workflow

### 1. Exploratory Data Analysis (EDA)

The dataset was explored to understand its structure and identify important relationships.

Main steps included:

* Checking dataset shape and information
* Descriptive statistics
* Checking duplicated rows
* Analyzing the distribution of `SalePrice`
* Studying relationships between important features and `SalePrice`
* Correlation analysis
* Correlation heatmap
* Analyzing categorical features
* Neighborhood price analysis
* Outlier detection

### 2. Data Cleaning

Missing values were handled according to the meaning of each feature.

Different strategies were used, including:

* Filling categorical missing values with `"None"` when the missing value represents the absence of a feature
* Filling numerical missing values with appropriate values such as `0` or the median
* Filling `Electrical` using its mode
* Filling `LotFrontage` using the median value within each neighborhood

After preprocessing:

**Total missing values = 0**

### 3. Outlier Treatment

Numerical outliers were investigated using the **IQR method**.

Extreme observations in `GrLivArea` were further investigated.

Two observations with extremely large living areas and unusually low sale prices were removed because they could strongly affect the regression model.

### 4. Feature Engineering

Three additional features were created:

* `TotalSF` — total square footage
* `TotalBathrooms` — weighted total number of bathrooms
* `TotalPorchSF` — total porch area

These features were created to represent combined aspects of the house more clearly.

### 5. Data Preprocessing

The dataset contains both numerical and categorical variables.

The preprocessing steps included:

* Removing the `Id` identifier
* Separating features and target
* Train-test split
* One-Hot Encoding for categorical variables
* Standard Scaling for numerical variables

`handle
