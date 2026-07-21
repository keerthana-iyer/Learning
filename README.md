# Medical Insurance Charges Prediction using Multiple Linear Regression


## Project Overview

This project develops a Multiple Linear Regression model to predict individual medical insurance charges based on demographic and lifestyle factors. The project follows a complete machine learning workflow, including data cleaning, exploratory data analysis, statistical hypothesis testing, feature engineering, model building, model evaluation, and regression diagnostics.

The objective is not only to build a predictive model but also to understand the factors influencing medical insurance costs.

---

## Dataset

The dataset contains information about insurance beneficiaries with the following features:

| Feature | Description |
|---------|-------------|
| age | Age of the beneficiary |
| sex | Gender |
| bmi | Body Mass Index |
| children | Number of dependent children |
| smoker | Smoking status |
| region | Residential region |
| charges | Medical insurance charges (Target Variable) |

---

## Project Workflow

### 1. Data Cleaning
- Checked dataset dimensions and data types
- Verified missing values
- Removed duplicate records
- Examined categorical variable distributions

---

### 2. Exploratory Data Analysis
- Summary statistics
- Distribution analysis
- Boxplots
- Histograms with KDE
- Q-Q plots

---

### 3. Statistical Hypothesis Testing

#### Smoking vs Insurance Charges
- Shapiro-Wilk Test (Normality)
- Levene's Test (Equal Variance)
- Independent Two-Sample t-Test

#### Regional Differences
- Shapiro-Wilk Test
- Levene's Test
- One-Way ANOVA

Results showed that smokers incur significantly higher insurance charges, while no statistically significant difference was observed across regions.

---

### 4. Feature Engineering

Categorical variables were encoded before model training.

- Binary Encoding
  - sex
  - smoker

- One-Hot Encoding
  - region (drop_first=True)

---

### 5. Train-Test Split

The dataset was split into training and testing sets to evaluate the model on unseen data and reduce the risk of overfitting.

---

### 6. Model Building

A Multiple Linear Regression model was trained using the processed dataset.

---

## Model Evaluation

| Metric | Value |
|--------|-------|
| MAE | 4177.05 |
| MSE | 35478020.68 |
| RMSE | 5956.34 |
| R² Score | 0.8069 |

The model explains approximately **81% of the variability** in medical insurance charges.

---

## Feature Importance

The learned regression coefficients indicate:

- Smoking status is the strongest predictor of insurance charges.
- BMI and Age positively influence insurance costs.
- Regional effects are relatively small after accounting for other variables.

---

## Regression Diagnostics

The following assumptions were evaluated:

- Residual Normality
- Homoscedasticity
- Residual Distribution
- Multicollinearity (Variance Inflation Factor)

Most variables showed acceptable VIF values. BMI and Age exhibited relatively higher VIF values but were retained because of their importance in predicting insurance charges.

Residual analysis suggested that the linear model performs reasonably well while indicating opportunities for further improvement.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Scikit-learn
- Statsmodels

---

## Key Learnings

Through this project I learned:

- Performing statistical hypothesis testing before model building
- Feature encoding techniques
- Building Multiple Linear Regression models
- Interpreting regression coefficients
- Evaluating regression models using MAE, MSE, RMSE and R²
- Diagnosing regression assumptions using residual analysis and VIF
- Understanding the difference between prediction performance and model interpretability

---

## Future Improvements

- Interaction terms (e.g., BMI × Smoker)
- Polynomial Regression
- Decision Tree Regressor
- Random Forest Regressor
- Gradient Boosting / XGBoost
- Hyperparameter tuning

---

## Conclusion

The Multiple Linear Regression model provides a strong baseline for predicting medical insurance charges, achieving an R² score of approximately **0.81**. Smoking status emerged as the most influential predictor, followed by BMI and Age. While the model satisfies most practical requirements, future work can explore more flexible machine learning algorithms to capture the remaining unexplained variation.

## Personal Note

This project was built as part of my journey from Data Analyst to Data Scientist.

Instead of focusing only on writing code, I spent time understanding the statistical reasoning behind every step—from hypothesis testing and regression assumptions to interpreting coefficients and diagnosing model performance.

The goal of this project was not just to predict insurance charges, but to build intuition for how regression models work in practice.
