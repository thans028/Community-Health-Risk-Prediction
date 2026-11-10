# Community Health Risk Prediction

## Project Overview

This project uses Python and CDC PLACES 2025 county-level data to explore relationships between community health indicators and diabetes prevalence.

I developed a Linear Regression model to estimate county-level diabetes prevalence using health indicators such as obesity, smoking, physical inactivity, high blood pressure, coronary heart disease, and stroke.

The goal was to explore how public health indicators can be used in data analysis and predictive modeling.

## Tools and Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- Jupyter Notebook
- CDC PLACES 2025 Data

## Dataset

- Source: CDC PLACES 2025 County Data
- Original dataset: 3,143 county records
- Records after removing missing values: 2,956
- Target variable: Diabetes prevalence (`DIABETES_CrudePrev`)

## Methodology

### 1. Data Preparation

- Imported the CDC PLACES county-level dataset using Pandas.
- Examined dataset dimensions, column names, data types, and summary statistics.
- Selected diabetes prevalence as the target variable.
- Selected seven health and population indicators as predictor variables.
- Removed records containing missing values from the selected variables.
- Converted population values into numeric format.

### 2. Feature Selection

**Target variable:**
- Diabetes prevalence

**Predictor variables:**
- Obesity prevalence
- Smoking prevalence
- Physical inactivity prevalence
- High blood pressure prevalence
- Coronary heart disease prevalence
- Stroke prevalence
- Total population

### 3. Model Development

- Algorithm: Linear Regression
- Training data: 80%
- Testing data: 20%
- Random state: 42

The model was trained using Scikit-learn and evaluated using a separate testing dataset.

## Model Evaluation Results

| Evaluation Metric | Actual Result |
|---|---:|
| Mean Absolute Error (MAE) | 0.600 |
| Root Mean Squared Error (RMSE) | 0.771 |
| R-squared (R²) | 0.925 |

### Results Interpretation

- **MAE (0.600):** The model's predictions differed from actual diabetes prevalence by approximately 0.60 percentage points on average.
- **RMSE (0.771):** The model's root mean squared prediction error was approximately 0.77 percentage points.
- **R² (0.925):** The model explained approximately 92.5% of the variation in diabetes prevalence in the test dataset.

These results describe performance on the notebook's random holdout test set.

## Key Findings

1. The model achieved an R² of 0.925 on the test dataset, showing a strong fit within this evaluation.
2. The average absolute prediction error was approximately 0.60 percentage points.
3. Community health indicators, including obesity, smoking, physical inactivity, high blood pressure, heart disease, and stroke prevalence, were used together to estimate county-level diabetes prevalence.

## Python Notebook

[View the Python notebook](community_health_risk_prediction.ipynb)

The notebook contains the data preparation, feature selection, model training, predictions, and evaluation calculations.

## Limitations

- The analysis uses county-level data, not individual patient records.
- The model estimates community-level diabetes prevalence; it does not predict an individual's diabetes risk.
- The random train/test split does not establish how well the model generalizes to entirely new geographic regions or future years.
- Relationships between health indicators do not establish causation.
- Further validation, including geographic or external testing, would be needed before considering practical public health applications.

## Project Takeaway

This project strengthened my skills in Python, data preparation, exploratory analysis, and machine learning. It helped me explore how public health data can be used to examine community health patterns and develop predictive models.
