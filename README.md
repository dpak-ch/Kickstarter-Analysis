# Kickstarter Analysis Using Excel
## Overview of the Project
### Purpose
The purpose of the analysis is two-fold:
1. Provide Louise with an analysis of the kickstarter campaigns so she can get potential insights on why her campaign came so close to its goal, but failed eventually
2. Give the students of this class a practical example on how Excel can be used for data analysis
## Analysis and Challenges
Analysis was performed on the kickstarter data using Excel features that are most useful for dissecting data - Pivot tables and charts. It is important for Louise to understand the reasons her campaign failed. To do that, she needs a way to look at campaigns similar to hers in terms of category, launch date and size.
### Outcomes by Launch Date
The easiest way to dissect this data was using a Pivot Table. I built a Pivot Table with the count of outcomes by Launch month. This gives Louise a sense of whether there are  times during the course of the year when campaigns were more successful. The option to view data by category and timeframe was provided using filters. Below is a screenshot of the pivot table with its filters.

![Outcomes_Pivot](https://user-images.githubusercontent.com/81054290/115276323-80581a80-a108-11eb-9edf-f1def1dbc674.PNG)

After filtering down to "theater" (which is partly what Louise is interested in), I made a visualization using a Line Chart to show Successful and Failed Campaigns as shown below: 

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/81054290/115276633-df1d9400-a108-11eb-8621-87a546df4471.png)

While I did not encounter any challenges in the workflow, here are a couple of things to watch out for:
1. Applying Filters correctly is critical to ensure the analysis provides the desired insight. 
2. We've filtered the data by parent category. Another option will be to include additional filters for "Subcategory" and "Country". While these filters did not change the analysis conclusions, there could have been additional insights.

### Outcomes based on Goals
For this analysis, I used "countifs" to bin outcomes by goal size. A Line chart was the nused to visualize the percentage of successful/failed campaigns by goal size as shown below:

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/81054290/115279133-ec884d80-a10b-11eb-9877-c16344964fcc.png)

Again, I did not encounter any specific challenges. However, complex formulas like Countifs that use multiple conditions are diffuclt to quality check and can lead to erroneous results, especially in large datasets. Do avoid this, it is recommended to do spot checks on the results by manual filters applied on the raw data.
