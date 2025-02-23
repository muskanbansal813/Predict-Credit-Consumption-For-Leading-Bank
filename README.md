# Predict-Credit-Consumption-For-Leading-Bank
1. Introduction

Business Context

Analytics is driving every industry using various technology platforms that collect information from multiple sources. The Credit Card industry, being data-rich, can leverage this data to understand customer behavior and develop marketing campaigns that directly address consumer behaviors, ultimately increasing sales and revenue.

Business Objectives

One of the leading banks provided data that includes:

Customer demographics

Customer behavioral data (transaction history, liabilities, assets)

Credit consumption (past and predicted)

The goal is to understand the relationship between consumer characteristics and their consumption patterns to predict credit card spending for customers with missing values in the dataset.

2. Data Description

Data Sources

The data is provided in three CSV files:

CustomerDemographics.csv

CustomerBehaviorData.csv

CreditConsumptionData.csv

Data Dictionary

CustomerDemographics.csv: Contains demographic information.

CustomerBehaviorData.csv: Contains spending and transaction history.

CreditConsumptionData.csv: Contains the target variable (cc_cons) representing average credit card spend for the next three months.

3. Data Preprocessing and Cleaning

Handling Missing Values

The primary focus is on predicting the average credit card spend (cc_cons) for the next three months.

Steps:

Separation of Data:

Customers with non-missing values for cc_cons (used for training).

Customers with missing values for cc_cons (used for prediction).

Handling Missing Values in Features:

Categorical Variables: Filled missing values using the mode (most frequent category).

Numerical Variables: Used median imputation to handle missing values.

Data Transformation

Dropped the ID column due to its uniqueness.

Applied outlier treatment using the Interquartile Range (IQR) method.

Encoded categorical variables using dummy variables.

4. Exploratory Data Analysis (EDA)

Summary statistics for numerical and categorical variables.

Data visualization:

Distribution of cc_cons (credit card spend) shows a right-skewed distribution.

Skewness value calculated: 2.12 (moderate right skew).

5. Feature Engineering

Created new aggregated features where necessary.

Selected features based on correlation analysis and domain knowledge.

6. Model Development

Problem Definition:

Predicting cc_cons (credit consumption) using Linear Regression as a regression problem.

Model Selection:

Linear Regression was chosen for its simplicity and interpretability.

Model Training:

Split the data into training and validation sets (80:20 ratio).

Trained the Linear Regression model on the training data.

Model Evaluation:

Used the Root Mean Square Percentage Error (RMSPE) metric for evaluation.

Performance metrics:

Mean Absolute Error (MAE): 76,575.96

Mean Squared Error (MSE): 10,793,541,320.37

Root Mean Squared Error (RMSE): 103,897.83

R-squared (R²): 0.72 (indicating a good fit)

7. Model Deployment & Prediction

Used the trained model to predict cc_cons for customers with missing values.

Generated a CSV file with predicted values.

8. How to Use This Repository

Prerequisites:

Ensure you have Python installed along with the required libraries:

pip install pandas numpy scikit-learn matplotlib seaborn

Steps to Run the Model:

Clone the repository:

git clone https://github.com/yourusername/credit-card-consumption-prediction.git

Navigate to the project folder:

cd credit-card-consumption-prediction

Run the preprocessing and model training script:

python model.py

The predicted values will be saved as predictions.csv.

9. Expected Outputs

Detailed code with comments (available in model.py).

Data Exploratory Analysis (EDA) results.

Model validation metrics and evaluation outputs.

Predicted values for customers with missing cc_cons values.

