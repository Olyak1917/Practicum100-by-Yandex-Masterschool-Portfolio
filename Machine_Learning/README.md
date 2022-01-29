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
    <img src=dendro.jpg width=600>
</p>

We train the clustering model with the K-means algorithm and predict customer clusters (we let the number of clusters be n=5). 

Look at the mean feature values for clusters. We notice that for some features ('gender', 'Phone') means almost do not differ, so these features are not so important and influencive. In the mean time others ('Age', 'Avg additional charges total', 'Contract Period', 'Month to end contract', 'Lifetime') differ quite a lot.

We plot distributions of features for the clusters. We notice that distributions of features for different clusters mostly repeat their shapes but differ in quantity.

<p align="center">
    <img src=age.jpg width=500>
</p>

<p align="center">
    <img src=freq.jpg width=500>
</p>

<p align="center">
    <img src=lifetime.jpg width=500>
</p>

We calculate the churn rate for each cluster (using the groupby() method). We find they are quite differ in terms of churn rate. Highest rate is 0.52 - cluster number 1, then 0.44 - cluster 4 and 0.27 - cluster 3. As for clusters 0 and 2, the churn rates are insignificant - 0.07 and 0.03, respectively. So we can expect clusters 1 and 4 are highly likely leaving. Cluster 3 is a little better, probably among undecided. As for clusters 0 and 2 (which gives us 46% of customers), we can consider them loyal. 


## Recommendations on working with customers

Clusters 1 and 4 show weakness in 'Partner', 'Promo Friends', 'Group visits'  features. In the meantime these clusters represent the youngest part (and massive 44%) of total Model Fitness customers. Probably they begin to fill bored, longly, lost and so wipe off in 2-3 months. We would recommend getting close to these customers first. 

- They probably could appreciate regular fitness events which involve lots of communication and competitive and team spirit. 

- Also special promotions like 'Promo Friends' should be more attractive, to suit these clusters budget. As their additional charges are smallest among all clusters, we can guess, that they, even if they will, cannot afford a personal fitness instructor. In that case we would recommend limited promotions like 'by 2 get 1 free', or 'pay today (for whatever package) and get 50% discount', and send notifications on them at least weekly to keep customers reminded. 

- Also, probably, proper refreshing of regular group classes program could also help them to stay entertained.

- As cluster 4 is weak in feature 'Near Location' while Model Fitness is a chain, it might be helpful to extend membership trough any gym club location (if not done yet), so the customer could choose the nearest one.

- As all of them have left their contact phone, it would be useful to conduct a survey to find out what needs to be improved.

LINK: [Detailed Project](forecasts_predictions_15.ipynb)
#
#