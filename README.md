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

1. Distric Summary
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



### Thomas High School Performance
![Screenshot](https://github.com/Sborresch/School_Districts_Analysis/blob/main/per_school_summary.png)

### Math & Reading Scores By Grade
![Screenshot](https://github.com/Sborresch/School_Districts_Analysis/blob/main/per_school_summary.png)

### Scores By School Spending

### Scores By School Size

### Scores By School Type

## Summary
