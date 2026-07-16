-- =========================
-- SELECT
-- =========================

SELECT * FROM Employees;

SELECT emp_name, salary FROM Employees;

SELECT emp_name, department FROM Employees;

SELECT * FROM Employees
WHERE department = 'IT';

SELECT emp_name, experience FROM Employees;


-- =========================
-- WHERE
-- =========================

SELECT * FROM Employees
WHERE salary > 70000;

SELECT * FROM Employees
WHERE city = 'Hyderabad';

SELECT * FROM Employees
WHERE experience < 4;

SELECT * FROM Employees
WHERE department = 'Finance';

SELECT * FROM Employees
WHERE salary = 52000;


-- =========================
-- GROUP BY
-- =========================

SELECT department, SUM(salary) AS Total_Salary
FROM Employees
GROUP BY department;

SELECT department, AVG(salary) AS Average_Salary
FROM Employees
GROUP BY department;

SELECT city, COUNT(*) AS Employee_Count
FROM Employees
GROUP BY city;

SELECT department, MAX(salary) AS Maximum_Salary
FROM Employees
GROUP BY department;

SELECT department, MIN(experience) AS Minimum_Experience
FROM Employees
GROUP BY department;


-- =========================
-- HAVING
-- =========================

SELECT department, COUNT(*) AS Employee_Count
FROM Employees
GROUP BY department
HAVING COUNT(*) > 3;

SELECT department, AVG(salary) AS Average_Salary
FROM Employees
GROUP BY department
HAVING AVG(salary) > 60000;

SELECT city, COUNT(*) AS Employee_Count
FROM Employees
GROUP BY city
HAVING COUNT(*) > 2;

SELECT department, SUM(salary) AS Total_Salary
FROM Employees
GROUP BY department
HAVING SUM(salary) > 200000;

SELECT department, MAX(salary) AS Maximum_Salary
FROM Employees
GROUP BY department
HAVING MAX(salary) > 90000;


-- =========================
-- TOP
-- =========================

SELECT TOP 5 * FROM Employees
ORDER BY salary DESC;

SELECT TOP 3 * FROM Employees
ORDER BY experience DESC;

SELECT TOP 2 * FROM Employees
WHERE department = 'Finance'
ORDER BY salary DESC;

SELECT TOP 4 * FROM Employees
WHERE city = 'Hyderabad';

SELECT TOP 1 * FROM Employees
ORDER BY salary DESC;


-- =========================
-- DISTINCT
-- =========================

SELECT DISTINCT department FROM Employees;

SELECT DISTINCT city FROM Employees;

SELECT DISTINCT salary FROM Employees;

SELECT DISTINCT department, city FROM Employees;

SELECT DISTINCT experience FROM Employees;

