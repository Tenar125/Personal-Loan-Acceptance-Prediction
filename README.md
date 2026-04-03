# Personal-Loan-Acceptance-Prediction
Project Overview

This project aims to predict which customers are likely to accept a personal loan offer based on their demographics, financial behavior, and prior interactions. By identifying patterns in customer behavior, banks and financial institutions can design targeted campaigns to improve loan acceptance rates and optimize marketing strategies.

Objectives

Analyze customer demographics and financial behaviors.

Explore correlations between income, education, and loan acceptance.

Identify key factors influencing customer decisions.

Build and compare multiple classification models to find the most accurate predictor

Dataset

The dataset contains various customer attributes including:

Numerical Columns: Age, Balance, Day, Duration

Categorical Columns: Job, Marital Status, Education, Contact Type, Housing Loan, Personal Loan, Default Status

Observations:

There are no missing values, making the dataset clean for analysis.

Most insights are driven by categorical data rather than numerical statistics.

Data Exploration & Insights

1. Numeric Data Distribution
2. 
Numeric features such as age, balance, day, and call duration were visualized using histograms.

A new feature, duration_min, was created by converting call duration into minutes for better readability.

Observation: Most customers who accepted the deposit offer had longer call durations. One notable outlier did not accept 

despite a long call, indicating exceptions exist.

2. Balance vs Loan Acceptance

Customers with balances between 40,000–60,000 are more likely to accept a deposit offer. 

High-balance outliers also accepted loans, while most customers rejecting the loan had balances below 40,000.

3. Job & Success Rate
4. 
Top 5 jobs by loan acceptance:

Students

Retired Individuals

Others (varies by dataset)

Observation: Students and retired individuals are more likely to respond positively to loan offers. Targeted campaigns toward 

these groups could improve conversion rates.
4. Marital Status & Loan
Married individuals show higher loan acceptance rates.

Observation: Marital status may correlate with financial stability, making married individuals more likely to accept loan offers.

5. Feature Engineering

age_category: Categorized as Youth (18–24), Adult (25–35), Middle Age (36–49), Senior (50+)

overdraft: Flag for negative balance (1 if balance < 0)

loan_numeric: Converted target variable to numeric (1 if loan = "yes", 0 otherwise)
Model Building

Two classification models were trained to predict loan acceptance:

1. Logistic Regression

Accuracy: 87.6%

Confusion matrix shows strong prediction for “no” responses but poor prediction for “yes”.

Recall for “yes”: 0.03 (very low)

Precision for “yes”: 0.43

3. Decision Tree Classifier

Accuracy: Slightly lower or comparable to logistic regression

Similar confusion issues due to imbalanced classes

Observation:

The models show high overall accuracy because the majority of customers reject the loan. However, they struggle to correctly 
predict the minority class (loan acceptance), highlighting the effect of class imbalance.

Key Takeaways

Longer call duration increases the likelihood of loan acceptance.

Higher account balances correlate with higher acceptance rates.

Students and retired individuals are prime targets for loan campaigns.

Married customers are slightly more likely to accept a loan.

Imbalanced dataset requires techniques such as oversampling, undersampling, or using algorithms robust to imbalance to 
improve “yes” prediction.

<img width="695" height="488" alt="image" src="https://github.com/user-attachments/assets/22d38d1f-b6a2-432f-a97f-e5da2e4df121" />

<img width="555" height="448" alt="image" src="https://github.com/user-attachments/assets/5d033c28-6a9c-40ed-b5d2-64d78f6d23a9" />

