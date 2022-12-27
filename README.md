# Assignment1
Module 1: Assignment 1
Please see the attached Word document and Excel document for additional information.

## Part 1

![Outcome colour filter](https://user-images.githubusercontent.com/120147552/209694366-6cfbe216-e299-4721-a653-2d7a403068df.png)

For filling each cell in the outcome column with a different color, depending on whether the associated campaign was successful, failed, canceled, or is currently live, I used the following colour allocation:
    Successful = Green,
    Failed = Red,
    Canceled = Yellow,
    Live = Blue
    
  ![Percent Funded](https://user-images.githubusercontent.com/120147552/209695331-c3d00d1a-06f6-428d-a501-0868806ca7ed.png)

To calculate the new percent funded column for each entry, I did Column E (pledged) divided by Column D (goal) and multiplied it by 100.
For filling each cell in the Percent Funded column according to a three-color scale according to the percentage of funding that each entry received, the scale starts at 0% with a dark shade of red, and it transitions to green at 100% and blue at 200%.

![Average Donation](https://user-images.githubusercontent.com/120147552/209695349-25911f04-0065-466b-81b1-a9557c9ce1f6.png)

A new column for Average Donation was created and filled by dividing column H (backers_count) by Column E (pledged) for each entry.

![Categories](https://user-images.githubusercontent.com/120147552/209696465-61c5286c-7d09-4507-a418-3859e9eaec89.png)

Two new columns, one called Parent Category and another called Sub-Category, were created by splitting Column R into the two separate columns.

![Outcomes per Parent Category](https://user-images.githubusercontent.com/120147552/209696867-3a11b28d-f7df-413e-8821-be8e7a7bba8a.png)

I created a new sheet titled "Outcomes by Parent Category" with a pivot table that analyzes the initial worksheet to count how many campaigns were successful, failed, canceled, or are currently live per category that could also be filtered by country.

![Outome by sub-category](https://user-images.githubusercontent.com/120147552/209697312-a4f1cf11-819d-4c89-ba82-2d42e1968b97.png)

I created a new sheet titled "Outcomes by Sub-Category" with a pivot table that analyzes your initial sheet to count how many campaigns were successful, failed, or canceled, or are currently live per sub-category and created a stacked-column pivot chart that can be filtered by country and parent category based on the table I created.

![Date created and ended](https://user-images.githubusercontent.com/120147552/209697591-8020b52f-4263-4ad1-82f8-61f22b1f4144.png)

I created two new columns Date Created Conversion and Date Ended Conversion and used the formula =((("Cell"/60)/60)/24)+DATE(1970,1,1) to convert the data contained in launched_at and deadline into Excel's date format.

![Outcomes over Time](https://user-images.githubusercontent.com/120147552/209698076-94c5d555-9896-4b6f-aef9-9a7f400b7e4a.png)

 I created a new sheet "Outcomes Over Time" with a pivot table that has a column of outcome, rows of Date Created Conversion, values based on the count of outcome, and filters based on parent category and Years. I then created a pivot-chart line graph that visualizes this new table.
 
 I created a report in Microsoft Word, and answer the following questions:
  
  Q1:Given the provided data, what are three conclusions that we can draw about crowdfunding campaigns?  
  A1: •	The Theater is the most supported crowdfunding campaign with plays being the most supported sub-category.
      •	Most campaigns are either successful or failed and only canceled less than 10% of the time.
      •	More Campaigns are successful in July than any other month of the year.
      
  Q2: What are some limitations of this dataset?
  
  A2: •	Not all categories are equally represented. For example: Journalism represents 4/1000 entries, where as Theater represents 344/1000 entries.
      •	The data is not all using the same currency of money.
      •	The countries are not represented equally with most of the data coming from the US.
      •	The years are not equally represented in the data set. For example: 2020 has 2 data points whereas the other years have between 81 and 107 data points.
      
 Q3: What are some other possible tables and/or graphs that we could create, and what additional value would they provide?

A3: •	We could create tables/graphs that show the number of backers and the average donation for each category/sub-category. This would provide an added value of              know how many people are offering support and how much on average each person is donating to each of the crowdfunding campaigns. This would help us to see              whether a small number of people are donating a lot of money or if many people are donating a smaller amount to the campaigns.
     •	Another possible table/graph we could create would show the backers count by country. This would help to show which country has more people contributing to             crowdfunding campaigns.
     •	We could also create a table/graph to show pledged/goal money based on category or sub-category. This would help to demonstrate which category or sub-                 category is getting pledged the most money regardless of outcome. For example: the ID 87 – Music category has a failed outcome but had 123,040 pledged                 whereas a lot of successful outcomes were for less pledged money. Perhaps the goal of each category plays a factor in the success rate.

## Crowfunding Goal Analysis

![Goal Analysis](https://user-images.githubusercontent.com/120147552/209698745-c011edf7-4cfc-42f2-822d-4da4424bea8f.png)

I Created a new sheet titled Goal Analysis and created 8 new columns and 12 new rows. 
I then used used the COUNTIFS() formula to count how many successful, failed, and canceled projects were created with goals within the ranges listed and populated the Number Successful, Number Failed, and Number Canceled columns with these data points. I pulled the data for this formula from the Crowdfunding sheet, from columns G and D. 
I then totaled the values in the Number Successful, Number Failed, and Number Canceled columns to populate the Total Projects column. Then, used a formula, find the percentage of projects that were successful, failed, or canceled per goal range.
Finally I created a line chart that graphs the relationship between a goal amount and its chances of success, failure, or cancellation.

## Statistical Analysis

![Stats workbook](https://user-images.githubusercontent.com/120147552/209699633-e0563226-f6e1-47cd-85c5-5d7fb743dbcb.png)

First, I created a new sheet that would become my workbook for this section of the assignment. I copied and pasted the columns Outcome and backers_count from the crowdfunding sheet. I then applied a filter to these columns so that I can filter out the data that I will need. First, I filtered for "successfull" outcomes and then copied those columns and pasted them in a new sheet titled Statistics Table. Then, I filtered for "failed" outcomes and copied and pasted those columns into the Statistics Table sheet.

![Statistics Table](https://user-images.githubusercontent.com/120147552/209700276-e0f67f2e-b3ad-4305-9bba-58125acf7d0b.png)

I then used Excel to evaluate the following values for successful campaigns, and then do the same for unsuccessful campaigns:
  The mean number of backers
  The median number of backers
  The minimum number of backers
  The maximum number of backers
  The variance of the number of backers
  The standard deviation of the number of backers
  
  In the Word document previously created, I answered the following points:
   
   Use your data to determine whether the mean or the median better summarizes the data.
            The Median would better summarize this set of data. This is because there are outliers within both the successful and failed backers_ count outcomes.               Therefore, the Mean is affected by the outliers and creates a bias to the outliers. To help better show this I have created boxplots for both the                   successful and failed outcomes by backers_count which demonstrates that the medians are not in the centre of the interquartile ranges and the means are             also pulled up from the median due to the outliers in the data set. 
            
![boxplots](https://user-images.githubusercontent.com/120147552/209701442-52564ed0-82a9-4d4e-a13b-8f95579da661.png)
                  
  Use your data to determine if there is more variability with successful or unsuccessful campaigns. Does this make sense? Why or why not?
            There is more variability in the successful campaigns. I believe that this makes sense because the standard deviation is larger for the successful                   outcomes than that the failed outcomes; this means that the data points in the successful outcomes are spread out more (further from the mean) than                 within the failed outcomes. 

