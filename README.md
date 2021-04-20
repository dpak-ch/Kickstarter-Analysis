# Kickstarter Analysis Using Excel

## Contents
* [Overview](#overview-of-the-project)
* [Analysis](#analysis-and-challenges)
* [Results](#results)

## Overview of the Project
### Purpose
The purpose of the analysis is two-fold:
1. Provide Louise with an analysis of the kickstarter campaigns so she can get potential insights on why her campaign came so close to its goal, but failed eventually
2. Give the students of this class a practical example on how Excel can be used for data analysis
## Analysis and Challenges
Analysis was performed on the kickstarter data using Excel features that are most useful for dissecting data - Pivot tables and charts. It is important for Louise to understand the reasons her campaign failed. To do that, she needs a way to look at campaigns similar to hers in terms of category, launch date and size.
### Outcomes by Launch Date
The easiest way to dissect this data was using a Pivot Table. I built a Pivot Table with the count of outcomes by Launch Month. This gives Louise a sense of whether there are  times during the course of the year when campaigns were more successful. The option to view data by category and timeframe was provided using filters. Below is a screenshot of the pivot table with its filters.

![Outcomes_Pivot](https://user-images.githubusercontent.com/81054290/115276323-80581a80-a108-11eb-9edf-f1def1dbc674.PNG)

After filtering down to "theater" (which is mostly what Louise is interested in), I made a visualization using a Line Chart to show Successful and Failed Campaigns as shown below: 

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/81054290/115276633-df1d9400-a108-11eb-8621-87a546df4471.png)

#### Challenges
While I did not encounter any challenges in the workflow, here are a couple of things to watch out for:
1. Applying Filters correctly is critical to ensure the analysis provides the desired insight. 
2. We've filtered the data by parent category. Another option will be to include additional filters for "Subcategory" and "Country". While these filters did not change the analysis conclusions, there could have been additional insights.

### Outcomes based on Goals
For this analysis, I used "countifs" to bin outcomes by goal size. A Line chart was the nused to visualize the percentage of successful/failed campaigns by goal size as shown below:

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/81054290/115279133-ec884d80-a10b-11eb-9877-c16344964fcc.png)

#### Challenges
Again, I did not encounter any specific challenges. However, complex formulas like Countifs that use multiple conditions are diffuclt to quality check and can lead to erroneous results, especially in large datasets. Do avoid this, it is recommended to do spot checks on the results by manual filters applied on the raw data.

## Results
### Conclusions About Outcomes Based on Launch Date
1. May-Jul have seen the most number of campaign launches. While the number of campaigns launched are well above the average for the entire year, the percentage of successful campaigns is only modestly higher than average (~65% vs average of 61%). So, someone starting a campaign in this timeframe can expect a slight edge over starting the rest of the months.
2. December is the worst month for campaign launches. Not only were there the lowest number of launches, the % of failed campaigns is also the highest for that month (51% vs average of 39% failed). 
### Outcomes Based on Goals
1. Majority of the "plays" (~61%) had goals of <$5000. These campaigns also had a significantly high success rate (~71%) compared to the average of 49%. 
2. "Plays" with goals between $5000 and $25,000 had a lower success rate of ~51%. Very few campaigns had goals >$25,000 and the success % may not be meanigful due to the low sample size.
### Limitations of the Dataset
1. The dataset provides a look into the performance of campaigns of different sizes, launched at various times. However, critical insights on why similar sized campaigns failed is difficult to glean from the data. Additional information to subdivide the data (city, type of play - e.g. comedy vs tragedy, marketing information etc.) may give somebody like Louise the insight she needs to launch a successful campaign. For example, it can be observed from the data that Great Britain has a significantly higher % of successful "plays" compared to the US. Along the same lines, there might be areas or cities in the US where certain kinds of plays are not popular.
2. Another limitations is that columns like "staff_pick" and "spotlight" do not come with any description of what they mean and hence cannot be used effectively in the analysis.

### Other Possible Charts/Tables
1. Although not very useful for Louise, the following chart is interesting and points to possible variation among different geograohic profiles within the United States. The Bar Chart below shows that Great Britain had significantly higher % of successful "plays" campaigns compared to the US (77% vs. 62%)

![Theater_Outcome_by_Country](https://user-images.githubusercontent.com/81054290/115305003-451b1300-a12b-11eb-8db0-8dbedb0b9182.png)

2. Another plot that helps Louise further dig down into the data is a Box and Whisker plot of "plays" outcomes in the US. For this plot, I've filtered down just to the campaigns that had goals <$5000. The plot shows that the statistics pertaining to "successful" and "failed" campaigns look very similar, and that there is no discernable correlation between goal amount and outcome within the selected criteria.

![US Plays - Goals vs Outcome B W Plot](https://user-images.githubusercontent.com/81054290/115427001-aa701200-a1c6-11eb-9296-183da8f72a9f.png)



