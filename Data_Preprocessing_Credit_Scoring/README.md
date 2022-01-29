# Project - Data Preprocessing: Report for a Bank's Loan Division

**(*This was my very first project as a Data Analyst)*)**

**Technologies and Tools** - Python, Jupyter, Pandas, NLTK Package


**Goal:** To find out if a customer’s marital status and number of children have an impact on whether they will default on a loan.

**Project Description**

Your project is to prepare a report for a bank’s loan division. You’ll need to find out if a customer’s marital status and number of children have an impact on whether they will default on a loan. The bank already has some data on customers’ credit worthiness.

Your report will be considered when building a credit score for a potential customer. A credit score is used to evaluate the ability of a potential borrower to repay their loan.

## Instructions for completing the project

### Step 1. Open the data file and have a look at the general information.

### Step 2. Preprocess the data:

- Identify and fill in missing values
- Replace the real number data type with the integer type
- Delete duplicate data
- Categorize the data

Be sure to explain:
- Which missing values you identified
- Possible reasons these missing values were present
- Which method you used to fill in missing values
- Which method you used to find and delete duplicate data and why
- Possible reasons why duplicate data was present
- Which method you used to change the data type and why
- Which dictionaries you've selected for this dataset and why

The data may contain artifacts, or values that don't correspond to reality (for instance, a negative number of days employed). This kind of thing happens when you're working with real data. You need to describe the possible reasons such data may have turned up and process it.

### Step 3. Answer these questions:

- Is there a connection between having kids and repaying a loan on time?
- Is there a connection between marital status and repaying a loan on time?
- Is there a connection between income level and repaying a loan on time?
- How do different loan purposes affect on-time loan repayment?

Interpret your answers. Explain what the results you obtained mean.

### Step 4. Write an overall conclusion.

## Description of the data
children: the number of children in the family

days_employed: how long the customer has been working

dob_years: the customer’s age

education: the customer’s education level

education_id: identifier for the customer’s education

family_status: the customer’s marital status

family_status_id: identifier for the customer’s marital status

gender: the customer’s gender

income_type: the customer’s income type

debt: whether the customer has ever defaulted on a loan

total_income: monthly income

purpose: reason for taking out a loan
#

## Overall Conclusion

Our project is to prepare a report for a bank’s loan division. We need to find out if a customer’s marital status and number of children has an impact on whether they will default on a loan. There is a dataset provided by bank, which includes customers’ worthiness, family status, age, gender, education level, type of income, total income, number of children and loan purpose.

While completing the project, we open the data file /datasets/credit_scoring_eng.csv and have a look at the general information. Than we start to pre-process the data: we Identify and fill in missing values in columns “gender”, “total_income”, “children”. It was quite significant number of missing values in column “total_income” – about 10% (probably the form customer was required to fill up was different and missing field about the total income). We replace them with medians, calculated with grouping by income type, gender and age, as they notably vary from one group to another. We drop one whole column “dob_years”, because it does not make sense, probably due to wrong source or wrong formatting. We also convert data type int64, which is redundant, to int8, and float64 to float32 to reduce memory usage. We check dataset for duplicates; there are some case sensitivity duplicates. We convert everything to lower case. In real life - they are not duplicates, they are different borrowers to the bank. As we do not have any customer ID, or Name and Surname or/and birthday in dataset provided, we cannot stipulate they are the same people. There are millions of people of same age, gender, type of income, education level and marital status who want a loan to buy a property. As for 'total_income' column, we remember, that we filled it with many same values by our discretion. So the conclusion is: we must keep all this rows until personal ID data will be available and will confirm (or ruin) the idea of duplicates. It’s not duplicates anymore from the bank’s point of view, so we do not delete them here.  

We categorize data on total income into 11 categories. 
Investigation reveals, however, it was over detailed, half (5-6) would already be enough. We categorized data in “purpose” column. Investigation shows that all entries in “purpose” column can be classified into 4 categories: “car”, “education”, “real estate” and “wedding”.

Investigation of dataset provided shows that number of children, marital status, income level and purpose of loan can affect on the ability of a potential borrower to repay their loan.

Obtained results illustrate connection between having kids and repaying a loan on time – percentage of debt is higher in customers with kids – 9.2% against 7.5%

Connection between marital status and repaying a loan on time was also found. The less reliable category is unmarried - 9.7% of debt, slightly better is civil partnership - 9.3%. Married looks much better - 7.5%, and the most reliable category turned out widow/widower - 6.6%. Divorced got 7.1%.

There is rather little dependence of financial reliability on total income. 10K to 25K of total income gives us percentage of debts 8.5-8.3%. BTW, it’s also covers about half of customers. 25K to 30K shows peak in debts – 9.0%. From 30K to 50K it is 6.5-7.8%. 50-60K gives 8.3%. Minimum of debts are in categories - under 10K and above 60K – 6.3% and 5.6%, respectively.

<p align="center">
    <img src=pivot.jpg width=700>
</p>

The most impressive is connection by the criterion of the purpose of loan. Thus, purpose “education” shows a record percentage of debts – 34.1%, followed by “car” – 9.3% and “real estate” – 7.2%. “Wedding” seems to be the safest.

So, childfree widow/widower (or divorced) with income above 60K, who wants a loan for wedding, makes the highest overall credit score.



LINK: [Detailed Project](credit_scoring_1.ipynb)
