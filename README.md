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
    <img src=Startup_AABtest&EventFunnel\funnel10.jpg width=500>
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
    <img src=Tableau_Public_Project\draft_dashboard.png width=500>
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
    <img src=Tableau_Public_Project\trending_history.jpg width=500>
</p>

<p align="center">
    <img src=Tableau_Public_Project\trending_table.jpg width=500>
</p>

#

We publish ready dashboard on the Tableau Public server:
## Interactive Dashborad on Video Trending by Time and Country

<p align="center">
    <img src=Tableau_Public_Project\dashboard_entire.jpg width=500>
</p>


LINK: [Brief Presentation](presentation_video_trending1.pdf)



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
    <img src=EDA_e_comm\funnelA.jpg width=500>
</p>

**Group A Conversion**
<p align="center">
    <img src=EDA_e_comm\funnelB.jpg width=500>
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
    <img src=BA_Ya_Afisha\cost1&4&10_by_time.jpg width=500>
</p>




<p align="center">
    <img src=BA_Ya_Afisha\heatmapCAC.jpg width=500>
</p>



## Conclusion

Based on our findings we would recommend focus on Sources 2 and 4 as they provide highest revenue, good number of same day orders and not the highest CAC. Sources 5 and 1 are also quite close. We like Source 3 also, but there is enormous CAC, we would recommend investigating the situation with this particular source before marketing budget allocation. Recommended costs for Source 3 considered reasonable within those values for Source 4 to be effective. 

We also check all the metrics for Mobile Devices and Desktops separately. Unfortunately, costs data provided have no separation for costs for “touch” platform and costs for “desktop” platform. Under these circumstances calculation of important metrics as CAC, ROMI and so on separately by platform is not possible. Data on orders does not have a session id, as well as data on visits, so we, strictly speaking, even could not be sure what platform the order came from. So, analyzing platforms on “Sales” and “Marketing” parameters seem to be very limited. However, we can analyze various platforms in “Product” part. Our findings show that there are 3 times more visits from “desktops” and session duration is 3 times longer for “desktops”. From these results we can conclude that Desktop version is considered convenient by users and working properly as 773 sec (about 13 min) is perfect duration for studying offers, making choice and placing order. Also we can see that less than a quarter of orders come from “touch” platform. It looks like users look through app on “touch” platform at glance and then go to “desktop” to make orders. So we would recommend to support both platforms as Mobile version is a must nowadays and “desktop” is in evident demand among Yandex.Afisha users. 

LINK: [Detailed Project](BA_Ya_Afisha\7_BA_YaAfisha.ipynb)