# Medical-Insurance-Cost-Prediction

This project focuses on predicting medical costs using machine learning techniques based on patient demographics and health-related factors. The dataset includes features such as age, sex, BMI, number of children, smoking status, region, and medical costs.

## Objectives

1. **To explore the dataset** and understand the underlying patterns and distributions of variables.
2. **To study correlations** between predictors (e.g., smoking status, BMI, age) and medical costs.
3. **To identify the most significant predictors** influencing medical costs.
4. **To build regression models** (simple and multivariate) to predict medical costs based on selected predictors.
5. **To evaluate and compare the performance** of models using statistical measures.
6. **To provide actionable insights** for insurance companies regarding the key factors driving medical costs.

## Data Cleaning

- **Missing Values:** The dataset contained no missing values across all columns.
- **Duplicate Records:** One duplicate row was identified and removed, reducing the dataset to 1337 rows.
- **Data Types:** Data types were validated to ensure proper handling during analysis. Categorical variables (e.g., sex, smoker, and region) were retained as objects for initial exploration and later encoded for modeling.

## Data Exploration

- **Age:** Average age is 39.22 years, with a symmetric distribution.
- **BMI:** Average BMI is 30.66, indicating a tendency toward overweight.
- **Children:** Most families have 0-1 children.
- **Medical Costs:** Positively skewed, with an average cost of $13,279.12.
- **Categorical Variables:** Balanced gender distribution; 20.5% of the individuals are smokers, and the Southeast region has the highest proportion of payees.

## Correlation Analysis

- **Strong Positive Correlation:** Smoking status (0.79) with medical costs.
- **Moderate Positive Correlation:** Age (0.3) and BMI (0.2).
- **Negligible Correlation:** Number of children (0.068) and sex (0.057).

## Simple Linear Regression

Models were built for the top three predictors:

- **Smoking Status:** R² = 0.620. Smoking increases medical costs by $23,620 on average.
- **Age:** R² = 0.089. Each additional year adds $258 to costs.
- **BMI:** R² = 0.039. Each BMI unit adds $394 to costs.

## Multivariate Regression

1. **Model 1 (Three Predictors - Smoking, Age, BMI):**
   - R² = 0.7777, MSE = 34,512,843.88.
   - Smoking contributed most significantly, followed by BMI and age.

2. **Model 2 (All Predictors):**
   - R² = 0.1618, MSE = 130,132,666.29.
   - Lower performance likely due to overfitting and multicollinearity.

**Comparison:** Model 1 outperformed Model 2, indicating that including only significant predictors improves accuracy and efficiency.

## Conclusion

The analysis highlights smoking status, age, and BMI as the most critical factors affecting medical costs. A focused model using these predictors achieved an R² of 0.7777, significantly higher than the model incorporating all predictors. This study emphasizes the importance of feature selection in regression modeling, as additional predictors may introduce noise and reduce performance.

### Recommendations

1. **For Insurers:** Consider smoking status as a primary factor when assessing premiums.
2. **For Future Analysis:** Regularization techniques can help address overfitting in models with all predictors.

## Tools and Techniques Used

- **Python Libraries:**
  - `pandas` and `numpy` for data cleaning, manipulation, and analysis.
  - `matplotlib` and `seaborn` for data visualization.
  - `scikit-learn` for building machine learning models.
  - `statsmodels` for statistical analysis and regression modeling.
- **Data Cleaning:**
  - Handling duplicates and validating data types.
- **Exploratory Data Analysis (EDA):**
  - Descriptive statistics and visualizations to understand data distributions.
  - Correlation analysis to identify relationships between predictors and medical costs.
- **Machine Learning Models:**
  - Simple linear regression for univariate analysis.
  - Multivariate regression to evaluate the combined effect of multiple predictors.
- **Performance Evaluation:**
  - Metrics like R-squared and Mean Squared Error (MSE) to assess model accuracy.
  
## How to Use This Repository

1. **Dataset:** Include the `insurance.csv` dataset in the root directory.
2. **Run the Analysis:** Use the Python scripts or Jupyter notebooks provided to reproduce the results.
3. **Dependencies:** Ensure the required Python libraries are installed (e.g., pandas, numpy, seaborn, scikit-learn, statsmodels).

## Acknowledgments

This project was completed as part of the CT7205 Machine Learning and Optimisation module at the University of Gloucestershire
