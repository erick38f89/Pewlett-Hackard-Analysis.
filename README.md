# Pewlett-Hackard-Analysis.

##Overview of Project

In this project, we use SQL, to generate a retiring employees list with the titles, and determine eligiblity criteria to retire and to participate in a mentorship program if not retiring.

##Results

We generated several tables to join the data from the employees and departments to determine the total of retiring employees. We created new tables with the associated values crated into new tables with SQL queries that create a total of employees retiring with the following commands:

SELECT e.emp_no,
       e.first_name,
       e.last_name,
       t.title,
       t.from_date,
       t.to_date
INTO retirement_titles
FROM employees as e
INNER JOIN titles as t
ON (e.emp_no = t.emp_no)
WHERE (e.birth_date BETWEEN '1952-01-01' AND '1955-12-31')
order by e.emp_no;

Those employess that don't get the specific retiring criteria may be elegible for a mentoring program in which  before the retirement time comes, they can transfer their knowledge and shared their activites with potential replacements.

##Summary

The analysis results in a variety of charts that confirm there will be many roles who could become vacant with a large upcoming silver sunset generation. The prospect of replacing this large number of retiring employees is not very realistic, therefore the mentoring program is a way to ramp down the sunset and have a better preparation for the employment gap for the company.
