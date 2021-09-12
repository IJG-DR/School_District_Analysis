# School District Analysis

## Project Overview

Maria, the chief data scientist for a school city system, is responsible for analyzing standarized testing results used by the School Board and the School Superintendent in evaluating the efficacy of these tests and determining budgetary allocation among the schools.

The School Board has notified Maria and her supervisor that the data file containing all student scores shoes evidence of academic dishonesty, specifically, reading and math scores for ninth graders at the Thomas High School.

Maria has requested our assistance in repeating the school district analysis by excluding the scores for Thomas High School ninth graders and comparing the results against her earlier analysis.

## Methodology

Utilizing the pandas numpy library and python coding on jupyter notebooks, and using the same development environment other analysts on the team have on their computers, we reproduced the school analysis excluding the math and reading scores for nith graders at Thomas High School.

Our analysis utilized the same data files, mainly the clean_students_complete.csv and the schools_complete.csv data files (see Resources folder).

We utilized several pandas and python methods to summarize the data and calculate relevant averages for scores at different levels. These methods included the loc() method as well as the groupby() and mean () methods. The data was then presented in summary data frames.

In reproducing the analysis, we followed the same methodology as the original project in order to have comparable results. However, we believe that the methodology used to calculate the averages for some of the summary data frames is statistically incorrect. We have added a note in our summary of findings which elaborates on this issue.

## Schools District Analysis Results

### Replacing Ninth-Grade Reading and Math Scores

In order to remove the ninth grade Thomas High Schools scores, we performed a loc() search for all students that met two conditions, school is Thomas High School and grade is ninth grade, and ran the code first to replace reading scores for empty data (Nan's), and then repurposed the same code to replace math scores for Nan's as well. Below is the segment of code we utilized:

![Replace Thomas High School 9th grade code.](Resources/Images/Replace_THS_9th_grade_code.png)


To verify that the code was effective, we listed a few lines of the data to make sure that only the score fields were changed. Below is the printout of the sample records in the data:

![Replace Thomas High School 9th grade DataFrame.](Resources/Images/Replace_THS_9th_grade_DataFrame.png)


### Recreating the School District Analysis

To recreate the School District Analysis using the modified ninth grade data, we generated the following data frames which we compared to the initial School Distric Analysis results.

* The district summary
* The school summary
* The top 5 performing schools, based on the overall passing rate
* The bottom 5 performing schools, based on the overall passing rate
* The average math score for each grade level from each school
* The average reading score for each grade level from each school
* The scores by school spending per student 
* The scores by school size
* The scores by school type

The following tables showed the compared before and after results.

#### (1) District Summary

To update the district summary, we recalculated the total student count by subtracting the number of ninth-grade students in Thomas High School (461) from the total student count (_____), then you'll recalculate the passing math and passing reading percentages, and the overall passing percentage with the recalculated total student count. The following tables show the before and after District Summary data frames, highliting any observed differences.

##### District Summary - Before
![District Summary before.](Resources/Images/1_District_Summary_BEFORE.png)


##### District Summary - After
![District Summary after.](Resources/Images/1_District_Summary_AFTER.png)


#### (2) School Summary

Likewise, we updated the school summary based on the adjusted number of students after subtracting the Thomas High School ninth-grade student count. The following tables show the before and after Schools Summary data frames, highliting any observed differences.

##### School Summary - Before
![School Summary before.](Resources/Images/2_School_Summary_BEFORE.png)

##### School Summary - After
![School Summary after.](Resources/Images/2_School_Summary_AFTER.png)


#### (3) Top 5 Performing Schools

##### Top Performing Schools - before
![Top Performing before.](Resources/Images/3_Top_Performing_BEFORE.png)

##### Top Performing Schools - after
![Top Performing after.](Resources/Images/3_Top_Performing_AFTER.png)


#### (4) Bottom 5 Performing Schools

##### Bottom Performing Schools - before
![Bottom Performing before.](Resources/Images/4_Bottom_Performing_BEFORE.png)

##### Bottom Performing Schools - after
![Bottom Performing after.](Resources/Images/4_Bottom_Performing_AFTER.png)


#### (5) Math Scores by Grade

##### Math Scores by grade - before
![Math Scores per grade per school before.](Resources/Images/5_Math_per_Grade-School_BEFORE.png)

##### Math Scores by grade - after
![Math Scores per grade per school after.](Resources/Images/5_Math_per_Grade-School_AFTER.png)


#### (6) Reading Scores by Grade


##### Readomg Scores by grade - before
![Reading Scores per grade per school before.](Resources/Images/6_Reading_per_Grade-School_BEFORE.png)

##### Reading Scores by grade - after
![Reading Scores per grade per school after.](Resources/Images/6_Reading_per_Grade-School_AFTER.png)


#### (7) Scores by Spending

##### Scores by Spending - before
![Scores by spending before.](Resources/Images/7_Scores_by_Spending_BEFORE.png)

##### Scores by Spending - after
![Scores by spending after.](Resources/Images/7_Scores_by_Spending_AFTER.png)


#### (8) Scores by Size

##### Scores by Size - before
![Scores by size before.](Resources/Images/8_Scores_by_Size_BEFORE.png)

##### Scores by Size - after
![Scores by size after.](Resources/Images/8_Scores_by_Size_AFTER.png)


#### (9) Scores by Type

##### Scores by Type - before
![Scores by type before.](Resources/Images/8_Scores_by_Type_BEFORE.png)

##### Scores by Type - after
![Scores by type after.](Resources/Images/8_Scores_by_Type_AFTER.png)


## Summary



