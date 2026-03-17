# Bank-Customer-Churn-Analysis
This project explores the drivers of customer churn at a fictional bank using exploratory data analysis and machine learning. The goal is to identify key factors that predict whether a customer will leave the bank and quantify their relative importance.

The data set used for this analysis and modeling exercise was obtained from [Kaggle](https://www.kaggle.com/datasets/gauravtopre/bank-customer-churn-dataset) and comprises customer details for Bank ABC. **Fields include:**

- Customer ID - Unique identifier assigned to bank customer
- Credit Score - The customer's credit score
- Country - The customer's country of residence
- Gender - The customer's gender
- Age - The customer's age
- Tenure - Number of years the customer has been with the bank
- Balance - The customer's bank account balance at the time of data collection
- Products Number - The number of bank products the customer is subscribed to
- Credit Card - Whether the customer has a credit card with the bank (Y/N)
- Active Member - Whether the customer is an active account member (bank product use, account login frequency, transaction activity, etc.) (Y/N)
- Estimated Salary - The customer's estimated salary at the time of data collection
- Churn - The primary variable of interest; indicates whether the customer has left the bank (Y/N)

**Data Analysis Approach:** Python (Pandas) was used for cleaning and initial EDA (Distribution of means & data spread, univariate and multivariate comparisons to churn, correlation heat maps, and chi squared & t-tests). Random forest modeling was used to assess feature importance, predict the likelihood of customer churn, and identify conditions that increase churn risk.

**Findngs:** The tuned Random Forest, evaluated at the F₂-optimal classification threshold, correctly identifies 83% of customers who churn (sensitivity = 0.831), with a cross-validated ROC AUC of 0.860. Key drivers of churn were:

- Age — risk increases substantially after 40, with customers in their late 40s to early 60s at highest risk
- Number of products — customers with 3 or 4 bank products are at considerably higher risk than those with 1 or 2, a non-linear effect not captured by linear correlation
- Membership activity — non-active members show substantially higher churn probability than active members, with the PDP confirming a clear step change between the two groups
- Geography & gender — German customers churn at a meaningfully higher rate than French or Spanish customers (Cramér's V = 0.17); female customers churn at a modestly higher rate than male customers (point-biserial r = −0.11)

Retention efforts should be prioritised for customers aged 45–65 who hold 3 or more products and show signs of membership disengagement. German customers, particularly older female customers, represent a high-risk geographic segment warranting targeted intervention.
