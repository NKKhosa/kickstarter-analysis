# kickstarter-analysis
Performing analysis on Kickstarter data to uncover trends

# Optimizing the Funding of Plays Through Kickstarter

## Overview of Project

### Purpose
A client, Louise, is experimenting with the use of kickstarter to fund her plays. She would like some insight into the successes and failures of various play kickstarters. Here we have compared the outcomes based on campaign launch date, and funding goals.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
The analysis of outcomes based on the campaign launch date was conducted using a pivot table that was filtered from the main dataset by the parent category of "theatre" and by years. The Date created column was converted from the Unix timestamps in the "launched_at" column to ease readability, and used as the axis. From this subset, a chart was created to show the number of successful, failed, and canceled campaigns from each month.
(Ref: Launch_date_pivot_table.png in resources folder)

### Analysis of Outcomes Based on Goals
To conduct the analysis of outcomes based on goals, the goals were split into 12 categories starting with >1000, 1000 to 4999, and then increasing in increments of 5000 until 50000 was reached. From the dataset the COUNTIFS() function was utilized to list the number of successful, failed, and canceled campaigns in each category for only the subset of the data that was in the subcategory of "plays". Next, the percentage of successful, failed, and canceled campaigns were used to create a line chart.
(Ref: Goal_amount_vs_outcome_table.png, Example_COUNTIF_formula_used.png in resources folder)

### Challenges and Difficulties Encountered
I had some challenges with the syntax of the COUNTIFS() function due to the multiple if criteria required to obtain the specific results. However, after combing through the formula I was able to debug it of syntax errors, such as missing commas and quotations. 


## Results

### Conclusions Drawn from Outcomes Based on Launch Date
From the Outcomes Based on Launch Date chart, we can surmise that there is a steady number of failed campaigns through out the year. This means that the month a campaign is launched does not quite affect the probability of its failure. 

The successful campaigns, however, do spike from May to July. This suggests that there is an increase in campaigns started in these months. However, the fact that the failed campaigns dont match the same increase during these months suggests that there is some other criteria, that once met, and matched with the above launch months, will increase the likelihood of success. 


### Conclusions Drawn from Outcomes Based on Goals
From the Outcomes Based on Goals graph, we can see that there is no real trend based on the categories of funding goal amounts that we have chosen. Initially, for the "Less than 1000" and "1000 to 4999" categories there is a significantly higher percentage of successful vs. failed campaigns. This, however, lowers to an even split between successful and failed campaigns for the "5000 to 9999" through "2000 to 24999" categories. Then, the percentage failed increases for the next two categories, and then there is another flip, where percentage successful is higher, and then another flip where percentage failed is higher for the last two categories. 

This shows that lower funding goals, specifically >5000 have a greater chance of successfully meeting their goals, but as the goal increases, there is generally a lower chance of success.

### Limitations of Dataset
A potential limitation of this dataset is that it only includes metrics from the site itself. These campaigns do not exist in a vaccuum on kickstarter.com and external factors such as, level of engagement and promotion of campaigns (e.g. across online platforms, in real life, etc.) could greatly impact the probability of success. 

One way to make this dataset more robust may be to include the number of shares to various social media/ networking platforms. And, to account for the offline promotion, perhaps a questionaire could be added that prompts campaign runners to share the level of outreach that was done outside of the website to reveal potential correlations in successful outcomes. 

Additionaly, the number of views a campaign gets could help reveal would be beneficial to know. Using this compared to the number of backers, we would be able to determine the level of outreach a campaign needs to get the appropriate level of backers.


### Additional Tables/ Graphs that May be Insightful
An additional tables and graphs that could be created to help Lousie with her research could be a visualization of length of campaign vs outcome. We have already seen that there is a more beneficial time to launch a campaign, but perhaps the length of a campaign is also critical in the level of success.

Another graph that could be insightful would be the number of backers vs outcome, particularly the average number of backers that successful campaigns recieved. This could help Louise ensure that her campaign is exposed to the optimal number of people to increase chances of backers.
