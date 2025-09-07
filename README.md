# Bank-Customer-Churn-Analysis
The data set used for this analysis and modeling exercise was obtained from [Kaggle](https://www.kaggle.com/datasets/gauravtopre/bank-customer-churn-dataset) and comprises customer details for Bank ABC. Fields include:

Customer ID - Unique identifier assigned to bank customer
Credit Score - The customer's credit score
Country - The customer's country of residence
Gender - The customer's gender
Age - The customer's age
Tenure - Number of years the customer has been with the bank
Balance - The customer's bank account balance at the time of data pull
Products Number - The number of bank products the customer is subscribed to
Credit Card - Whether the customer has a credit card with the bank (Y/N)
Active Member - Whether the customer is an active account member (bank product use, account login frequency, transaction activity, etc.) (Y/N)
Estimated Salary - The customer's estimated salary at the time of data pull
Churn - The main variable to interest; indicates whether the customer has left the bank (Y/N)

Data Analysis Approach: Python (Pandas) was used for cleaning and initial EDA (Distribution of means & data spread, univariate and multivariate comparisons to churn, correlation heat maps, and chi squared & t-tests). Random forest modeling was used to assess feature importance, predict the liklihood of customer churn, and identify conditionas that increase churn risk.


