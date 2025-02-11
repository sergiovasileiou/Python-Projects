# Data Technician Workbook: Python Fundamentals 🐍📊

**Author:** Sergios Vasileiou  
**Course Date:** 2/2/25  

This repository contains my Python-based exercises and projects as part of the Data Technician course. It covers Python programming fundamentals, data exploration and manipulation with Pandas, and practical data analysis using real-world datasets. Enjoy exploring the code challenges and solutions! 🚀

## Table of Contents
- [Day 2: Task 1 - FizzBuzz Challenge 🐝](#day-2-task-1---fizzbuzz-challenge-🐝)
- [Day 3: Python and Pandas Exercises 🐼](#day-3-python-and-pandas-exercises-🐼)
  - [Exercise 1: Loading and Exploring Data 💾](#exercise-1-loading-and-exploring-data-💾)
  - [Exercise 2: Indexing and Slicing 📑](#exercise-2-indexing-and-slicing-📑)
  - [Exercise 3: Data Manipulation 🔧](#exercise-3-data-manipulation-🔧)
  - [Exercise 4: Aggregation and Grouping 📊](#exercise-4-aggregation-and-grouping-📊)
  - [Exercise 5: Advanced Operations 🔝](#exercise-5-advanced-operations-🔝)
  - [Exercise 6: Exporting Data 💾➡️CSV](#exercise-6-exporting-data-💾➡️csv)
  - [Exercise 7: Visualising Results 🎨](#exercise-7-visualising-results-🎨)
- [Day 4: Tasks with GDP Data 🌍](#day-4-tasks-with-gdp-data-🌍)
  - [Task 1: GDP Data Exploration 🔎](#task-1-gdp-data-exploration-🔎)
  - [Task 2: Group Project on GDP Data Analysis 🤝](#task-2-group-project-on-gdp-data-analysis-🤝)
- [Course Notes & Additional Information 📚](#course-notes--additional-information-📚)

---
## Day 2: FizzBuzz Challenge

- **Goal:**  
  Implement the classic FizzBuzz algorithm using Python, ensuring that numbers divisible by 3 print "fizz," by 5 print "buzz," and by both print "fizzbuzz;" all others print the number.
  
- **What Was Achieved:**  
  A working script that iterated through numbers 1–100 correctly handling the conditional logic.
  
- **Key Takeaway:**  
  Reinforced understanding of loops, conditional statements, and modulo operations in Python.

---

## Day 3: Python & Pandas Exercises

### Exercise 1: Loading and Exploring Data
- **Goal:**  
  Import data from a CSV file (student.csv) and perform initial exploration.
  
- **What Was Achieved:**  
  Read the CSV into a Pandas DataFrame; displayed the first few rows; printed DataFrame information and summary statistics.
  
- **Key Takeaway:**  
  Gained hands-on experience with file I/O and fundamental DataFrame methods for data inspection.

### Exercise 2: Indexing and Slicing
- **Goal:**  
  Practice selecting specific columns and rows from the DataFrame.
  
- **What Was Achieved:**  
  Successfully retrieved specific columns (e.g., 'name' and 'mark') and filtered rows based on conditions (e.g., class equal to "Four").
  
- **Key Takeaway:**  
  Solidified skills in indexing and slicing which are critical for data manipulation.

### Exercise 3: Data Manipulation
- **Goal:**  
  Modify the DataFrame through adding a new column, renaming existing columns, and dropping unnecessary ones.
  
- **What Was Achieved:**  
  Added a 'passed' column (mark ≥ 60), renamed the 'mark' column to 'score,' and removed the 'passed' column afterward.
  
- **Key Takeaway:**  
  Enhanced proficiency in modifying and adjusting DataFrame structures for cleaner data representation.

### Exercise 4: Aggregation and Grouping
- **Goal:**  
  Summarize data by grouping it based on categorical fields.
  
- **What Was Achieved:**  
  Grouped the data by 'class' to calculate mean scores, counted the number of students per group, and computed average scores for different genders.
  
- **Key Takeaway:**  
  Developed the ability to aggregate data effectively, an essential step in exploratory data analysis.

### Exercise 5: Advanced Operations
- **Goal:**  
  Create a pivot table for a deeper comparative analysis and assign letter grades based on score ranges.
  
- **What Was Achieved:**  
  Formulated a pivot table to view average scores across classes and genders, applied custom logic to assign grades, and sorted the DataFrame by scores.
  
- **Key Takeaway:**  
  Demonstrated advanced data reshaping techniques and business logic application with Pandas.

### Exercise 6: Exporting Data
- **Goal:**  
  Export the cleaned and enriched DataFrame to a new CSV file.
  
- **What Was Achieved:**  
  Successfully saved the DataFrame (including the new grade column) to an external CSV—ensuring reproducibility and data persistence.
  
- **Key Takeaway:**  
  Highlighted the importance of data export for sharing results and further analysis.

### Exercise 7: Visualising the Results (Optional)
- **Goal:**  
  Create visual representations (such as histograms) to display the distribution of scores.
  
- **What Was Achieved:**  
  Generated insightful plots that illustrated the score distribution, aiding the interpretation of data trends.
  
- **Key Takeaway:**  
  Introduced the basics of data visualization, underscoring its role in exploratory data analysis.

---

## Day 4: GDP Data Exploration

### Task 1: GDP Data Exploration
- **Goal:**  
  Load the "GDP (nominal) per Capita.csv" dataset and perform basic inspection.
  
- **What Was Achieved:**  
  Read the GDP CSV into a DataFrame; viewed the top 10 and bottom 5 rows; and extracted key columns like 'Country/Territory' and 'UN_Region.'
  
- **Key Takeaway:**  
  Applied learned data exploration techniques to a real-world economic dataset.

### Task 2: Group Project on GDP Data Analysis
- **Goal:**  
  Collaboratively analyze the GDP dataset to uncover regional trends.
  
- **What Was Achieved:**  
  Filtered and segmented the data by geographic regions, and explored various visual and statistical analyses as a group.
  
- **Key Takeaway:**  
  Improved teamwork and collaborative data analysis skills while reinforcing the extraction of actionable insights.

---

## Course Notes & Additional Information

- **Course Notes:**  
  Detailed notes were maintained throughout the exercises to capture essential concepts and troubleshooting tips.
  
- **Additional Resources:**  
  Supplementary links and guides from the revision materials provided further insights into advanced topics.

- **Overall Takeaway:**  
  This workbook strengthened my proficiency in Python programming and data manipulation with Pandas while cementing both individual and collaborative data analysis practices.
