# Kickstarting with Excel

## Overview of Project

### Purpose
The purpose of this project was to increase familiarity and skill with Microsoft Excel. By testing a variety of methods including calculation formulas, lookups, and pivot tables, we internalized how to search across data sets within a single workbook and turn the resulting information into actionable analyses.

## Analysis and Challenges
I performed my analysis in two distinctly different fashions:
 - Assessing outcomes by launch date was primarily pivot table manipulation
 - Assessing outcomes by goal was driven by formulaic calculations

### Analysis of Outcomes Based on Launch Date
The launch date outcome analysis relied on creating a pivot table. After creating the "YEAR" column as instructed, the pivot table setup was relatively straightforward:

![Pivot Table](pivot_table_example)

### Analysis of Outcomes Based on Goals
On the other hand, our goal-based outcome analysis eschewed pivot tables for formulas. 

![Table from Formulas](../Desktop/GW%20Classwork/Module%201%20-%20Crowdfunding%20Analysis/Resources/Countifs%20example.png)

Throughout that sheet, most of the formulas were some variation of:
```
=COUNTIFS(Kickstarter!$F:$F,"successful",Kickstarter!$D:$D,"<1000")

=SUM(B2:D2)

=B2/E2*100
```

### Challenges and Difficulties Encountered
The biggest challenge I encountered was refreshing my memory on the syntax for COUNTIFS. Since Excel is generally object based, I assumed that the criteria for each range would need to be formatted as:
```
Cell_Coordinates = Criteria
```
However, upon review the criteria stood alone as simply "criteria" (e.g. "<1000").

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
  1. May and June seem to be the best months to launch a theater campaign. Though failures peaked in May as well, their increase there paled in comparison to the number of successful fundraising efforts.
  2. October and December returned the lowest rates of success; December was the only month in which less than half of campaigns were successful.
- What can you conclude about the Outcomes based on Goals?
  1. Not surprisingly, lower goals were reached more often their more-expensive counterparts. 
  2. Groups of campaigns seeking less than 20,000 were more likely to succeed than fail; and there was a surprisingly similar relationship across the range spanning 35,000-44,999. In any other group, a campaign was more likely to fail than succeed.
- What are some limitations of this dataset?
  1. We don't know the results of the live campaigns which could affect the data one way or the other (it may less than 2% of all campaigns but the impact could be more significant at the month or goal level).
  2. Theater campaigns were undertaken in nearly 20 different countries so unless we are to assume that the currency values have all been standardized (presumably to American dollars), we might be misrepresenting some of monetary values.
- What are some other possible tables and/or graphs that we could create?
  * Though a line graph seems like the clear choice for evaluating outcomes by launch date (as it generally would for most cases in which the x-axis represents chronological time), it's possible that a bar chart or histogram would have been a more valuable visual representation of outcomes based on goal.
  
  ![Potential Bar Chart](../Desktop/GW%20Classwork/Module%201%20-%20Crowdfunding%20Analysis/Resources/Potential%20bar%20chart.png)
