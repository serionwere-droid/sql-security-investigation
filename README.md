 SQL Security Investigation Project
Project Overview

This project demonstrates the use of SQL queries to investigate login attempts and identify potential security threats within an organization. The primary focus was detecting suspicious logins occurring outside normal working hours (after 18:00) and analyzing employee access patterns.

Objectives

Detect failed login attempts after working hours

Investigate login activity on specific dates

Identify login attempts originating outside Mexico

Review employee department access

Practice SQL filtering using WHERE, AND, OR, and NOT

 Technologies Used

SQL

Database Filtering Techniques

Cybersecurity Investigation Methods

 After-Hours Failed Login Attempts
SELECT *
FROM log_in_attempts
WHERE login_time > '18:00' AND success = FALSE;


Goal:
Identify failed login attempts occurring after business hours that may indicate unauthorized access.

 Login Attempts on Specific Dates
SELECT *
FROM log_in_attempts
WHERE login_date = '2022-05-08' OR login_date = '2022-05-09';


Goal:
Analyze login activity on selected dates to detect unusual patterns or repeated failures.

 Login Attempts Outside Mexico
SELECT *
FROM log_in_attempts WHERE NOT country LIKE 'MEX%';


Goal:
Detect potentially suspicious login attempts originating from outside the organization's operating region.

 Employees in the Marketing Department
SELECT *
FROM employees
WHERE department = 'Marketing' AND office LIKE 'East%';


Goal:
Review Marketing department employees located in East offices for unusual login behavior.

 Employees in Finance or Sales
SELECT *
FROM employees
WHERE department = 'Finance' OR department = 'Sales';


Goal:
Monitor access activity in departments that manage sensitive financial and business data.

 Employees Not in IT
SELECT *
FROM employees
WHERE department = 'information technology';


Goal:
Evaluate system access from non-IT staff who typically have limited administrative privileges.

 Key Skills Demonstrated

SQL data filtering

Security investigation

Analytical thinking

Threat detection

Database querying

 Project Summary

This investigation analyzed login attempts across multiple departments to detect suspicious behavior and reduce the risk of data breaches. By leveraging SQL filtering techniques, it was possible to uncover unusual access patterns, monitor high-risk departments, and support the development of stronger security countermeasures.
