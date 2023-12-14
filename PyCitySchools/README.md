# pandas-Challenge

                Module 4 - Pandas - Challenge

                         Jeremy Hooper

Introduction

The Pandas Challenge tests the UWA Data Analysis Bootcamp participants' knowledge of Python Pandas Library in processing real-life data. This describes how I prepared the code in pandas for the Py City Scools challenge and interpreted the results. I prepared the code in Jupyter Notebook. I have annotated the code accordingly in each cell and followed the instructions provided in the assignment instructions.

Data Preparation

The data provided was 2 csv files, namely 'schools_complete.csv' and 'students_complete.csv'. The data provided information regarding the 15 schools' size, budget, whether they were Government or Independent schools, the students attending these schools, and their maths and reading scores. 

Description of Data Processing

1. I began the code by importing the pandas and pathlib dependencies, followed by reading the two csv data files schools_complete.csv, and students_complete.csv. I merged the two data files (left merge) in a merged DataFram called school_data_complete.

I examined the DataFrame and found it had 39170 rows and 11 columns. After that, I reviewed the column names and data types. I found all of the columns holding numerical data were dtype int64. I have left the data examination code on the coding sheet.

2  After the initial preparation, I prepared a Local Government Area (LGA) 
Summary. This included processing and preparing the academic maths and reading scores to calculate the percentage of students with passing scores. After completing the calculations, I brought all the results together in a DataFrame called lga_summary_df. The output said there were 15 unique schools with 39,170 students and a total budget of $24,649,428. The average maths score was 70.3, the average reading score was 69.98, the % passing maths was 86.08%, the % passing reading was 84.25%, and the % overall passing was 72.81%. Not that I used the school_DataFrame to calculate the total budget.

3. I followed the instructions to prepare a DataFrame summarising key metrics about each school. At first, I created a DataFrame school_groups_df as a copy of the school_data_complete grouped on 'school_name'. I used this DataFrame as the data source required for the calculations. 'Per Student Budget amount was calculated at this stage. I created the DataFrame schoo_summary_df from the processing and calculations at this stage. I output five lines to confirm the code worked.

4. Top Performing Schools (By % Overall Passing). I created a DataFrame top_schools_df from school_summary_df. I first selected the columns I wanted to show in the output and then sorted the data using 'sort_values(by='% Overall Passing'). I output the top 5 rows using the head() function. Similarly, I calculated the Bottom performing schools and output the bottom 5 schools in a DataFrame called 'bottom_schools_df. In both cases, I restricted the columns to the school name, School Type, Per Student Budget, % Passing Maths, % Passing Reading, and % Passing Overall.

5.  Maths and reading Scores by Year - I created two DataFrames, 'average_maths_scores_by_year_df' and 'average read_scores by year' to show these scores for Years 9, 10, 11, and 12 for the students of each of the 15 schools. These scores show a consistency of maths scores within schools of the 4 years while showing a variation of up to 4% between the schools. Reading scores have a variation of up to about 7% between schools.

6.  Scores by School Spending - I performed this exercise by binning the 'Per Student Budget' spend for each school using the bins set out in the instructions of '< $585', '$585-$630', $630-$645', and $645-$680. I called the resulting DataFrame roupled_psbudget_df. Interestingly, there appears to be a negative correlation between the per-student budget spend and the spend. 

7.  Scores by School Size - I performed this exercise by binning the 'Total Students' numbers into 'Small ( up to 1000)', 'Medium (between 1000 and 2000)', and Large (between 2000 and 5000). I called the resulting DataFrame 'grouped_schoolsize_df'.  The smaller schools performed better than the larger ones.  

8.  Scores by School Type - I grouped the academic data by School Types, Government, and Independent. I called the resulting DataFrame 'grouped_stype_df. The tables show that Independent Schools outperform Government schools.

Findings and Discussion

1.  The data provided budgeting and academic statistics for 15 independent and government schools of different sizes.

2.  'The Top Performing Schools' by '% overall passing rate' were dominated by Independent Schools, with 5 schools in the top 7 or 3 in the top 5.

3.  The 'Bottom Performing Schools' by '% overall passing rate' were a mix of Government and Independent Schools.

4.  'The Maths Score by Year' chart generally showed that scores in each school were similar each year over the four years. This suggests that the teaching style of each school affected the maths scores. I assumed that each school taught the same or similar syllabus.

5.  The 'Reading Score by Year' chart showed a similar trend. I found that the same schools were higher or lower overall in maths and reading. This could be due to socio-economic reasons in the different school zones.

5.  The 'Scores by School Spending (Per Student)' chart showed little correlation between the 'Per Student Budget' and academic achievement.

6.  The 'Scores by School Size' chart correlates with school size(student numbers) and academic achievement. The smaller the school, the better the achievement. The lower number of smaller schools could also influence this.

7.  The 'Scores by School Type' chart strongly correlates with the type of school. Independent schools outperformed government schools.

Two Conclusions I Believe to be Correct 

1.  Smaller schools have better academic performance than larger schools.

2.  Independent Schools have better academic performance than Government schools.

References

In this challenge, I received help from the following sources:

Course Notes
Pandas Tutorial - https://www.w3schools.com/python/pandas/default.asp
Community Tutorials -  https://pandas.pydata.org/pandas-docs/stable/getting_started/tutorials.html
Pandas, a Complete Introduction - https://www.learndatasci.com/tutorials/python-pandas-tutorial-complete-introduction-for-beginners/
Pandas Tutorials, Pandas Data Analysis in Python (11 Videos) - Corey Schafer - Youtube.
ChatGPT.
