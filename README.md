Problem statement:-
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


![EDA1](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/adff6271-cb30-4513-a2a3-ba7092efb044)
![EDA2](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/8478a8b4-17e7-4625-9d3b-46d127f87a36)
![EDA3](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/19eee3c8-07cb-40ae-a2ba-6217326be14b)
![EDA4](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/42569592-8dcf-4c40-8188-15575883d80c)
![EDA5](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/e1f398f7-5892-492e-87ed-ddbea0ccfa27)
![EDA6](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/f0bf6063-8034-400a-9d34-e0e402f75766)
![EDA7](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/b7c2683a-fd15-43b3-8f2f-282c723a9756)
![EDA8](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/478bbf8a-dd48-44da-9721-7ffd33999288)
![EDA9](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/eaa328ce-d9de-4cce-9d62-9e5692a7145c)
![EDA10](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/398d5041-b0da-48a2-af28-d045f8115906)
![EDA11](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/84844477-4f38-4c16-9256-15b840188a08)
![EDA12](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/102de665-c537-41d4-9445-c4d1c0afccac)
![EDA13](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/6183f3d4-203d-483a-8ef4-f13069dfb72d)
![EDA14](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/784dfe94-5537-4315-bb54-940713b63ae2)
![EDA15](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/e3d0c40d-eee5-4feb-8388-ada2c4ba3926)
![EDA16](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/bd27b5a0-5d16-4e2a-977d-b6c2517539f9)
![EDA17](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/6a8dcccb-c1ee-4427-9180-712e7c40feb6)
![EDA19](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/7d8dd31b-af0d-4afd-9e93-2d64099693d9)
![EDA20](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/6d56792e-0982-49d9-8171-6c758b928076)
![EDA21](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/810045b2-0e23-4e51-b4e6-eb4a2225c7b5)
![EDA22](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/c1741bee-48a4-4255-8131-1c1342948971)
![EDA23](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/061f3d8c-9608-4b3c-a04d-47294c7106ea)
![EDA24](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/8316e3ce-4858-455a-8892-b153793cf94b)
![EDA25](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/c4fa6cd6-53d5-4a51-9854-7fcb8213260c)
![EDA26](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/2bcbcd56-1ce3-4723-8f1c-841b27a4f6ba)
![EDA27](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/6c1f5928-acd8-44a4-96fa-23d2e23b9657)
![EDA28](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/4be93b88-0608-455b-97b7-434445c5cdb3)

**Segmented univariate Analysis:-**


![EDA29](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/0cf3de3a-1301-4a77-9b1d-3bdb5eed2215)
![EDA30](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/f5a332f4-a20e-4144-a803-c2bbf5f7dc2c)
![EDA31](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/8856618d-2b10-4461-887e-8afca75c378c)
![EDA32](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/283739d7-f360-4220-bc7d-5e8f14914f43)
![EDA33](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/9c200931-daf7-46bf-a144-5d137200238d)
![EDA34](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/912488f0-70a9-4e6f-bf95-a15ae2a5fa54)
![EDA35](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/6fe942a3-3e64-41ff-95f6-2226822bac90)
![EDA36](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/8e18f39b-6c87-49b2-b527-6d2394628e92)
![EDA37](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/5597e6e3-721e-4a2d-9f43-8173ea6b425b)
![EDA38](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/49547feb-8a58-4f5a-8533-a8defbf1567d)
![EDA39](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/24667abe-540d-4edd-9d46-dd071c9fa2f3)

**Now Lets start Bivariate Analysis:-**
Analysing annual income, loan type, loan status, Product combination, Gender, Education & application status.


![EDA40](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/802956cf-215b-4925-b4f1-1895c9be70bc)
![EDA41](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/bebca4a3-3ee9-4993-b2ed-bf9a201b0c67)
![EDA42](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/2c1ba08d-8dac-4cd8-bc10-85569b97812f)
![EDA43](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/434405e0-345c-4139-9841-ccc7c3401616)
![EDA44](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/d0382901-51ba-4281-bff7-2b97ec2ec80c)
![EDA45](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/f9acdd94-a479-4365-9183-6504cf7660c6)
![EDA46](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/7db731be-71b0-4264-9e4b-195d39f9af24)
![EDA47](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/dc134068-c22d-4973-a1fe-4908487c35be)
![EDA48](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/757031dd-7f3b-491c-a773-ac5f3faae54b)
![EDA50](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/ee486309-ed4d-40df-8c9d-091a3bdd2fad)
![EDA49](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/5b27c490-63ba-4fc9-8657-788a813d7ee4)
![EDA51](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/2e846fe8-9e1c-4b29-9082-357b371d4029)
![EDA52](https://github.com/erahul0074u/Rahul-Kumar-Lending-Club-Case-Study/assets/137909149/e347d288-1b28-4df5-9d5a-7fe6dd272e4d)

**Conclusion:-**

Banks should focus less on income type ‘Working’ as they are having most number of unsuccessful payments.
Loan Purpose on 'Repair' having highest number of unsuccessful repayments.
Housing Type 'With Parents' having least number of unsuccesful repayments.
In Genders,'Females' are more in number for applying loans.
Banks should focus on 'Students' ,'Pensioner' for successful repayments













