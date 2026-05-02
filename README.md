# BrightLearn-Sql-Aggregates-And-Operators
A practical SQL project focused on aggregate functions, grouping, and advanced filtering using multiple datasets.
## 📚 Overview

This exercise builds on SQL basics and introduces aggregation, grouping, and advanced filtering techniques used in real-world data analysis.

### Key Topics Covered:
- Aggregate functions: COUNT, SUM, AVG, MIN, MAX
- GROUP BY and HAVING
- SQL operators: DISTINCT, BETWEEN, IN, NOT, AND, OR
- ORDER BY and LIMIT
- Aliasing using AS


## 🗂 Datasets

This exercise uses **5 tables**:

### 1. `students`
| student_id | name    | age | department |
|------------|---------|-----|------------|
| 1          | Alice   | 20  | IT         |
| 2          | Bob     | 22  | HR         |
| 3          | Charlie | 21  | IT         |
| 4          | Diana   | 23  | Finance    |
| 5          | Eve     | 22  | HR         |


### 2. `courses`
| course_id | course_name  | department | credits |
|-----------|--------------|------------|---------|
| 101       | SQL Basics   | IT         | 3       |
| 102       | Python       | IT         | 4       |
| 103       | Data Science | IT         | 4       |
| 104       | Excel        | Finance    | 2       |
| 105       | Statistics   | HR         | 3       |


### 3. `enrollments`
| enrollment_id | student_id | course_id | grade |
|---------------|------------|------------|--------|
| 1             | 1          | 101        | 85     |
| 2             | 2          | 102        | 78     |
| 3             | 3          | 103        | 90     |
| 4             | 4          | 104        | 88     |
| 5             | 5          | 105        | 82     |


### 4. `salaries`
| employee_id | name  | department | salary | bonus |
|-------------|-------|------------|--------|--------|
| 1           | Tom   | IT         | 60000  | 5000   |
| 2           | Jerry | HR         | 55000  | 4000   |
| 3           | Spike | Finance    | 70000  | 6000   |
| 4           | Tyke  | IT         | 62000  | 5500   |
| 5           | Butch | HR         | 54000  | 3500   |


### 5. `projects`
| project_id | project_name    | department | budget |
|------------|-----------------|------------|---------|
| 1          | AI App          | IT         | 120000  |
| 2          | Payroll System  | Finance    | 80000   |
| 3          | Dashboard       | IT         | 150000  |
| 4          | Website         | Marketing  | 60000   |
| 5          | HR Portal       | HR         | 50000   |


## 🧠 Learning Objectives

By completing this exercise, I practiced how to:
- Use aggregate functions to summarize data
- Group data and filter grouped results
- Apply advanced filtering techniques
- Work with multiple tables
- Create meaningful query outputs using aliases


## 📝 Exercise Breakdown

### 🔹 Students Table
1. Distinct departments  
2. Average age per department  
3. Departments with more than 1 student  
4. Students aged between 21 and 23  
5. IT or HR students older than 21  


### 🔹 Courses Table
6. Total credits per department (with HAVING)  
7. Courses not equal to 4 credits  
8. Top 3 courses by credits  


### 🔹 Enrollments Table
9. Max, min, and average grade  
10. Enrollment count per course  


### 🔹 Salaries Table
11. Total salary and bonus per department  
12. Departments with average salary above 55,000  
13. Employees with total compensation above 60,000  


### 🔹 Projects Table
14. Total and average budget per department (HAVING condition)  
15. Projects within a budget range excluding Marketing  


## 💻 Example Query

```sql
SELECT department, AVG(age) AS avg_age
FROM students
GROUP BY department;
