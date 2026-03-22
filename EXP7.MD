# <center> EXPERIMENT 7
## 1. Compute the no. of days remaining in this year.
```sql
SELECT DATEDIFF(
    -> CONCAT(YEAR(CURDATE()),'-12-31'),CURDATE());
```
## 2. Find the highest and lowest salaries and the difference between of them.
```sql
SELECT
    -> MAX(SAL) AS HIGHEST_SALARY,
    -> MIN(SAL) AS LOWEST_SALARY,
    -> MAX(SAL) - MIN(SAL) AS DIFFERENCE
    -> FROM EMPLOYEE;
```
## 3. List employee whose commission is greater than 25% of their salaries.
```sql
 SELECT ENAME, SAL, COMM
    -> FROM EMPLOYEE
    -> WHERE COMM > (SAL * 0.25);
```
## 4. Make a query that displays salary in dollar format.
```sql
SELECT ENAME,
    -> CONCAT('$', FORMAT(SAL, 2)) AS SALARY_IN_DOLLAR
    -> FROM EMPLOYEE;
```
## 5. Create a matrix query to display the job,the salary 
```sql
 SELECT JOB,
    -> SUM(CASE WHEN DEPTNO = 10 THEN SAL ELSE 0 END) AS DEPT10,
    -> SUM(CASE WHEN DEPTNO = 20 THEN SAL ELSE 0 END) AS DEPT20,
    -> SUM(CASE WHEN DEPTNO = 30 THEN SAL ELSE 0 END) AS DEPT30,
    -> SUM(CASE WHEN DEPTNO = 40 THEN SAL ELSE 0 END) AS DEPT40,
    -> SUM(SAL) AS TOTAL_SALARY
    -> FROM EMPLOYEE
    -> GROUP BY JOB;
```
## 6.
```sql
SELECT
    -> COUNT(*) AS TOTAL_EMPLOYEES,
    -> SUM(CASE WHEN YEAR(HIREDATE) = 1980 THEN 1 ELSE 0 END) AS "1980",
    -> SUM(CASE WHEN YEAR(HIREDATE) = 1981 THEN 1 ELSE 0 END) AS "1981",
    -> SUM(CASE WHEN YEAR(HIREDATE) = 1982 THEN 1 ELSE 0 END) AS "1982",
    -> SUM(CASE WHEN YEAR(HIREDATE) = 1983 THEN 1 ELSE 0 END) AS "1983"
    -> FROM EMPLOYEE;
```
## 7.
```sql
SELECT DATE_SUB(
    -> LAST_DAY('2026-02-10'),
    -> INTERVAL (WEEKDAY(LAST_DAY('2026-02-10')) + 1)
    -> DAY) AS LAST_SUNDAY;
```
## 8.
```sql
SELECT DEPTNO, COUNT(*) AS TOTAL_EMPLOYEES
    -> FROM EMPLOYEE
    -> GROUP BY DEPTNO;
```
## 9.
```sql
SELECT JOB, COUNT(*) AS TOTAL_EMPLOYEES
    -> FROM EMPLOYEE
    -> GROUP BY JOB;
```
## 10.
```sql
SELECT DEPTNO, SUM(SAL) AS TOTAL_SALARY
    -> FROM EMPLOYEE
    -> GROUP BY DEPTNO;
```