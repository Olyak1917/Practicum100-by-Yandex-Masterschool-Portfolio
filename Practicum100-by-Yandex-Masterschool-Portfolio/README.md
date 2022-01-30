# Practicum100-by-Yandex-Masterschool-Portfolio
This is my personal Portfolio of demonstrated experience in real-world Data Analyst Projects. 



# Project for a startup that sells food products - Sales Funnel (Conversion) Study, A/A/B Test Results Analysing

**Technologies and Tools** - Python, Jupyter, Pandas, Numpy, Seaborn, Matplotlib, Plotly, Scipy


**Goal:** To investigate user behavior for the company's app.

**Project Description**

You work at a startup that sells food products. You need to investigate user behavior for the company's app.

First study the sales funnel. Find out how users reach the purchase stage. How many users actually make it to this stage? How many get stuck at previous stages? Which stages in particular?

Then look at the results of an A/A/B test. The designers would like to change the fonts for the entire app, but the managers are afraid the users might find the new design intimidating. They decide to make a decision based on the results of an A/A/B test.

The users are split into three groups: two control groups get the old fonts and one test group gets the new ones. Find out which set of fonts produces better results.

Creating two A groups has certain advantages. We can make it a principle that we will only be confident in the accuracy of our testing when the two control groups are similar. If there are significant differences between the A groups, this can help us uncover factors that may be distorting the results. Comparing control groups also tells us how much time and data we'll need when running further tests.

<p align="center">
    <img src=Startup_AABtest&EventFunnel\funnel10.jpg width=700>
</p>

LINK: [Detailed Project](Startup_AABtest&EventFunnel\start_up_event_funnel&AABtest(5))
#
#

# SQL Project - Sturtup on Apps for Book Lovers
**Technologies and Tools** - Python, Jupyter, PostgreSQL, Sqlalchemy, Pandas


**Goal:** The project goal is to generate a value proposition for a new product.

**Project Description**

The coronavirus took the entire world by surprise, changing everyone's daily routine. City dwellers no longer spent their free time outside, going to cafes and malls; more people were at home, reading books. That attracted the attention of startups that rushed to develop new apps for book lovers. 

You've been given a database of one of the services competing in this market. It contains data on books, publishers, authors, and customer ratings and reviews of books. This information will be used to generate a value proposition for a new product.

**Task**

- Find the number of books released after January 1, 2000.
- Find the number of user reviews and the average rating for each book.
- Identify the publisher that has released the greatest number of books with more than 50 pages (this will help you exclude brochures and similar publications from your analysis).
- Identify the author with the highest average book rating (look only at books with at least 50 ratings).
- Find the average number of text reviews among users who rated more than 50 books.
## Conclusion
We would recommend that new product focus on books, released after year 2000, with a reviews from users who rated more than 50 books, and high ratings (>=4), paying special attention on books, published by Penguin Books. No need to say that J.K. Rowling is a must for every books app.

LINK: [Detailed Project](SQL_project\1_6a_booklovers_new_app_value_proposition_SQL)
#
#


# Visualisation Project - Tableau Public Dashboard

**Goal:** To create Interactive Tableau Dashboard according to the Draft.

**Project Description**

Let's take alook at the draft:
<p align="center">
    <img src=Tableau_Public_Project\draft_dashboard.png width=600>
</p>
The date and time filter and country filter should modify all of the dashboard's graphs. Note that the interaction history graphs "Trending History" and "Trending History, %" should have date and time along the X axis. "Trending History" should have the number of videos in the trending section (the videos_count field) along the Y axis, and the other graph should have the percentage there.


To build the dashboard, complete the following steps:

In Tableau Public, use trending_by_time.csv to create a dashboard modeled on the draft.

Publish the dashboard on the Tableau Public server. Make sure it's available for the entire internet: try opening it in several browsers. 

Use your dashboard to answer the questions the managers asked you:

- Which video categories trended most often?
- How were they distributed among regions?
- What categories were especially popular in the United States? Were there any differences between the categories popular in the US and those popular elsewhere?


<p align="center">
    <img src=Tableau_Public_Project\trending_history.jpg width=700>
</p>

<p align="center">
    <img src=Tableau_Public_Project\trending_table.jpg width=700>
</p>

#

We publish ready dashboard on the Tableau Public server:
## Interactive Dashborad on Video Trending by Time and Country

<p align="center">
    <img src=Tableau_Public_Project\dashboard_entire.jpg width=700>
</p>


LINK: [Brief Presentation](Tableau_Public_Project\presentation_video_trending1.pdf)



LINK: [Deshboard](https://public.tableau.com/app/profile/olga3629/viz/project_10_auto_nz/DashboardonVideoTrending?publish=yes)
#
#


# Project - EDA and A/B Test Results Analysing

**Technologies and Tools** - Python, Jupyter, Pandas, Seaborn, Matplotlib, Plotly


**Goal:** Testing changes related to the introduction of an improved recommendation system.

**Project Description**

You've received an analytical task from an international online store. Your predecessor failed to complete it: they launched an A/B test and then quit (to start a watermelon farm in Brazil). They left only the technical specifications and the test results. 

### Technical description

- Test name: `recommender_system_test`
- Groups: А (control), B (new payment funnel)
- Launch date: 2020-12-07
- The date when they stopped taking up new users: 2020-12-21
- End date: 2021-01-01
- Audience: 15% of the new users from the EU region
- Purpose of the test: testing changes related to the introduction of an improved recommendation system
- Expected result: within 14 days of signing up, users will show better conversion into product page views (the `product_page` event), product card views (`product_card`) and purchases (`purchase`). At each of the stage of the funnel `product_page → product_card → purchase`, there will be at least a 10% increase.

- Expected number of test participants: 6000

Download the test data, see whether it was carried out correctly, and analyze the results. 



### Instructions on completing the task

- Describe the goals of the research
- Explore the data
    - Does it need converting types?
    - Are there any missing or duplicate values? If so, what's their nature?
- Carry out exploratory data analysis
    - Study conversion at different funnel stages
    - Is the number of events per user distributed equally in the samples?
    - Are there users who enter both samples?
    - How is the number of events distributed by days?
    - Think of the possible details in the data that you have to take into account before starting the A/B test?
- Evaluate the A/B test results
    - What can you tell about the A/B test results?
    - Use the z-criterion to check the statistical difference between the proportions
- Describe the conclusions on the EDA stage, as well as on the evaluation of the A/B test results

## Conclusion


**Group A Conversion**
<p align="center">
    <img src=EDA_e_comm\funnelA.jpg width=700>
</p>

**Group A Conversion**
<p align="center">
    <img src=EDA_e_comm\funnelB.jpg width=700>
</p>

As we can see from the funnels, all stage’s conversion has decreased.

We plot distribution of number of events per user. As we can see from the graph, distribution of events per user is very similar in the samples.

We plot the distribution of events by days. From the graph we can see constant grow of events till 25th of December, 2020. Than we can see sharp decreasing in number of events with a small local peak around New Year date.

<p align="center">
    <img src=EDA_e_comm\eda_16.jpg width=500>
</p>

We think of the possible details in the data that we have to take into account before starting the A/B test.
Important thing we have to take into account is the calendar of Public holidays. It is never a good idea to test anything around X-Mass and A New Year Eve because spikes in purchases related to holidays can distort A/B test results.
Also before starting A/B test we have to take into account difference in sizes between samples. To be suitable for testing, samples should not differ for more than 10%.

On the next step we evaluate the A/B test results.
What can we tell about the A/B test results?
First, as already mentioned samples appeared more suitable for testing are not ones for 'recommender_system_test', but for 'interface_eu_test'. So we had to evaluate 'interface_eu_test' results. 
Then, condition 15% of EU customers was not fulfilled in either sample.

As for test results of A/B tests - the target - "At each of the stage of the funnel product_page → product_card → purchase, there will be at least a 10% increase" was not achieved. Almost all stages conversion has decreased - from 66.56% to 65.52% for 'product page', from 35.32% to 33.1% for 'purchase'. Only 'product cart' slightly increased from 32.12% to 33.66%, but anyway is far from targeted 10%. And even total purchase sum (column 'details') decreased from 145954 for group A to 129659 for group B.

We conclude that test 'interface_eu_test' was unsuccessful.

Next, we use the z-criterion to check the statistical difference between the proportions.

We formulate statistical hypotheses for to check the statistical difference between the proportions:

H0 - there is no statistical difference between proportions A and B.

H1 - there is a statistical difference between proportions A and B.

After conducting z-test for our A and B groups we cannot reject our H0 hypothesis for events 'product_page', 'login' and 'product_cart'. So we do not observe a statistically significant difference between proportions on these stages. For the event 'purchase' we reject our H0 hypothesis. So there is a difference in proportions for event 'purchase'. We choose a statistical significance level as 0.05.

We would recommend not introducing changes according to 'interface_eu_test' because test appeared unsuccessful. Also we recommend repeating 'recommender_system_test' properly in accordance with technical specifications.

LINK: [Detailed Project](EDA_e_comm\1_6b_e_comm_EDA_ab_test_results_analyzing.ipynb)
#
#
# Project - Business Analytics for Yandex Afisha

**Technologies and Tools** - Python, Jupyter, Pandas, Seaborn, Matplotlib, Numpy


**Goal:** Market expenses optimisation.

**Project Description**
You've been offered an internship in the analytical department at Yandex.Afisha. Your first task is to help optimize marketing expenses.


You have:

- Server logs with data on Yandex.Afisha visits from June 2017 through May 2018

- Dump file with all orders for the period

- Marketing expenses statistics


You are going to study:

- How people use the product

- When they start to buy

- How much money each customer brings

- When they pay off

## Step 1. Download the data and prepare it for analysis
Store the data on visits, orders, and expenses in variables. Optimize the data for analysis. Make sure each column contains the correct data type.

## Step 2. Make reports and calculate metrics:
### Product
- How many people use it every day, week, and month?
- How many sessions are there per day? (One user might have more than one session.)
- What is the length of each session?
- How often do users come back?
### Sales
- When do people start buying? (In KPI analysis, we're usually interested in knowing the time that elapses between registration and conversion — when the user becomes a customer. For example, if registration and the first purchase occur on the same day, the user might fall into category Conversion 0d. If the first purchase happens the next day, it will be Conversion 1d. You can use any approach that lets you compare the conversions of different cohorts, so that you can determine which cohort, or marketing channel, is most effective.)
- How many orders do they make during a given period of time?
- What is the average purchase size?
### How much money do they bring? (LTV)
- Marketing
- How much money was spent? Overall/per source/over time
- How much did customer acquisition from each of the sources cost?
- How worthwhile where the investments? (ROI)

Plot graphs to display how these metrics differ for various devices and ad sources and how they change in time.

## Step 3. Write a conclusion: advise marketing experts how much money to invest and where.
#
#

<p align="center">
    <img src=BA_Ya_Afisha\session_len.jpg width=500>
</p>


<p align="center">
    <img src=BA_Ya_Afisha\cost1&4&10_by_time.jpg width=600>
</p>


<p align="center">
    <img src=BA_Ya_Afisha\heatmapCAC.jpg width=600>
</p>



## Conclusion

Based on our findings we would recommend focus on Sources 2 and 4 as they provide highest revenue, good number of same day orders and not the highest CAC. Sources 5 and 1 are also quite close. We like Source 3 also, but there is enormous CAC, we would recommend investigating the situation with this particular source before marketing budget allocation. Recommended costs for Source 3 considered reasonable within those values for Source 4 to be effective. 

We also check all the metrics for Mobile Devices and Desktops separately. Unfortunately, costs data provided have no separation for costs for “touch” platform and costs for “desktop” platform. Under these circumstances calculation of important metrics as CAC, ROMI and so on separately by platform is not possible. Data on orders does not have a session id, as well as data on visits, so we, strictly speaking, even could not be sure what platform the order came from. So, analyzing platforms on “Sales” and “Marketing” parameters seem to be very limited. However, we can analyze various platforms in “Product” part. Our findings show that there are 3 times more visits from “desktops” and session duration is 3 times longer for “desktops”. From these results we can conclude that Desktop version is considered convenient by users and working properly as 773 sec (about 13 min) is perfect duration for studying offers, making choice and placing order. Also we can see that less than a quarter of orders come from “touch” platform. It looks like users look through app on “touch” platform at glance and then go to “desktop” to make orders. So we would recommend to support both platforms as Mobile version is a must nowadays and “desktop” is in evident demand among Yandex.Afisha users. 

LINK: [Detailed Project](BA_Ya_Afisha\7_BA_YaAfisha.ipynb)

#
#
# Project for Startup - Market Research on LA Restaurants

**Technologies and Tools** - Python, Jupyter, Pandas, Numpy, Seaborn, Matplotlib, Plotly


**Goal:** To prepare Market Research on Los Angeles restaurants.

**Project Description**

You’ve decided to open a small robot-run cafe in Los Angeles. The project is promising but expensive, so you and your partners decide to try to attract investors. They’re interested in the current market conditions—will you be able to maintain your success when the novelty of robot waiters wears off?
You’re an analytics guru, so your partners have asked you to prepare some market research. You have open-source data on restaurants in LA.
#

Type of Establishment for Chain and Non-Chain:
<p align="center">
    <img src=LA_restaurants_market_research\stack.jpg width=500>
</p>

There is an interesting finding - "Bakery" only exists in a chain format.


<p align="center">
    <img src=LA_restaurants_market_research\pie.jpg width=600>
</p>


<p align="center">
    <img src=LA_restaurants_market_research\seats_among_chain.jpg width=550>
</p>


<p align="center">
     <img src=LA_restaurants_market_research\avg_seats_each_type.jpg width=500>
</p>


<p align="center">
    <img src=LA_restaurants_market_research\seats_distr_top.jpg width=550>
</p>



## Overall Conclusion and Recommendations

Based on the results of our research we would support the idea of opening a small robot-run cafe in Los Angeles. The project looks promising even after the novelty of robot waiters wearing off because the small size cafés (22-36seats on average) on top popular streets are obviously trending now. We recommend opting for one of the top ten streets by number of restaurants. Before choosing a particular street we recommend to carry out an additional research on which of the top popular streets attracts most of the youth - apparently a primary target audience for whatever "robot-running". The idea of small café also could be extended to chain format as it fully matches to typical chain unit. This could be done after success of the first (trial) launch or it could be a whopping synchronous launch of 3-5 places provided that there is adequate investment attracted.

LINK: [Presentation](https://drive.google.com/file/d/1FU0V-5Gkstn-k7Zs7zcU9LrFpx3yHt0I/view?usp=sharing)

LINK: [Detailed Project](LA_restaurants_market_research\9_LA_restaurants_market_research.ipynb)
#
#
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
#

## Overall Conclusion

Our project is to prepare a report for a bank’s loan division. We need to find out if a customer’s marital status and number of children has an impact on whether they will default on a loan. There is a dataset provided by bank, which includes customers’ worthiness, family status, age, gender, education level, type of income, total income, number of children and loan purpose.

Investigation of dataset provided shows that number of children, marital status, income level and purpose of loan can affect on the ability of a potential borrower to repay their loan.

Obtained results illustrate connection between having kids and repaying a loan on time – percentage of debt is higher in customers with kids – 9.2% against 7.5%

Connection between marital status and repaying a loan on time was also found. The less reliable category is unmarried - 9.7% of debt, slightly better is civil partnership - 9.3%. Married looks much better - 7.5%, and the most reliable category turned out widow/widower - 6.6%. Divorced got 7.1%.

There is rather little dependence of financial reliability on total income. 10K to 25K of total income gives us percentage of debts 8.5-8.3%. BTW, it’s also covers about half of customers. 25K to 30K shows peak in debts – 9.0%. From 30K to 50K it is 6.5-7.8%. 50-60K gives 8.3%. Minimum of debts are in categories - under 10K and above 60K – 6.3% and 5.6%, respectively.

<p align="center">
    <img src=Data_Preprocessing_Credit_Scoring\pivot.jpg width=700>
</p>

The most impressive is connection by the criterion of the purpose of loan. Thus, purpose “education” shows a record percentage of debts – 34.1%, followed by “car” – 9.3% and “real estate” – 7.2%. “Wedding” seems to be the safest.

So, childfree widow/widower (or divorced) with income above 60K, who wants a loan for wedding, makes the highest overall credit score.

LINK: [Detailed Project](Data_Preprocessing_Credit_Scoring\credit_scoring_1.ipynb)
#
#
# Project - Gym Customer Interaction Strategy, based on Supervised (Classification) and Unsupervised (Clustering) Machine Learning

**Technologies and Tools** - Python, Jupyter, Pandas, Seaborn, Matplotlib, Scipy, Sklearn


**Goal:** To build a model to predict user churn, to create user clusters.

**Project Description**

The gym chain Model Fitness is developing a customer interaction strategy based on analytical data.

One of the most common problems gyms and other services face is customer churn. How do you know if a customer is no longer with you? You can calculate churn based on people who get rid of their accounts or don't renew their contracts. However, sometimes it's not obvious that a client has left: they may walk out on tiptoes.

Churn indicators vary from field to field. If a user buys from an online store rarely but regularly, you can't say they're a runaway. But if for two weeks they haven't opened a channel that's updated daily, that's a reason to worry: your follower might have gotten bored and left you.

For a gym, it makes sense to say a customer has left if they don't come for a month. Of course, it's possible they're in Cancun and will resume their visits when they return, but's that's not a typical case. Usually, if a customer joins, comes a few times, then disappears, they're unlikely to come back.

In order to fight churn, Model Fitness has digitized a number of its customer profiles. Your task is to analyze them and come up with a customer retention strategy.

You should:

- Learn to predict the probability of churn (for the upcoming month) for each customer
- Draw up typical user portraits: select the most outstanding groups and describe their main features
- Analyze the factors that impact churn most
- Draw basic conclusions and develop recommendations on how to improve customer service:
- Identify target groups
- Suggest measures to cut churn
- Describe any other patterns you see with respect to interaction with customers

## Instructions for completing the project
### Step 1. Download the data
Model Fitness provided you with CSV files containing data on churn for a given month and information on the month preceding it. The dataset includes the following fields:

- 'Churn' — the fact of churn for the month in question

- Current dataset fields:
    - User data for the preceding month
        - 'gender'
        - 'Near_Location' — whether the user lives or works in the neighborhood where the gym is located
        - 'Partner' — whether the user is an employee of a partner company (the gym has partner companies whose employees get discounts; in those cases the gym stores information on customers' employers)
        - Promo_friends — whether the user originally signed up through a "bring a friend" offer (they used a friend's promo code when paying for their first membership)
        - 'Phone' — whether the user provided their phone number
        - 'Age'
        - 'Lifetime' — the time (in months) since the customer first came to the gym

- Data from the log of visits and purchases and data on current membership status
    - 'Contract_period' — 1 month, 3 months, 6 months, or 1 year
    - 'Month_to_end_contract' — the months remaining until the contract expires
    - 'Group_visits' — whether the user takes part in group sessions
    - 'Avg_class_frequency_total' — average frequency of visits per week over the customer's lifetime
    - 'Avg_class_frequency_current_month' — average frequency of visits per week over the preceding month
    - 'Avg_additional_charges_total' — the total amount of money spent on other gym services: cafe, athletic goods, cosmetics, massages, etc.

### Step 2. Carry out exploratory data analysis (EDA)
- Look at the dataset: does it contain any missing features? Study the mean values and standard deviation (use the describe() method).
- Look at the mean feature values in two groups: for those who left (churn) and for those who stayed (use the groupby() method).
- Plot bar histograms and feature distributions for those who left (churn) and those who stayed.
- Build a correlation matrix and display it.
### Step 3. Build a model to predict user churn
Build a binary classification model for customers where the target feature is the user's leaving next month.
- Divide the data into train and validation sets using the train_test_split() function.
- Train the model on the train set with two methods:
    - logistic regression
    - random forest
- Evaluate accuracy, precision, and recall for both models using the validation data. Use them to compare the models. Which model gave better results?

Remember to indicate the random_state parameter when dividing data and defining the algorithm.
### Step 4. Create user clusters
Set aside the column with data on churn and identify object (user) clusters:
- Standardize the data.
- Use the linkage() function to build a matrix of distances based on the standardized feature matrix and plot a dendrogram. Note: rendering the dendrogram may take time! Use the resulting graph to estimate the number of clusters you can single out.
- Train the clustering model with the K-means algorithm and predict customer clusters. (Let the number of clusters be n=5, so that it'll be easier to compare your results with those of other students. However, in real life, no one will give you such hints, so you'll have to decide based on the graph from the previous step.)
- Look at the mean feature values for clusters. Does anything catch your eye?
- Plot distributions of features for the clusters. Do you notice anything?
- Calculate the churn rate for each cluster (use the groupby() method). Do they differ in terms of churn rate? Which clusters are prone to leaving, and which are loyal?
### Step 5. Come up with conclusions and basic recommendations on working with customers
Draw conclusions and formulate recommendations regarding the strategy for customer interaction and retention.

You don't need to go into detail. Three or four essential principles and examples of their implementation in the form of specific marketing steps will do.
#
## Step 5. Overall conclusions

On the first step we download the data. We check data for duplicates, no duplicates found.

The data look good. There are no missing values, all min, max, means and standard deviation look meaningful, that means there are no outliers in the dataset provided. The data types are proper, although could be reduced from int64 , this is not necessary because total data volume is quite small.

We look at the mean feature values in two groups: for those who left (churn) and for those who stayed (using the groupby() method).

We plot bar histograms and feature distributions for those who stayed (first bunch of bar histograms) and for those who left (second bunch of bar histograms). Feature 'Age' has normal distribution for both groups. Features 'Avg additional charges total', 'Avg class frequency current month', 'Avg class frequency total' shows skewed normal distribution. 'Avg class frequency current month' for those who left demonstrates alarming peak on '0'. That must be very important feature so. 'Contract Period' could be telling a lot on user intentions, as we see predominant one-two-month contracts among those who left. On the contrary, we can see fair distribution of short and six-twelf-month contracts in those who stayed. Feature 'Group Visits' supports those who stayed, as well as feature 'Partner'. Feature 'Lifetime' naturally goes longer for those who stayed. Feature 'Month to end contract' seem to just follow the 'Contract Period' feature. Features 'Near Location', 'Phone', 'Promo Friends' and 'Gender' seem to be insignificant and not influencing factors.

We build a correlation matrix and display it in the form of heatmap. From this matrix we can see that there is a strong correlation between features 'Avg class frequency total'and 'Avg class frequency current month', namely, 0.95; and 'Month to end contract' and 'Contract period', 0.97. Other features do not demonstrate any considerable correlation.

We build a binary classification model for customers where the target feature is the user's leaving next month.

We divide the data into train and validation sets using the train_test_split() function. We indicate the random_state = 0 parameter when dividing data and defining the algorithm. We train the model on the train set with two methods:

- logistic regression
- random forest

We evaluate accuracy, precision, and recall for both models using the validation data. We use them to compare the models. Logistic Regression Model (Accuracy: 0.93, Precision: 0.86, Recall: 0.83) gave better results than Random Forest Model (Accuracy: 0.91, Precision: 0.83, Recall: 0.78).


We set aside the column with data on churn and identify object (user) clusters.

We standardize the data.

We use the linkage() function to build a matrix of distances based on the standardized feature matrix and plot a dendrogram.  We use the resulting graph to estimate the number of clusters we can single out. From the dendrogram we can see that 4 would be the optimal number of clusters.

<p align="center">
    <img src=Machine_Learning\dendro.jpg width=600>
</p>

We train the clustering model with the K-means algorithm and predict customer clusters (we let the number of clusters be n=5). 

Look at the mean feature values for clusters. We notice that for some features ('gender', 'Phone') means almost do not differ, so these features are not so important and influencive. In the mean time others ('Age', 'Avg additional charges total', 'Contract Period', 'Month to end contract', 'Lifetime') differ quite a lot.

We plot distributions of features for the clusters. We notice that distributions of features for different clusters mostly repeat their shapes but differ in quantity.

<p align="center">
    <img src=Machine_Learning\age.jpg width=500>
</p>

<p align="center">
    <img src=Machine_Learning\freq.jpg width=500>
</p>

<p align="center">
    <img src=Machine_Learning\lifetime.jpg width=500>
</p>

We calculate the churn rate for each cluster (using the groupby() method). We find they are quite differ in terms of churn rate. Highest rate is 0.52 - cluster number 1, then 0.44 - cluster 4 and 0.27 - cluster 3. As for clusters 0 and 2, the churn rates are insignificant - 0.07 and 0.03, respectively. So we can expect clusters 1 and 4 are highly likely leaving. Cluster 3 is a little better, probably among undecided. As for clusters 0 and 2 (which gives us 46% of customers), we can consider them loyal. 


## Recommendations on working with customers

Clusters 1 and 4 show weakness in 'Partner', 'Promo Friends', 'Group visits'  features. In the meantime these clusters represent the youngest part (and massive 44%) of total Model Fitness customers. Probably they begin to fill bored, longly, lost and so wipe off in 2-3 months. We would recommend getting close to these customers first. 

- They probably could appreciate regular fitness events which involve lots of communication and competitive and team spirit. 

- Also special promotions like 'Promo Friends' should be more attractive, to suit these clusters budget. As their additional charges are smallest among all clusters, we can guess, that they, even if they will, cannot afford a personal fitness instructor. In that case we would recommend limited promotions like 'by 2 get 1 free', or 'pay today (for whatever package) and get 50% discount', and send notifications on them at least weekly to keep customers reminded. 

- Also, probably, proper refreshing of regular group classes program could also help them to stay entertained.

- As cluster 4 is weak in feature 'Near Location' while Model Fitness is a chain, it might be helpful to extend membership trough any gym club location (if not done yet), so the customer could choose the nearest one.

- As all of them have left their contact phone, it would be useful to conduct a survey to find out what needs to be improved.

LINK: [Detailed Project](Machine_Learning\forecasts_predictions_15.ipynb)
#
#
