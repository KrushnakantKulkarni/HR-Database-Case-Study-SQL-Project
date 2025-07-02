# HR-Database-Case-Study-SQL-Project
This repository showcases an advanced SQL case study involving a normalized HR (Human Resources) database. It demonstrates how to create a complete relational database schema, enforce foreign key constraints, populate tables, and run analytical queries on a simulated HR system.
🗂️ Table of Contents
📌 Overview

🧮 Database Schema

📋 Key Objectives

📦 Dataset Structure

🔍 Example SQL Queries

🚀 Getting Started

📎 License

📌 Overview
This project involves:

Creating a full HR schema with multiple interconnected tables

Inserting realistic employee, department, and job data

Using SQL joins, constraints, and views

Answering HR-related business queries to gain meaningful insights

It mirrors real-world corporate HR systems and can be used for data analysis, practice, and interview preparation.

🧮 Database Schema
The HR database consists of the following tables:

Table Name	Description
regions	Stores global regions like Europe, Asia, etc.
countries	Contains countries and their region IDs
locations	Includes physical office locations
departments	Company departments and their locations
jobs	Job titles with salary ranges
employees	All employee records including salaries
job_history	Tracks past job positions for employees

Additionally, a view called emp_details_view combines relevant data from these tables for simplified access.

📋 Key Objectives
✅ Design a normalized HR schema with proper constraints

✅ Insert realistic data including multiple job roles, countries, and departments

✅ Establish all foreign key relationships between tables

✅ Create a view to simplify employee details extraction

✅ Execute business-level queries (e.g., top salaries, department assignments)

📦 Dataset Structure
The dataset contains:

🌍 25 countries and 4 regions

🏢 23 office locations

👔 27 departments

🧑‍💻 100+ employees with varying salaries and roles

💼 Job titles with salary bands

📅 Job histories for tracking employee transfers/promotions                                                                                                                                                            
 Basic Information Queries
Retrieve the first_name and department_id of the employee with the last name 'De Haan'.
```
select first_name,department_id from employees where last_name='DE HAAN';
+------------+---------------+
| first_name | department_id |
+------------+---------------+
| Lex        |            90 |
+------------+---------------+
1 row in set (0.001 sec)
```

Find all details of departments with the name 'Sales'.
```
select * from departments where department_name='sales';
+---------------+-----------------+------------+-------------+
| department_id | department_name | manager_id | location_id |
+---------------+-----------------+------------+-------------+
|            80 | Sales           |        145 |        2500 |
+---------------+-----------------+------------+-------------+
1 row in set (0.001 sec)
```

List all employees with a salary greater than 9700.

Get details of employees hired before January 1, 1992.

List employee ID, name, job ID, and department ID for employees in departments 20, 60, or 80.

List the same for employees not in departments 20, 60, or 80.



📊 Managerial and Salary Analysis
List last names, phone numbers, salaries, and manager IDs of employees whose manager ID is 100, 102, or 103.

Show first names and salaries of employees whose first names end with 'e'.

Display last names and department IDs of employees whose last name starts with the second letter 'i'.
(LIKE '_i%')

List all employees whose last names contain ‘L’, ‘J’, or ‘H’ and sort by salary in descending order.

🧠 Pattern Matching & Filters
Find employees with names starting with ‘J’.

Find departments where department_name ends with ‘s’.

List employees whose email starts with 'S'.

Find employees with the same first and last name (if any).

📈 Analytical & Business Logic
Get the count of employees in each department.

Find the total salary paid per department.

List employees with the maximum salary.

Find the average salary by job ID.

Get the highest and lowest salaries in the company.

📅 Job History & Time-based
List employees who have job history records (from job_history).

Find employees who changed jobs in the year 1998.

Show job history for a specific employee (e.g., employee_id = 101).

Get the total duration (in years/months) an employee worked in the company (from history).

🧾 View & Joins Based
Use the emp_details_view to list all employee names, department names, and region names.

Find employees along with their city and country.

Display all employee data joined with their department, location, country, and region.

📚 BONUS Suggestions (Not explicitly written but useful for practice):
List the number of employees hired per year.

Which job title has the highest number of employees?

Who is the highest-paid employee per department?

Which department has the highest average salary?
