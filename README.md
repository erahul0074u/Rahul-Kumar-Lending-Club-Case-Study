![image](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/43576485-f366-4621-91bf-cae14f4608e2)Problem statement:-
You work for a consumer finance company which specialises in lending various types of loans to urban customers. When the company receives a loan application, the company has to make a decision for loan approval based on the applicant’s profile. Two types of risks are associated with the bank’s decision:
If the applicant is likely to repay the loan, then not approving the loan results in a loss of business to the company
If the applicant is not likely to repay the loan, i.e. he/she is likely to default, then approving the loan may lead to a financial loss for the company.
The data given below contains information about past loan applicants and whether they ‘defaulted’ or not. The aim is to identify patterns which indicate if a person is likely to default, which may be used for taking actions such as denying the loan, reducing the amount of loan, lending (to risky applicants) at a higher interest rate, etc.
In this case study, you will use EDA to understand how consumer attributes and loan attributes influence the tendency of default.

Objective of the case study:-
**To identify the risky loan for financial company**

**Steps Followed to solve the case study:-**

1. Data Understanding
2. Data cleaning (cleaning missing values, removing redundant columns etc.)
3. Data Analysis
4. Recommendations

**1. Data Understanding:-**
Some of the important columns in the dataset are loan_amount, term, interest rate, grade, sub grade, annual income, purpose of the loan etc.The target variable, which we want to compare across the independent variables, is loan status. The strategy is to figure out compare the average default rates across various independent variables and identify the ones that affect default rate the most.

**2. Data Cleaning:-**
a. Some columns have a large number of missing values. First fixed the missing values and then checked for other types of data quality problems. Many Columns have 100% missing value, some have 65% and some have 33% missing value. 

The column description contains the comments the applicant had written while applying for the loan. Although some text analysis techniques can also be used to derive new features from this column (such as sentiment, number of positive/negative words etc.), we will not use this column in this analysis.
Secondly, months since last delinquent represents the number months passed since the person last fell into the 90 DPD group. There is an important reason we shouldn't use this column in analysis - since at the time of loan application, we will not have this data (it gets generated months after the loan has been approved), it cannot be used as a predictor of default at the time of loan approval.

Checked format of column, and found its ok. 

**3. Data Analysis:-**

Analysis will start from understanding objective of the analysis clearly and identify the variables that we want to consider for analysis.
The objective is to identify predictors of default so that at the time of loan application, we can use those variables for approval/rejection of the loan. Now, there are broadly three types of variables - 
1. those which are related to the applicant (demographic variables such as age, occupation, employment details etc.)
2. Loan characteristics (amount of loan, interest rate, purpose of loan etc.) &
3. Customer behaviour variables (those which are generated after the loan is approved such as delinquent 2 years, revolving balance, next payment date etc.).
Now, the customer behaviour variables are not available at the time of loan application, and thus they cannot be used as predictors for credit approval.
Thus, going forward, we will use only the other two types of variables.

Now Start with **Univariate Analysis**


Thus let's drop the two columns.
