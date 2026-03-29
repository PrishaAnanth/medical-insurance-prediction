# Health Insurance Premium Prediction for Pricing Optimization

### Project Overview
This project focuses on predicting medical insurance charges using demographic and health-related features such as age, BMI, smoking status, and region. The goal is to build machine learning models that can estimate insurance costs accurately and help understand the key factors influencing these charges.
### Dataset Description
The dataset contains 1338 records with the following features:
- age – Age of the individual
- sex – Gender
- bmi – Body Mass Index
- children – Number of dependents
- smoker – Smoking status
- region – Residential region
- charges – Medical insurance cost (target variable)
### Data Preprocessing
- Missing values in the age column were handled using median imputation.
- Categorical variables (sex, smoker, region) were encoded using encoding.
- Features and target variable were separated.
- Dataset was split into training (80%) and testing (20%).
### Exploratory Data Analysis
- The distribution of charges was right-skewed, indicating the presence of high-cost outliers
- Smoking status showed the strongest impact on insurance charges
- BMI and age also had noticeable influence
- Correlation analysis confirmed these relationships
### Models Implemented
Three machine learning models were used:

1. Linear Regression : Used as a baseline model and Captures linear relationships.
2. Random Forest Regressor : Handles non-linear patterns and Improves accuracy using multiple decision trees.
3. Gradient Boosting Regressor : Sequentially improves errors.Achieved the best performance.
### Model Performance
- **Linear Regression** achieved an RMSE of **5798.12** and an R² score of **0.7835**.
- **Random Forest** improved the performance with an RMSE of **4574.36** and an R² score of **0.8652**.
- **Gradient Boosting** delivered the best results with the lowest RMSE of **4327.85** and the highest R² score of **0.8793**.
### Hyperparameter Tuning
Grid Search was applied to optimize the Gradient Boosting model
Best parameters:
- Learning rate: 0.05
- Max depth: 2
- Min samples split: 2
- Number of estimators: 200 <br>
Tuned Model Performance:
- RMSE: 4333.01
- R² Score: 0.8791
### Feature Importance
Feature importance analysis showed:
Smoking status is the most influential factor,
Followed by BMI and age.
Other features have relatively lower impact.
### Key Insights
Insurance costs are heavily influenced by lifestyle choices, especially smoking.
Higher BMI and age contribute to increased medical expenses.
Ensemble models outperform simple linear models.
Gradient Boosting provides the most reliable predictions.
