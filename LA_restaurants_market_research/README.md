# Project for Startup - Market Research on LA Restaurants

**Technologies and Tools** - Python, Jupyter, Pandas, Numpy, Seaborn, Matplotlib, Plotly


**Goal:** To prepare Market Research on Los Angeles restaurants.

**Project Description**

You’ve decided to open a small robot-run cafe in Los Angeles. The project is promising but expensive, so you and your partners decide to try to attract investors. They’re interested in the current market conditions—will you be able to maintain your success when the novelty of robot waiters wears off?
You’re an analytics guru, so your partners have asked you to prepare some market research. You have open-source data on restaurants in LA.
#

Type of Establishment for Chain and Non-Chain:
<p align="center">
    <img src=stack.jpg width=500>
</p>

There is an interesting finding - "Bakery" only exists in a chain format.

#
<p align="center">
    <img src=pie.jpg width=500>
</p>

#
<p align="center">
    <img src=seats_among_chain.jpg width=500>
</p>

#
<p align="center">
     <img src=avg_seats_each_type.jpg width=500>
</p>

#
<p align="center">
    <img src=seats_distr_top.jpg width=500>
</p>

#
## Overall Conclusion

We download and prepare data for the analysis. There are 3 records with missing value in 'chain' column. We fill in 'True' for 'TAQUERIA LOS 3 CARNALES' and 'False' for other two - 'JAMMIN JIMMY'S PIZZA' and 'THE LEXINGTON THEATER'. There are 57 (now 58) different chains in the dataset provided. There are no duplicates found.

We investigate the proportions of the various types of establishments and plot a graph. Restaurants are predominant here in LA - 7255 records, than we can see considerable amount of Fast Foods - 1066 records. Pizzas, Bars and Bakeries are in much smaller quantities - 320, 292 and 283 records, respectively.

We investigate the proportions of chain and nonchain establishments and plot a praph. There are 5974 nonchain type establishments and 3677 establishments of chain type.

We investigate and plot graph on which type of establishment typically a chain is. From the graph we can see that vast majority of Chain Type Establishments are Restaurants - 2293 records. Next are Fast Foods - 605 records, then - Bakeries - 283 and Cafes - 266 records. Pizzas are represented by number of 153, and Bars - by 77 records.

We investigate what characterizes chains: are there many establishments with a small number of seats or a few establishments with a lot of seats? We plot a bar graph for number of seats distribution among Chain Type Establishments. From the graph we can see that somehow there are no Establishments with number of seat in a range from 51 to 57 seats, it looks like a kind of anomaly. More than 75% Chain Type Establishments are places with 50 or less seats. 50% of Chain Type Establishments contain 27 or less seats. 25% of Chain Type Establishments have not more than 14 seats. Big places (100+) are quite rare, they probably have their niche of big events like weddings, jubilees or corporate events. Below we also plot a boxplot to illustrate what are outliers for all Chain Type Establishments. So we can characterize chains mostly as many establishments with a small number of seats.

We determine the average number of seats for each type of restaurant and which type of restaurant has the greatest number of seats. We plot bar graph on average number of seats for each type of restaurant. On average, greatest number of seats has Type 'Restaurant' - 48 seats. Next are 'Bar' and 'Fast Food' Type with 45 and 32 seats, respectively. 'Pizza' has 28, 'Cafe' - 25 and 'Bakery' - 22 seats.

We put the data on street names from the address column in a separate column named 'street'.

We plot a graph of the top ten streets by number of restaurants. Leading streets have from 405 to 254 restaurants. The list of top ten restaurants is as follows, in descending order: SUNSET BLVD - 405, WILSHIRE BLVD -398, PICO BLVD - 371, WESTERN AVE - 371, FIGUEROA ST - 334, OLYMPIC BLVD - 310, VERMONT AVE - 288,3RD ST - 265, SANTA MONICA BLVD - 264, HOLLYWOOD BLVD 254. With total amount of 3260 restaurants, the top 10 streets hold more than 30% of all establishments. We find the number of streets that only have one restaurant. It must be noted here that dataset provided contains a massive amount of misspelled street names and other address errors. We did our best to verify the data by means of open sources, however due to mentioned initial data quality the result might not be entirely accurate. We encountered 151 streets that only have one restaurant.

For streets with a lot of restaurants, we look at the distribution of the number of seats. We plot a boxplot for distribution of number of seats in Top 10 Streets' restaurants. We can observe that there are outliers on each street with the number of seats more than 100, up to more than 200. But there are few. For most streets 75% of places have below 50 seats, except WILSHIRE BLVD and HOLLYWOOD BLVD which tend to have more seats. Medians are 22-36 seats, means - 35-56 seats (uplifted due to outliers). We can conclude that relatively small places of 22-36 seats are in trend on the top popular streets.

LINK: [Presentation](https://drive.google.com/file/d/1FU0V-5Gkstn-k7Zs7zcU9LrFpx3yHt0I/view?usp=sharing)

## Recommendations

Based on the results of our research we would support the idea of opening a small robot-run cafe in Los Angeles. The project looks promising even after the novelty of robot waiters wearing off because the small size cafés (22-36seats on average) on top popular streets are obviously trending now. We recommend opting for one of the top ten streets by number of restaurants. Before choosing a particular street we recommend to carry out an additional research on which of the top popular streets attracts most of the youth - apparently a primary target audience for whatever "robot-running". The idea of small café also could be extended to chain format as it fully matches to typical chain unit. This could be done after success of the first (trial) launch or it could be a whopping synchronous launch of 3-5 places provided that there is adequate investment attracted.


LINK: [Detailed Project](9_LA_restaurants_market_research.ipynb)
#
