# Medical Insurance Cost Prediction

## Project Overview

This project explores medical insurance data to understand the factors associated with insurance charges and builds a **Linear Regression model** to predict medical insurance costs.

The project includes exploratory data analysis (EDA), data cleaning, feature engineering, feature scaling, statistical feature analysis, and model evaluation using Python and machine learning libraries.

## Dataset

The dataset contains **1,338 records and 7 columns**.

| Feature | Description |
|---|---|
| `age` | Age of the individual |
| `sex` | Gender of the individual |
| `bmi` | Body Mass Index |
| `children` | Number of children covered by the insurance |
| `smoker` | Smoking status |
| `region` | Residential region |
| `charges` | Medical insurance charges — target variable |

The `charges` column is the target variable that the model aims to predict.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- SciPy
- Jupyter Notebook

## Project Workflow

### 1. Exploratory Data Analysis (EDA)

The dataset is explored to understand its structure, distributions, and relationships.

- Inspected the dataset using `head()`, `tail()`, `shape`, `info()`, and `describe()`.
- Checked for missing values and duplicate records.
- Analyzed numerical feature distributions using histograms.
- Examined categorical feature counts.
- Used box plots to inspect numerical feature distributions and potential outliers.
- Created a correlation heatmap to examine relationships between numerical variables.

### 2. Data Cleaning and Preprocessing

- Created a copy of the original dataset for preprocessing.
- Removed duplicate records.
- Encoded gender and smoking status as numerical variables.
- Converted the region column into dummy variables using one-hot encoding.
- Renamed the encoded columns to `is_female` and `is_smoker`.

### 3. Feature Engineering

- Created BMI categories using the following ranges:
  - Underweight
  - Normal
  - Overweight
  - Obese
- Converted the BMI categories into dummy variables.
- Examined feature relationships with insurance charges using Pearson correlation.
- Applied chi-square tests to investigate associations between categorical features and categorized insurance charges.
- Selected a subset of features for model training.

### 4. Feature Scaling

Used `StandardScaler` to scale the following numerical features:

- `age`
- `bmi`
- `children`

### 5. Model Training

A Linear Regression model was developed using Scikit-learn.

- Separated the input features (`X`) from the target variable (`y`).
- Split the data into training and testing sets using an 80:20 ratio.
- Used `random_state=42` for reproducibility.
- Trained the model using the selected features to predict insurance charges.

### 6. Model Evaluation

The model's performance was evaluated using:

- **R² Score:** Measures the proportion of variance in insurance charges explained by the model.
- **Adjusted R² Score:** Adjusts the R² score based on the number of predictors and observations.

*This project is intended for educational purposes. Predictions from the model should not be treated as official insurance quotes or financial advice.*

