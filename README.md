# HR_EMPLOYEE_SQL_PROJECT
This project explores an HR Employee Management dataset that tracks employees, departments, projects, and work hours.
The goal is to analyze workforce distribution, productivity, and project engagement using real-world SQL queries and insights.

**🧱 Database Structure**

The database consists of four interrelated tables:

**Table Description**

departments Contains department details and IDs
employees Employee demographics, salaries, and department info
projects Projects owned by different departments
employee_projects Relationship table showing which employees worked on which projects, along with hours work


**🧠 Key SQL Concepts Applied**

Data retrieval using SELECT, WHERE, and ORDER BY

Table relationships with JOIN (INNER JOIN, LEFT JOIN)

Data aggregation using COUNT, SUM, AVG, MAX

Grouping and filtering with GROUP BY and HAVING

Limiting results with LIMIT

Data-driven storytelling through insights


# Query Objective SQL Concepts Key Insight

1 Display all employees and their departments JOIN, ORDER BY Basic employee-department mapping
2 Count of employees per department COUNT(), GROUP BY Helps HR assess department size
3 Average salary per department AVG(), GROUP BY Shows pay distribution across teams
4 List of all projects and their departments JOIN, ORDER BY Tracks project ownership
5 Number of employees per project COUNT(), GROUP BY Identifies team sizes per project
6 Employees working on more than one project HAVING COUNT() > 1 Shows multitasking staff
7 Top 5 employees by total hours worked SUM(), ORDER BY, LIMIT Highlights most productive workers
8 Top 5 employees by max hours on a single project MAX(), GROUP BY Identifies most dedicated project contributors


⚡ Sample Query – Top 5 Productive Employees

SELECT 
    e.employee_id,
    CONCAT(e.first_name, ' ', e.last_name) AS employee_name,
    SUM(ep.hours_worked) AS total_hours
FROM employees e
JOIN employee_projects ep 
    ON e.employee_id = ep.employee_id
GROUP BY e.employee_id, employee_name
ORDER BY total_hours DESC
LIMIT 5;

🧩 Example Output

employee_name total_hours

Ruth Okoro 168
David Kim 155
John Musa 150
Grace Odu 144
Anita Jones 141

💡 Business Insights

Workforce Distribution: Departments like IT and Engineering have the highest staff count.

Performance Recognition: Top 5 employees recorded over 140 total project hours — excellent for recognition or promotion consideration.

Workload Balance: A few employees contribute significantly more hours; this suggests the need for better task distribution.

Salary Review: Departments with lower average salaries may require compensation adjustments.


🧰 **Tools & Technologies**

SQL (MySQL) – Query writing & analysis

Excel – Data preparation and CSV formatting

GitHub – Documentation & portfolio management


🧑‍💻 Author

Solomon Adeniran
Data Analyst | PrimeSol Analytics
📍 Passionate about uncovering insights through data and storytelling with SQL, Excel, and Power BI.
Data Analyst | Skilled in SQL, Excel, and Power BI LinkedIn Profile www.linkedin.com/in/solomon-adetola-72445830b
