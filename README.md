# School District Analysis
## Overview
### Purpose

  Maria, Chief Data Scientist for a city school district, reached out to the data analytics team to discuss proficiency standards for the State Board of Education. Maria was able to collect two CSV data files called [schools_complete.csv](https://github.com/Sborresch/School_Districts_Analysis/blob/main/Resources/schools_complete.csv) and [students_complete.csv](https://github.com/Sborresch/School_Districts_Analysis/blob/main/Resources/students_complete.csv). These files contain various data at the school and student level including math scores, reading scores, student ID, school ID, and much more. Maria has tasked the data analytics team to clean, organize, and find patterns and trends in the data to aid in the State Board of Education's decision making process for school budget allocation.

### Background
  During the data analysis process, Maria informed the data analytics team that there was a descrepency in the [students_complete.csv](https://github.com/Sborresch/School_Districts_Analysis/blob/main/Resources/students_complete.csv) file. It was found that Thomas High School 9th grade students math and reading scores were inncorrect for some unknown reason. In this situation the data analytics team has three options:

1. Do nothing
2. Remove the rows with corrupted data
3. Fill in the values with NaN

It was decided that the data analytics team will fill in the corrupted data values with the string "NaN". Once the corrupted values were fixed, the analysis had to be re-ran to find the key metrics the School Board of Education requested for decision making purposes. The key metrics are listed below and in more detail in the Results section of this analysis:

1. District Summary
2. School Summary
3. Thomas High School Performance
4. Math & Reading Scores By Grade
5. Scores By School Spending
6. Scores By School Size
7. Scores By School Type

## Results

Below is a comparison analysis between the results prior to the corrupted data being fixed and the results after.

### District Summary
#### Updated Results
![Screenshot](https://github.com/Sborresch/School_Districts_Analysis/blob/main/district_summary.png)

Above is an image of the district summary dataframe that the data analytics team created using Python programing language, Pandas Distribution, and Jupyter Notebook. This details a quick overview of the aggregated data where there are 15 total schools, 39170 students, a budget of $24 million, and the following test proficency scores:

- Average Math Score = 78.9
- Average Reading Score = 81.9
- % Passing Math = 74.8
- % Passing Reading = 85.7
- % Overall Passing = 64.9

#### Corrupted Results

This details a quick overview of the aggregated data where there are 15 total schools, 39170 students, a budget of $24 million, and the following test proficency scores:

- Average Math Score = 79.0
- Average Reading Score = 82.0
- % Passing Math = 75.0
- % Passing Reading = 86.0
- % Overall Passing = 65.1

#### Change

Based on the above results from the updated and the corrupted versions of data, there was minor changes in the proficency scores. After the Thomas High School ommited 9th grade math and reading scores the following categories decreased by one point average math score, average reading score, % passing math, % passing reading and % overall passing. This is likely due to the change in count for total students that passed math and reading that served as the denominator to all calculations.

### School Summary
![Screenshot](https://github.com/Sborresch/School_Districts_Analysis/blob/main/per_school_summary.png)

The above image is a image of the data frame that details both the categores from the student and school CSV files, merged on the School ID category, and by each of the 15 high schools. 

#### Thomas High School Performance

Based on the image above, Thomas High School performed quite well given the corrupted data. On both the updated and corrupted results, school type, total students, total budget and per student budget did not change because only the test scores were removed, not the entire row values. Therefore keeping the count of students the same. However, the test score categories were different. Below are the findings both before and after the corrupted data was fixed:

corrupted:updated
- Average Math Score = 83.4: 83.4
- Average Reading Score = 84.0: 84
- % Passing Math = 93.2: 93.2
- % Passing Reading = 97.3: 97.0
- % Overall Passing = 91.0: 91.0

The only difference in the data after changing the Thomas High School corrupted data values to NaN is in the % Passing Reading. There was a negative change in the tenth decimal point which overall shows a small decrease in Thomas High School proficency.

#### Top 5 Performing Schools
![Screenshot](https://github.com/Sborresch/School_Districts_Analysis/blob/main/top_five_schools.png)

There was no change in the ranking of the top 5 performing schools between the corrupted data results and the updated data results. Both dataframes showed the following schools ranked by performance from first to fith:

1. Cabrera High School
2. Thomas High School
3. Griffin High School
4. Wilson High School
5. Pena High School

#### Bottom 5 Performing Schools
![Screenshot](https://github.com/Sborresch/School_Districts_Analysis/blob/main/bottom_five_schools.png)

There was no change in the ranking of the bottom 5 performing schools between the corrupted data results and the updated data results. Both dataframes showed the following schools ranked by performance from first to fith:

1. Rodriguez High School
2. Figueroa High School
3. Huang High School
4. Hernandez High School
5. Johnson High School

### Math & Reading Scores By Grade
#### Math Scores By Grade
![Screenshot](https://github.com/Sborresch/School_Districts_Analysis/blob/main/math_avg_per_school_per_grade.png)

The above dataframe was put together by the data analytics team for the State Board of Education so that they can identify which grades are performing highest or lowest in math proficency by high school. This should allow each high school to identify which level of students may be struggling, out performing, or performing at average rates. This can promote certain resources to different grade levels. When any low performing grade has better resources score higher on the math proficiency tests, the high schools overall % average will increase.

There was no statistical change in the values between the corrupted and updated results.

#### Reading Scores By Grade
![Screenshot](https://github.com/Sborresch/School_Districts_Analysis/blob/main/reading_avg_per_school_per_grade.png)

The above dataframe was put together by the data analytics team for the State Board of Education so that they can identify which grades are performing highest or lowest in reading proficency by high school. This should allow each high school to identify which level of students may be struggling, out performing, or performing at average rates. This can promote certain resources to different grade levels. When any low performing grade has better resources score higher on the reading proficiency tests, the high schools overall % average will increase.

There was no statistical change in the values between the corrupted and updated results.

### Scores By School Spending
![Screenshot](https://github.com/Sborresch/School_Districts_Analysis/blob/main/scores_per_schoolspending_per_student.png)

The above dataframe was put together by the data analytics team for the State Board of Education so that they could identify if the spending per student effects proficency in students. Based on the dataframe the percent of overall passing was incrementally higher as less money was provided. In the <$586 spending per student category it had the highest overall passing, % passing math, % passing reading, average reading score, and average math score. It can be determined that there is more spending per student for high schools and students who do not perform as high as other to provide better resources to improve said test scores

There was no statistical change in the values between the corrupted and updated results.

### Scores By School Size
![Screenshot](https://github.com/Sborresch/School_Districts_Analysis/blob/main/scores_per_school_size.png)

The above dataframe was put together for the State Board of Education so that they could identify if the size of the school made any statistical difference on proficency in the students. Based on the dataframe schools that are classified as small or medium, which is less than 2000 students, had similar proficiency results across the board. Of those categories small and medicum schools obtained a B and A average. As the schools got larger, 2000-5000 students, the proficency in students decreased across the board especially in the % overall passing. This can show that schools with higher population counts have lower proficency possiby due to resource allocation. As these schools should also be receiving the most spending per student based on the Scores By School Spending dataframe results.

There was no statistical change in the values between the corrupted and updated results.

### Scores By School Type
![Screenshot](https://github.com/Sborresch/School_Districts_Analysis/blob/main/scores_per_school%2Btype.png)

The above dataframe was put together for the State Board of Education so that they could identify if the school type has any statistical difference on the proficency in the students. Based on the dataframe schools that have the school type of charter perform better across the board in all proficiency categories. Discrict school types have the largest range between comparing any data categories in this analysis thus far. The biggest range is between % overall passing category with districts value of 54 and charters value of 90. This can show that schools that are in districts may have fewer resources or disadvantages and should be investigated further to bridge the large gaps.

There was no statistical change in the values between the corrupted and updated results.

## Summary
This project was a great opportunity for the data analytics team to work on with Maria and the State Board of Education. There was a bump in the road that caused a second identical analysis of the data except the data source had a small amount of different data. For this reason there was not a high level of statistical difference between the uncorrected results and the corrected results. However, it is important to note there were some differences including:
- Changes in Thomas High School proficeny performance
- The district summary findings in proficency performance
- Changes of value in the data source students_complete.csv
- Changes in the math and reading scores for Thomas High School basged on grade, specifically 9th grade

