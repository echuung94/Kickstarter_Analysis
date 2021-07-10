# Kickstarter Analysis 
Performing analysis on Kickstarter data to uncover trends

## Overview of Project
Louise's play, Fever, had come close to its fundraising goal. The purpose of this challenge was to assist Louise in 
determining how different campaigns fared in relation to their launch date and their funding goals. 
To provide Louise a visual summary of the data, line graphs were used, as they are useful in showing the data variables and trends very clearly, and are also used
to compare changes for more than one group over the same period of time. 

## Analysis and Challenges 

### Analysis of Outcomes Based on Launch Date

To examine the outcomes of the plays, pivot tables and graphing in Excel was used for visualiation based on launch date. The Year()
function was initially used to extract the year from the "DateCreatedConversion" column. After the "Years" column was created, a pivot
table was created in a new worksheet. The pivot table was filtered on "Parent Category" and "Years", the launched column filtered
for rows, and the outcomes column filtered for columns and values. The column labels were then filtered to show only "successful,"
"failed," and "canceled." The "Row Labels" column was then grouped to show the months of the year. Within the pivot table, 
the "Parent Category" was filtered so only the data for "theater" was shown. Using  the filtered pivot table, a line chart 
was created to show the number of successful, failed, and canceled project by month. 

![Theater_Outcomes_by_Launch](https://github.com/echuung94/kickstarter-analysis/blob/main/Resources/Theater_Outcomes_vs_Launch.png)
 

### Analysis of Outcomes Based on Goals

To analyze the outcomes based on goals,  the Countif() function was used to collect the outcome and goal data. In a new sheet, several
columns were created with dollar amount-ranges so that the data can be grouped by their goal amount. The Countif() function was used 
to populate the "Number Successful," "Number failed," and "Number canceled" by filtering on the Kickstarter "outcome" column, the "goal" 
column using the ranges given, and the "subcategory" column with "plays" as the criteria. The sum() function was used
to populate the "Total Projects" column with the ranges calculated for the number of successful, failed, and canceled projects. 
The percentage of each project was calculated for all the goal ranges as well. A line chart was then created to visualize the relationship
between the goal-amount ranges (x-axis) and the percentage of the projects (y-axis).

![Outcomes_Based_on_Goals](https://github.com/echuung94/kickstarter-analysis/blob/main/Resources/Outcomes_Based_on_Goals.png)

### Challenges and Difficulties Encountered

One challenge that I encountered was trying to display the correct date on the pivot table once the launched column was filtered for rows. 
Before all the data showed up in the chart, there was a "blank" row that hid most of the dates. I was unsure of why most of the data was 
hidden until I went back to the original Kickstarter worksheet and noticed that when the formula used to change the epoch time to date
was dragged down the column, there was so much data, excel could not grab all the dates from the "launched_at" column. I manually went 
down the column to make sure all the blanks were filled with the correct date. 

## Results

1. What are two conclusions you can draw about the Outcomes based on Launch Date?</br>
Louise's play, Fever, was most the successful in the month of May with 111 shows although it was the highest amount of failed shows; the
play had failed 55 times in May. 
After the increase in shows from April to May, the numbers of successful shows started to gradually decrease until September while the 
number of failed shows remained fairly consistent.  

2. What can you conclude about the Outcomes based on Goals?</br>
We can conclude that based on the table and line chart, the goal ranging "1000 to 4000," showed the highest number of successful 
projects with 388 projects and a percentage rate of 73%. The goal, "less than 1000," shows 141 successful projects with the highest 
percentage rate of 76%. 

3. What are some limitations of this dataset?</br>
Since data is a human creation,  it is possible that there could be limitations of this dataset. One possible limitation could be 
that the data is incomplete. There could be missing values for the amount of times a play was shown within a day or month.
Extreme values may be another possible limitation of this dataset. For example, the goal amount could have been calculated 
incorrectly showing an increasingly large amount acheived. That would cause the inability to accuarately assess the performance and sales
of that particular day or month.  

4. What are some other possible tables and/or graphs that we could create?</br>
A possible graph that could have been created would be a bar graph. A bar graph is easy to understand and can show what changes over time,
If we wanted to compare a particular subcategory to another and see how the outcome over a period of time, a possible graph that 
could have been created would be a bar graph. A bar graph is easy to understand and can show what changes over time. Viewers 
can easily see how the two categories performed within the time frame and view whether numbers increased or decreased over time. 
