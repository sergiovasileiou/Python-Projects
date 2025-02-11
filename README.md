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

## Day 2: Task 1 - FizzBuzz Challenge

The goal of this task is to implement FizzBuzz in Python. The program should:
- Iterate through the integers from 1 to 100.
- Print "fizz" if a number is divisible by 3.
- Print "buzz" if a number is divisible by 5.
- Print "fizzbuzz" if a number is divisible by both 3 and 5.
- Otherwise, print the number.

[code]
for i in range(1, 101):
    if i % 3 == 0 and i % 5 == 0:
        print("fizzbuzz")
    elif i % 3 == 0:
        print("fizz")
    elif i % 5 == 0:
        print("buzz")
    else:
        print(i)
[/code]

---

## Day 3: Python Exercises

### Exercise 1: Loading and Exploring the Data

**Tasks:**
- Read the CSV file (`student.csv`) into a Pandas DataFrame.
- Display the first 5 rows.
- Print DataFrame information.
- Display summary statistics.

[code]
import pandas as pd

# Read CSV into DataFrame
df = pd.read_csv('student.csv')

# Display the first 5 rows
print(df.head(5))

# Display DataFrame info
print(df.info())

# Display summary statistics
print(df.describe())
[/code]

---

### Exercise 2: Indexing and Slicing

**Tasks:**
- Select the 'name' column.
- Select both 'name' and 'mark' columns.
- Display the first 3 rows.
- Display rows where 'class' is 'Four'.

[code]
# Select the 'name' column
print(df['name'])

# Select the 'name' and 'mark' columns
print(df[['name', 'mark']])

# Select the first 3 rows
print(df.head(3))

# Select all rows where 'class' is 'Four'
print(df[df['class'] == 'Four'])
[/code]

---

### Exercise 3: Data Manipulation

**Tasks:**
- Add a new column 'passed' to indicate if the student's mark is ≥ 60.
- Rename the 'mark' column to 'score'.
- Drop the 'passed' column.

[code]
# Add new column 'passed'
df['passed'] = df['mark'] >= 60

# Rename 'mark' column to 'score'
df.rename(columns={'mark': 'score'}, inplace=True)

# Drop the 'passed' column
df.drop(columns=['passed'], inplace=True)
[/code]

---

### Exercise 4: Aggregation and Grouping

**Tasks:**
- Group the DataFrame by 'class' and calculate the mean score.
- Count the number of students in each class.
- Calculate the average score for each gender.

[code]
# Group by 'class' and calculate mean score
grouped_class = df.groupby('class')['score'].mean()
print(grouped_class)

# Count the number of students in each class
counts = df['class'].value_counts()
print(counts)

# Calculate average score for each gender
avg_gender = df.groupby('gender')['score'].mean()
print(avg_gender)
[/code]

---

### Exercise 5: Advanced Operations

**Tasks:**
- Create a pivot table with 'class' as rows, 'gender' as columns, and 'score' (mark) as values.
- Create a new column 'grade' with:
  - 'A' for marks ≥ 85,
  - 'B' for marks 70-84,
  - 'C' for marks 60-69,
  - 'D' for marks below 60.
- Sort the DataFrame by 'score' in descending order and display the top 15 rows.

[code]
# Create the pivot table
pivot_table = df.pivot_table(values="score", index="class", columns="gender", aggfunc="mean")
print(pivot_table)

# Define function to assign grades
def assign_grade(score):
    if score >= 85:
        return "A"
    elif score >= 70:
        return "B"
    elif score >= 60:
        return "C"
    else:
        return "D"

# Apply function to create new 'grade' column
df['grade'] = df['score'].apply(assign_grade)

# Sort DataFrame by 'score' in descending order
df_sorted = df.sort_values(by=['score'], ascending=False)
print(df_sorted.head(15))
[/code]

---

### Exercise 6: Exporting Data

**Task:**
- Save the DataFrame (with the new 'grade' column) to a CSV file.

[code]
from google.colab import drive
drive.mount('/content/drive')

# Define the file path for saving
save_path = "/content/drive/My Drive/student_with_grades.csv"

# Save the DataFrame as a CSV file
df.to_csv(save_path, index=False)

# Print confirmation
print(f"File saved successfully at: {save_path}")
print(df.head())
[/code]

---

### Exercise 7: Visualising the Results

**Task:**  
(Optional) Create visualisations (e.g., a histogram of the scores).

[code]
import matplotlib.pyplot as plt

# Plot a histogram of the 'score' column
df['score'].hist(bins=10)
plt.title("Score Distribution")
plt.xlabel("Score")
plt.ylabel("Frequency")
plt.show()
[/code]

---

## Day 4: Task 1 - GDP Data Exploration

Using the `GDP (nominal) per Capita.csv` file, complete the following:

**Tasks:**
- Read the CSV file into a DataFrame called "df_gdp".
- Print the first 10 rows.
- Print the last 5 rows.
- Print the 'Country/Territory' and 'UN_Region' columns.

[code]
# Load GDP data into a DataFrame
df_gdp = pd.read_csv('GDP (nominal) per Capita.csv')

# Print the first 10 rows
print(df_gdp.head(10))

# Print the last 5 rows
print(df_gdp.tail(5))

# Print 'Country/Territory' and 'UN_Region' columns
print(df_gdp[['Country/Territory', 'UN_Region']])
[/code]

---

## Day 4: Task 2 - Group Project on GDP Data Analysis

Work as a group to further analyse the GDP data. Below is an example of filtering the data by UN Region.

[code]
# Filter rows where 'UN_Region' is 'Europe'
europe = df_gdp[df_gdp['UN_Region'] == 'Europe']
print("Europe Region Data:\n", europe.head())

# Filter rows where 'UN_Region' is 'Americas'
americas = df_gdp[df_gdp['UN_Region'] == 'Americas']
print("Americas Region Data:\n", americas.head())

# Filter rows where 'UN_Region' is 'Africa'
africa = df_gdp[df_gdp['UN_Region'] == 'Africa']
print("Africa Region Data:\n", africa.head())

# Filter rows where 'UN_Region' is 'Asia'
asia = df_gdp[df_gdp['UN_Region'] == 'Asia']
print("Asia Region Data:\n", asia.head())
[/code]

---

## Course Notes & Additional Information

- Detailed course notes and a revision guide are included in this workbook.
- Additional resources and links from the revision guide offer further information on these topics.

---

This README provides an in-depth overview of my Python workbook. All code blocks are enclosed within custom bracket tags (e.g., `[code]` and `[/code]`) so that they are displayed as text and not executed automatically. Enjoy reviewing the data-driven journey!
