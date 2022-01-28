# Project - EDA and A/B Test Results Analysing

**Technologies and Tools** - Python, Jupyter, Pandas, Seaborn, Matplotlib, Plotly


**Goal:** testing changes related to the introduction of an improved recommendation system.

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


- `ab_project_marketing_events_us.csv` — the calendar of marketing events for 2020
- `final_ab_new_users_upd_us.csv` — all users who signed up in the online store from December 7 to 21, 2020
- `final_ab_events_upd_us.csv` — all events of the new users within the period from December 7, 2020 to January 1, 2021
- `final_ab_participants_upd_us.csv` — table containing test participants

Structure of `ab_project_marketing_events_us.csv`:

- `name` — the name of the marketing event
- `regions` — regions where the ad campaign will be held
- `start_dt` — campaign start date
- `finish_dt` — campaign end date

Structure of `final_ab_new_users_upd_us.csv`:

- `user_id`
- `first_date` — sign-up date
- `region`
- `device` — device used to sign up

Structure of `final_ab_events_upd_us.csv`:

- `user_id`
- `event_dt` — event date and time
- `event_name` — event type name
- `details` — additional data on the event (for instance, the order total in USD for `purchase` events)

Structure of `final_ab_participants_upd_us.csv`:

- `user_id`
- `ab_test` — test name
- `group` — the test group the user belonged to

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

We download 4 datasets. We change types where needed - dates for 'datetime64' and categorical values for 'category'.

We find no duplicates in datasets.

We find a lot of missing values (about 86%) in dataset 'final_ab_events_upd_us' in column 'details'.
Only 'event_name' - 'purchase' has info on details, what looks naturally, because it's obviously sum of purchase. And count of 'details' values (60 314) coincident with count of events 'purchase'. That confirms our guess that 'details' shows purchase sum. So we replace missing values with '0' as no event except 'purchase' is characterized by purchase sum.

Let's prepare data for the funnel and answer the task questions.

We plot Types of Events Distribution. From graph we can see that number of events 'purchase' exceed the number of events 'product_cart'.

We check part of new users from EU region in each test group 'recommender_system_test' and 'interface_eu_test'.
For test group 'recommender_system_test' we find 3481 new users of 3675 participating in recommender_system_test are from EU region. This is not 15% that required by specs, this is almost 95%.
For test group  'interface_eu_test' we find that all 10850 users participating in interface_eu_test are from EU.

We check if there are users who enter both A and B samples.
Our findings show there are no users who enter both A and B samples. Group A consists of 8214 participants, group B - of 6311.

We check if there are users in group A who enter both 'recommender_system_test' and 'interface_eu_test'.
Among group A (8214) there are no users who are participating in both tests same time. 2747 users participated in 'recommender_system_test' and 5467 users participated in 'interface_eu_test', wthich is 8214 being summed up.
We check if there are users in group B who enter both 'recommender_system_test' and 'interface_eu_test'.
Among group B (6311) there are no users who are participating in both tests same time. 928 users participated in 'recommender_system_test' and 5383 users participated in 'interface_eu_test', wthich is 6311 being summed up.
Based on above data study we understand that we have to choose 'interface_eu_test' for building funnel and analyzing, as A and B groups for 'recommender_system_test' are much smaller than requested (2747+928=3675 against 6000 expected) and unacceptably differ in size (2747 and 928). After that studies we can go to funnel building itself.

**Group A Conversion**
<p align="center">
    <img src=funnelA.jpg width=500>
</p>

**Group A Conversion**
<p align="center">
    <img src=funnelB.jpg width=500>
</p>

As we can see from the funnels, all stage’s conversion has decreased.

We plot distribution of number of events per user. As we can see from the graph, distribution of events per user is very similar in the samples.

We plot the distribution of events by days. From the graph we can see constant grow of events till 25th of December, 2020. Than we can see sharp decreasing in number of events with a small local peak around New Year date.

<p align="center">
    <img src=eda_16.jpg width=500>
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

LINK: [Project](1_6b_e_comm_EDA_ab_test_results_analyzing.ipynb)