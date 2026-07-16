
-- =========================
-- COMPARISON OPERATORS
-- =========================

SELECT * FROM Employees
WHERE salary >= 80000;

SELECT * FROM Employees
WHERE experience <= 3;

SELECT * FROM Employees
WHERE salary <> 45000;

SELECT * FROM Employees
WHERE salary < 50000;

SELECT * FROM Employees
WHERE experience > 5;


-- =========================
-- LOGICAL OPERATORS
-- =========================

SELECT * FROM Employees
WHERE department = 'IT' AND salary > 70000;

SELECT * FROM Employees
WHERE city = 'Hyderabad' OR city = 'Bangalore';

SELECT * FROM Employees
WHERE department = 'HR' AND experience < 3;

SELECT * FROM Employees
WHERE salary > 60000 OR experience > 6;

SELECT * FROM Employees
WHERE department <> 'Sales';


-- =========================
-- IN AND NOT IN
-- =========================

SELECT * FROM Employees
WHERE city IN ('Hyderabad', 'Mumbai');

SELECT * FROM Employees
WHERE department IN ('IT', 'Finance');

SELECT * FROM Employees
WHERE city NOT IN ('Chennai', 'Pune');

SELECT * FROM Employees
WHERE salary IN (45000, 75000, 91000);

SELECT * FROM Employees
WHERE department NOT IN ('HR', 'Sales');


-- =========================
-- BETWEEN
-- =========================

SELECT * FROM Employees
WHERE salary BETWEEN 50000 AND 80000;

SELECT * FROM Employees
WHERE experience BETWEEN 3 AND 6;

SELECT * FROM Employees
WHERE emp_id BETWEEN 105 AND 112;

SELECT * FROM Employees
WHERE salary NOT BETWEEN 40000 AND 60000;

SELECT * FROM Employees
WHERE experience BETWEEN 2 AND 4;


-- =========================
-- LIKE OPERATOR
-- =========================

SELECT * FROM Employees
WHERE emp_name LIKE 'R%';

SELECT * FROM Employees
WHERE emp_name LIKE '%a';

SELECT * FROM Employees
WHERE emp_name LIKE '%v%';

SELECT * FROM Employees
WHERE city LIKE 'B%';

SELECT * FROM Employees
WHERE department LIKE '%s';
