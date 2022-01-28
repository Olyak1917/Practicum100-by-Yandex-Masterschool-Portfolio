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



We download the data and prepare it for the analysis. We remove 2 outliers corresponding to sources 6 and 7 from data on visits as they are statistically insignificant (6 and 36 visits, respectively) and moreover, not represented in data on costs.

On the next step we make reports and calculate metrics.

 We find how many people use it every day, week, and month and plot histograms. From histogram we can see that peak number of customers for Mobile Devices is around 350, and for Desktops peak is about 700 users. So, we can conclude that this app is twice more popular on Desktops.
 
We plot distribution for number of both platform users together for every day. There are some outliers (anomalies) - 1 user for 2018-03-31 (probably just incomplete data, or probably – no activity after Good Friday https://www.calendar-12.com/calendar/2018/march/) and 3319 users for 2017-11-24 (overwhelmed due to Black Friday (Black Friday is the day following Thanksgiving Day). Distribution has peaks around 500 users and 1200 users.

<p align="center">
    <img src=session_len.jpg width=500>
</p>

Also to describe the number of active users we find  Sticky DAU = 15.9 and Sticky MAU = 3.9.
We plot bar graph on Number of Users by Weeks. Graph shows gradual growth till week 2017-11-27, having peak value of 10586 users, then number of weekly users starts to decrease.

We plot number of visitors by months. There is a sharp growth from September, 2017 to December, 2017. Then in January, 2018 user number starts to decrease, generally repeating previous (weekly) graph shape. There is a peak of 32796 users during 2017-11-01 week.

We find average number of sessions per day - 987 sessions.

We find the length of each session.
Distributions of Session Length for Mobile Devices and Desktops are generally same. However we can see slightly bigger proportion of Sessions durations around 500 sec for Desktops, then ones for Mobile Devices. Average Session Length for Desktop (773 sec) is about 3 times longer than one for Mobile Devices (240 sec). It looks like users found it more convenient to use the app on Desktop rather than on Mobile Device. That could probably mean the Mobile Version has a room for improvement.

We plot Session Length distribution for all devices. 75% of sessions are under 900 sec, 50% - under 360sec, 25% - under 120sec. Mean session length is 714 sec, median is 360 sec. There are some outliers up to 42660 sec. There are also 35794 records with zero length values.

We find the retention rate and build a partial heatmap. It's highest for the first cohort (2017-05-29) and even grows from time to time. In general, users come back not too often.

We investigate when people start buying. 

We plot bar graph for the first orders distribution by order date. First orders distribution by dates shows some seasonality. We can see increasing number of orders around November and December.

If we assume that registration supposed to come before order, than 145 records are corrupted and needed to drop as Session lenght is negative. If somehow order is possible without any preceding activity, than these records could make sense. Before we get additional info, we disregard these records.

For at least 70% of users the registration and the first purchase occur on the same day, another 5% of users order the next day. Within first 16 days 84% (30322) of all users have already made their first order.

We plot bar graph for orders by cohorts. 25197 users belong to Conversion 0d and 1893 users to Conversion 1d). The number of users making purchases decreases with time passed after first activity. Vast majority of users are making their first order on the registration day (25197 users) and next day (1893 user).

From pivot table and Heatmap on First Order by Cohort and Source we can see that most same day orders come from Sources 4, 3 and 5. Then go Sources 2, 1, 10 and 9. For the next day orders leaders are the same. Sources 4, 3 and 5 actually keep leading throughout the rest elapse times. So Sources 4, 3 and 5 look most effective prior evaluating costs involved.

<p align="center">
    <img src=cost1&4&10_by_time.jpg width=500>
</p>

We find out how many orders do users make during a given period of time. We observe that there are 36080 first orders for a given time (from 2017-06-01 to 2018-06-01).

We investigate the average purchase size. We plot a pivot table on average purchase size by cohorts by sources. It shows that Sources 2, 1 and 5 have the highest average purchase sizes.

We find how much money they bring (LTV). Average LTV increases with the age of cohort from about 5 to about 12. As margin rate is not provided, we apply 1, assuming gross profit is equal to revenue. As soon as actual margin rate will be available our metrics could be easily recalculated. Sources 2, 4 and 3 brought highest amounts of money. Sources 5 and 1 are quite close following. 

We find how much money was spent - overall/per source/over time. Overall cost totaled to 329132.62. Per Source - as follows: 
1      20833.27
2      42806.04
3     141321.63
4      61073.60
5      51757.10
9       5517.49
10      5822.49

Over time spending by sources are shown in respective pivot table. No clear patterns identified.

We investigate how much customer acquisition from each of the sources costs. Most expensive buyers are of Sources 3 (13.7), 2 (9.05), 4 (8.47), 5 (7.09). Less expensive ones come from Sources 1 (5.57) and 9 (2.97).

<p align="center">
    <img src=heatmapCAC.jpg width=500>
</p>

We find how worthwhile where the investments (ROMI). The June Cohort paid off in the 7th month (ROMI = 1.05). (We start counting at 0.) The September Cohort paid off in the 4th month (ROMI = 1.19). There is no more paid off Cohorts so far.

## Conclusion

Based on our findings we would recommend focus on Sources 2 and 4 as they provide highest revenue, good number of same day orders and not the highest CAC. Sources 5 and 1 are also quite close. We like Source 3 also, but there is enormous CAC, we would recommend investigating the situation with this particular source before marketing budget allocation. Recommended costs for Source 3 considered reasonable within those values for Source 4 to be effective. 

We also check all the metrics for Mobile Devices and Desktops separately. Unfortunately, costs data provided have no separation for costs for “touch” platform and costs for “desktop” platform. Under these circumstances calculation of important metrics as CAC, ROMI and so on separately by platform is not possible. Data on orders does not have a session id, as well as data on visits, so we, strictly speaking, even could not be sure what platform the order came from. So, analyzing platforms on “Sales” and “Marketing” parameters seem to be very limited. However, we can analyze various platforms in “Product” part. Our findings show that there are 3 times more visits from “desktops” and session duration is 3 times longer for “desktops”. From these results we can conclude that Desktop version is considered convenient by users and working properly as 773 sec (about 13 min) is perfect duration for studying offers, making choice and placing order. Also we can see that less than a quarter of orders come from “touch” platform. It looks like users look through app on “touch” platform at glance and then go to “desktop” to make orders. So we would recommend to support both platforms as Mobile version is a must nowadays and “desktop” is in evident demand among Yandex.Afisha users. 

LINK: [Detailed Project](7_BA_YaAfisha.ipynb)